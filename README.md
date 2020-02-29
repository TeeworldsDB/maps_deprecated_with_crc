# TeeworldsDB maps

A mirror of http://heinrich5991.de/teeworlds/maps/maps/

**WARNING INCOMPLETE**

The wget command does not get files hidden by nginx and thus all maps starting with a . are not in this mirror.
See http://heinrich5991.de/teeworlds/maps/LISTING for a complete list.

```
# dependencys
apt install figlet wget git

# download from heinrich5991.de
wget -r -np -nH --cut-dirs=3 -R index.html http://heinrich5991.de/teeworlds/maps/maps/

# commit to the mirror
for l in {a..z}; do figlet "$l"; git add ${l}*;git commit -m "Add maps ${l}*";git push;sleep 10;done
for l in {A..Z}; do figlet "$l"; git add ${l}*;git commit -m "Add maps ${l}*";git push;sleep 10;done
for l in {0..9}; do figlet "$l"; git add ${l}*;git commit -m "Add maps ${l}*";git push;sleep 10;done
git add .
git commit -m "Add maps *"
git push
```

