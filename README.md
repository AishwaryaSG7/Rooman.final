<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Music Playlist Generator</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }

        #playlist-generator {
            text-align: center;
            padding: 20px;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        label {
            display: block;
            margin-bottom: 10px;
        }

        select,
        input[type="range"] {
            width: 100%;
            padding: 8px;
            margin-bottom: 20px;
            box-sizing: border-box;
        }

        button {
            padding: 10px 20px;
            background-color: #4caf50;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: #45a049;
        }

        #playlist-output {
            margin-top: 20px;
        }
    </style>
</head>

<body>
    <div id="playlist-generator">
        <h2>Music Playlist Generator</h2>
        <label for="mood">Select Mood:</label>
        <select id="mood">
            <option value="happy">Happy</option>
            <option value="sad">Sad</option>
            <option value="energetic">Energetic</option>
            <option value="relaxed">Relaxed</option>
        </select>

        <label for="tempo">Select Tempo:</label>
        <input type="range" id="tempo" min="1" max="10" value="5">

        <label for="genre">Select Genre:</label>
        <select id="genre">
            <option value="pop">Pop</option>
            <option value="rock">Rock</option>
            <option value="hip-hop">Hip-Hop</option>
            <option value="electronic">Electronic</option>
        </select>

        <button onclick="generatePlaylist()">Generate Playlist</button>

        <div id="playlist-output"></div>
    </div>

    <script>
        function generatePlaylist() {
            const mood = document.getElementById('mood').value;
            const tempo = document.getElementById('tempo').value;
            const genre = document.getElementById('genre').value;

            const playlistOutput = document.getElementById('playlist-output');
            playlistOutput.innerHTML = `<p>Generated Playlist:</p>
                                        <p>Mood: ${mood}</p>
                                        <p>Tempo: ${tempo}</p>
                                        <p>Genre: ${genre}</p>`;
        }
    </script>
</body>

</html>
