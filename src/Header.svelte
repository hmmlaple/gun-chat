<script>
  import { username, user } from './user';

  function signout() {
    user.leave();
    username.set('');
  }
</script>

<header>
<h1>sussy chat</h1>
  {#if $username}
    <div class="user-bio">
      
      <span>You are logged in as: <strong>{$username}</strong></span>
      <img src={`https://avatars.dicebear.com/api/initials/${$username}.svg`} alt="avatar" /> 
    </div>

    <button class="signout-button" on:click={signout}>Log Out</button>

    {:else}

      <h3>sussy chat</h3>
  {/if}
</header>