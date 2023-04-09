<script>
    import Dashboard from "./lib/Dashboard.svelte";
    //DARKMODE
    let isDarkMode = true;

    const handleDarkMode = () => {
        isDarkMode = isDarkMode ? false : true;
    };
    //DISGUISE NavBar
    let isHidden = false;

    const handleHidden = () => {
        isHidden = isHidden ? false : true;
    }

</script>

<div class={ isDarkMode ? 'dark' : '' }>
    <header>
        <Dashboard
            isDarkMode={ isDarkMode }
            handleDarkMode={ handleDarkMode }

            isHidden={ isHidden }
            handleHidden={ handleHidden }
        />
    </header>
</div>

<style>
    div {
        /* ====Colors==== */
        --body-color: #E4E9F7;
        --sidebar-color: #fff;
        --primary-color: #695cfe;
        --primary-color-light: #f6f5ff;
        --toggle-color: #ddd;
        --text-color: #707070;

        /* ====Transition==== */
        --tran-02: all 0.2s;
        --tran-03: all 0.3s;
        --tran-04: all 0.4s;
        --tran-05: all 0.5s;
    }

    .dark {
        /* ====Colors==== */
        --body-color: #18191a;
        --sidebar-color: #242526;
        --primary-color: #3a3b3c;
        --primary-color-light: #3a3b3c;
        --toggle-color: #fff;
        --text-color: #ccc;
    }

    header {
        display: grid;
        justify-content: center;
    }
</style>
