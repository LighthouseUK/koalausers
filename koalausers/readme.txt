This module requires the following:

# Queue definition

The parameters are all customisable, except the name.

queue:
- name: search_index_update
  mode: push
  bucket_size: 100
  rate: 1/s
  retry_parameters:
    task_age_limit: 1d
    min_backoff_seconds: 30
    max_backoff_seconds: 600


# Dependencies

- App Engine NDB
- App Engine deferred library