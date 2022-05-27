# this is my compilation of useful snippets

### log filter
```bash
# show all usernames that had invalid login attempts. make a count on it
cat auth.log | grep "invalid" | cut -d " " -f 11 | sort | uniq | wc -l
# exclude everythin with 'Restore' 
cat auth.log | grep "invalid" | grep -v "Restore"

```
### scp down/upload
this snippet was taken from https://stackoverflow.com/questions/343711/transferring-files-over-ssh
```bash
# download: remote -> local
scp user@remote_host:remote_file local_file 
# upload: local -> remote
scp local_file user@remote_host:remote_file
```
### code (test)coverage report in python
assuming that bo_socialhub_notifyer is your module and test_bo_socialhub_notifyer are your unittests.
```bash
pytest -v --cov=bo_socialhub_notifyer --cov-report=html;open htmlcov/index.html
```

