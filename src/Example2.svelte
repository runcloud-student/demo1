<script>
    export var str = "i have learned something new today";
    function capitalizeFirstCharOfEachWord() {
        var strArray = str.split(" ");
        var i;
        for (i = 0; i < strArray.length; i++) {
            strArray[i] =
                strArray[i].charAt(0).toUpperCase() + strArray[i].slice(1); //Capitalize the first character and join with the remain characters of the word
        }
        str = strArray.join(" ");
    }
</script>

<main>
    <div>
        <h1>
            Example 2 - Capitalize the 1st character of each word in a given
            string.
        </h1>
        <p>
            <button on:click={capitalizeFirstCharOfEachWord}>
                Capitalize the 1st character of each word
            </button>
        </p>
        <p>
            {str}
        </p>
    </div>
</main>
