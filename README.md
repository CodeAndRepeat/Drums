# Drums

[Link to application](https://codeandrepeat.github.io/Drums)


### Play sound function:
```javascript
function playSound(e) {
            const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`);
            const key = document.querySelector(`.key[data-key="${e.keyCode}"]`);
            if (!audio) return;
            audio.currentTime = 0;
            audio.play();
            key.classList.add('playing');
        }
```

### Remove transition from key: 
``` javascript
function removeTransition(e) {
            if (e.propertyName !== 'transform') return;
            this.classList.remove('playing');
        }
```

## License

`Drums application` is available under the MIT license.

