#### `activate(owner, repo)`
  
  Enables repo on Travis CI. Return value indicates whether repo was enabled.

---

 #### `auto_cancel(owner, repo)`
  
   Enables auto-cancellation of branch builds. Return value indicates whether auto-cancellation was enabled.

---

#### `build(owner, repo, branch)`

  Triggers build for owner/repo:branch. Return value indicates whether build request was accepted.

---

#### `get_jobs(build_id)`

  Fetches the list of jobs of the build whose id is `build_id` where each job is represented per https://developer.travis-ci.com/resource/job#standard-representation. Returns `None` on error (e.g., no such build, or call failed).

---

#### `get_log_parts(job_id)`

  Fetches the contents of the log for the job whose id is `job_id`, and returns a list of that log's parts, where each part is a dictionary with two keys: `number`, and `content`. Returns `None` on failure.

---

#### `get_repo(owner, repo)`

  Returns repo object for owner/repo per https://developer.travis-ci.com/resource/repository#standard-representation. Returns `None` on error.

---

#### `get_user()`

  Fetches information about the current user, and returns a user object per https://developer.travis-ci.com/resource/user#standard-representation.

---

#### `sync()`

  Syncs user's repos on Travis CI, and returns `True` when syncing is complete. Returns `None` on error. 
