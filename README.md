# git-find-files


for branch in $(git rev-list --all)
do
  if (git ls-tree -r --name-only $branch | grep --quiet "$1") 
  then
     echo $branch
  fi
done
