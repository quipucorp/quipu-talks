# Quipu talks

Videos to GIF 
```
ffmpeg -i input.mp4  -vf fps=10 -loop 1 output.gif
```

Build and serve presentation
```
marp -I ./docs -o ./docs &&  marp -s ./docs
```
