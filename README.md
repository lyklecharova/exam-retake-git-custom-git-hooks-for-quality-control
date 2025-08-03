<h1>commit-msg</h1>

<p>
#!/bin/sh
MSG_FILE=$1
cat "$MSG_FILE" | grep -E '^(PROJ-[0-9]+): ' || {
  echo "❌ Commit message must start with a ticket number like 'PROJ-123: Description'"
  exit 1
}

</p>
<br/>
<h1>pre-push</h1>

<p>
#!/bin/sh

echo "🧪 Running tests before push..."
npm test

if [ $? -ne 0 ]; then
echo "❌ Tests failed. Push aborted."
exit 1
fi

echo "✅ Tests passed. Proceeding with push"

</p>
 <br/>

 <ul>
    <li>
    <p>This is a git log graph</p>
<img src="./git log --oneline --graph --all.png" alt="git log --oneline --graph --all"/>
    </li>
    <li>
    
<p>This is a git reflog history</p>
<img src="./git reflog.png" alt="reflog"/>
    </li>
</ul>
