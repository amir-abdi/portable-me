SHELL=/bin/bash
CONDA_ACTIVATE=source $$(conda info --base)/etc/profile.d/conda.sh ; conda activate
MAIN_BRANCH=main

# Exclude certain file name patterns from the check
EXCLUDE_PY= \
    ':!*/test_*.py' \
    ':!*/__init__.py' \
    ':!*/conftest.py'

TOPIC_BRANCH_NAME:=$(shell git symbolic-ref --short HEAD)

# To apply a rule only on changed files of the branch (compared to the $(MAIN_BRANCH)) and
# those currently staged (i.e., --cached) in local git.
ifeq ($(TOPIC_BRANCH_NAME), $(MAIN_BRANCH))
    CHANGED_FILES=git diff HEAD HEAD^ \
        --diff-filter=d --name-only --exit-code -- '*.py' $(EXCLUDE_PY)
else
    BRANCHING_POINT_COMMIT:=$(shell diff -u <(git rev-list --first-parent $(TOPIC_BRANCH_NAME)) \
        <(git rev-list --first-parent $(MAIN_BRANCH)) | \
        sed -ne 's/^ //p' | head -1)
    CHANGED_FILES=git diff $(BRANCHING_POINT_COMMIT) \
        --diff-filter=d --cached --name-only --exit-code -- '*.py' $(EXCLUDE_PY)
endif

some-rule:
    $(CONDA_ACTIVATE) env-name && \
    $(CHANGED_FILES) | xargs some-tool

