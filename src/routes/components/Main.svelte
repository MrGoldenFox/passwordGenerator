<script>
	const characters = [
		'A',
		'B',
		'C',
		'D',
		'E',
		'F',
		'G',
		'H',
		'I',
		'J',
		'K',
		'L',
		'M',
		'N',
		'O',
		'P',
		'Q',
		'R',
		'S',
		'T',
		'U',
		'V',
		'W',
		'X',
		'Y',
		'Z',
		'a',
		'b',
		'c',
		'd',
		'e',
		'f',
		'g',
		'h',
		'i',
		'j',
		'k',
		'l',
		'm',
		'n',
		'o',
		'p',
		'q',
		'r',
		's',
		't',
		'u',
		'v',
		'w',
		'x',
		'y',
		'z',
		'0',
		'1',
		'2',
		'3',
		'4',
		'5',
		'6',
		'7',
		'8',
		'9',
		'~',
		'`',
		'!',
		'@',
		'#',
		'$',
		'%',
		'^',
		'&',
		'*',
		'(',
		')',
		'_',
		'-',
		'+',
		'=',
		'{',
		'[',
		'}',
		']',
		',',
		'|',
		':',
		';',
		'<',
		'>',
		'.',
		'?',
		'/'
	];
	let passwordFirstField = '';
	let passwordSecondField = '';

	function generatePassword() {
		if (passwordFirstField !== '') {
			passwordFirstField = '';
		}
		for (let i = 0; i < 15; i++) {
			let index = Math.floor(Math.random() * characters.length);
			passwordFirstField += characters[index];
		}

		if (passwordSecondField !== '') {
			passwordSecondField = '';
		}
		for (let i = 0; i < 15; i++) {
			let index = Math.floor(Math.random() * characters.length);
			passwordSecondField += characters[index];
		}
	}
</script>

<main>
	<section>
		<div class="content">
			<h1>
				<span style="color: white">Generate a </span><span style="color: #55F991"
					>random password</span
				>
			</h1>
			<p>Never use an insecure password again.</p>
			<button on:click={generatePassword}>Generate passwords</button>
			<hr />
			<div class="Passwords">
				<p id="field1">{passwordFirstField}</p>
				<p id="field2">{passwordSecondField}</p>
			</div>
		</div>
	</section>
</main>

<style>
	main {
		position: absolute;
		background-color: #1c1c1c;
		width: 100%;
		height: 100vh;
		text-align: left;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	section {
		background-color: #1f2937;
		width: 90%;
		height: 90vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	.content {
		width: 80%;
		margin: 0px auto;
	}

	h1 {
		font-family: 'Karla', sans-serif;
		font-weight: 800;
		font-size: 2.5rem;
		line-height: 40px;
		letter-spacing: -2.5%;
		margin: 0;
	}

	p {
		color: #d5d4d8;
		font-family: 'Inter', sans-serif;
		font-weight: 400;
		font-size: 1.2rem;
		line-height: 28px;
		margin: 5px 0px 50px 0px;
	}

	button {
		font-family: 'Inter', sans-serif;
		font-weight: 500;
		font-size: 1rem;
		line-height: 24px;
		width: 191px;
		height: 42px;
		background-color: #10b981;
		border-radius: 6px;
		border: none;
		color: #ffffff;
		margin-bottom: 30px;
	}

	button:active {
		background-color: #0a4a3c;
	}

	hr {
		margin-bottom: 50px;
		display: block;
		height: 1px;
		border: 0;
		border-top: 1px solid #2f3e53;
		margin: 1em 0;
		padding: 0;
	}

	.Passwords {
		display: flex;
		flex-wrap: wrap;
		flex-grow: 1;
	}

	.Passwords P {
		display: flex;
		background-color: #273549;
		width: 211px;
		height: 39px;
		border: none;
		margin: 20px 20px 20px 0px;
		border-radius: 6px;
		color: #55f991;
		justify-content: center;
		align-items: center;
		letter-spacing: 1.05px;
		font-size: 0.9em;
	}

	@media only screen and (min-width: 1100px) {
		button:hover {
			background-color: #0e6e52;
		}

		button:active {
			background-color: #0a4a3c;
		}
	}
</style>
