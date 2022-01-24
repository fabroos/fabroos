### Hi there 👋

```js
player.addListener('ready', ({
        device_id
    }) => {
        console.log('Ready with Device ID', device_id);
        let contador = setInterval(() => {


            // contador universal de la app
            player.getCurrentState().then(state => {
                if (!state) {
                    console.error('User is not playing music through the Web Playback SDK');
                    return;
                }
                document.querySelector(".progress").style.width = `${100 * state.position / state.duration}%`;
                bar.value = state.position;
                bar.max = state.duration;
                document.querySelector(".actual-second").textContent = millisToMinutesAndSeconds(state.position);
            });
        }, 600);

    });
```

<!--
**fabroos/fabroos** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
