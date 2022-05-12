# This is my compilation of useful snippets

### log filter
show all usernames that had invalid login attempts. make a count on it

```bash
cat auth.log | grep "invalid" | cut -d " " -f 11 | sort | uniq | wc -l
```