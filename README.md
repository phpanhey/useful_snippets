# This is my compilation of useful snippets

### log filter
```bash
# show all usernames that had invalid login attempts. make a count on it
cat auth.log | grep "invalid" | cut -d " " -f 11 | sort | uniq | wc -l
# exclude everythin with 'Restore' 
cat auth.log | grep "invalid" | grep -v "Restore"

```