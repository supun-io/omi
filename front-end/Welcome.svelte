<script lang="ts">

    let authType : 'login' | 'signup' = 'login';

</script>

<style>

    #welcome {
        display: flex;
        width: 100%;
        height: 100vh;
        align-items: center;
        justify-content: center;
    }

    .center {
        width: 550px;
        margin: auto;
    }

    .auth {
        margin-top: 25px;
        padding: 25px 0;
        border-top: 1px solid #eee;
        border-bottom: 1px solid #eee;
    }

    .login-signup button {
        border: none;
        padding: 4px;
        background-color: transparent;
        cursor: pointer;
        font-weight: 600;
    }
    .login-signup button.active {
        color: var(--accent);
    }

    form {
        padding: 20px 0;
        width: 200px;
    }

    input {
        display: block;
        width: 100%;
        margin-bottom: 15px;
        padding: 8px 15px;
        border-radius: 5px;
        border: none;
        background-color: #eee;
    }

    input:focus {
        outline: 2px solid var(--accent);
    }

    button[type="submit"] {
        margin-top: 5px;
        background-color: var(--accent);
        border: none;
        padding: 8px 15px;
        color: white;
        border-radius: 5px;
        cursor: pointer;
        font-weight: 600;
    }

    .made-by {
        padding-top: 25px;
        font-size: 0.9rem;
    }
    .made-by a {
        color: var(--accent);
    }

    svg {
        vertical-align: middle;
        margin-right: 2px;
    }
    svg + a {
        vertical-align: middle;
    }

</style>

<div id="welcome">

    <div class="center">

        <h1>OMI ♠️</h1>

        <div class="intro">
            Omi is a popular 4-player card game in Sri Lanka 🇱🇰. Invite your friends and have fun!
        </div>

        <div class="auth">

            <div class="login-signup">
                <button class="login" class:active={authType === 'login'} on:click={() => authType = 'login'}>Login</button>
                <button class="signup" class:active={authType === 'signup'} on:click={() => authType = 'signup'}>Signup</button>
            </div>

            <form>

                <input type="text" name="username" placeholder="Username" />
                <input type="password" name="password" placeholder="Password" />

                <button type="submit">{ authType === 'login' ? "Log in" : "Create Account" }</button>

            </form>

        </div>

        <div class="made-by">
            Made with ❤️ by <a href="https://supun.io" target="_blank">Supun</a>
            <span style="float: right">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-github" viewBox="0 0 16 16">
                    <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
                </svg>
                <a style="text-decoration: none;color: inherit" href="https://github.com/supun-io/omi" target="_blank">Contribute</a>
            </span>
        </div>

    </div>

</div>
