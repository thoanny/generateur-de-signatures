<script>
</script>

<main>
	<div class="container mx-auto my-12 flex gap-6">
		<div class="w-1/3">
			<div class="bg-gray-100 rounded p-4 border">

				<!-- Formulaire -->

				<h4 class="text-2xl font-semibold">Générateur de signatures</h4>

				<h5 class="text-lg font-semibold mt-4">Identité</h5>

				<label for="photo">Photographie</label>
				<input type="text" id="photo" />

				<label for="fullname">Prénom et nom</label>
				<input type="text" id="fullname" />

				<label for="logo">Logo</label>
				<input type="text" id="logo" />

				<label for="jobtitle">Titre ou poste</label>
				<input type="text" id="jobtitle" />

				<label for="department">Service</label>
				<input type="text" id="department" />

				<label for="company">Entreprise</label>
				<input type="text" id="company">

				<label for="phone">Téléphone</label>
				<input type="text" id="phone">

				<label for="mobile">Mobile</label>
				<input type="text" id="mobile">

				<label for="email">E-mail</label>
				<input type="email" id="email">

				<label for="website">Site internet</label>
				<input type="url" id="website">

				<h5 class="text-lg font-semibold mt-4">Adresse</h5>

				<label for="addressline1">Adresse ligne 1</label>
				<input type="text" id="addressline1">

				<label for="addressline2">Adresse ligne 2</label>
				<input type="text" id="addressline2">

				<label for="addressline3">Adresse ligne 3</label>
				<input type="text" id="addressline3">

				<label for="zipcode">Code postal</label>
				<input type="text" id="zipcode">

				<label for="locality">Ville</label>
				<input type="text" id="locality">

				<label for="country">Pays</label>
				<input type="text" id="country">

				<h5 class="text-lg font-semibold mt-4">Réseaux sociaux numériques</h5>

				<label for="facebook">Facebook</label>
				<input type="url" id="facebook">

				<label for="twitter">Twitter</label>
				<input type="url" id="twitter">

				<label for="linkedin">LinkedIn</label>
				<input type="url" id="linkedin" />

				<label for="instagram">Instagram</label>
				<input type="url" id="instagram" />

				<label for="youtube">YouTube</label>
				<input type="url" id="youtube" />

				<h5 class="text-lg font-semibold mt-4">Bannière</h5>

				<label for="bannerimage">Image de la bannière</label>
				<input type="text" id="bannerimage" />

				<label for="bannerurl">URL au clic</label>
				<input type="url" id="bannerurl" />

				<h5 class="text-lg font-semibold mt-4">Autre</h5>

				<label for="ecofriendly">Éco-responsable</label>
				<textarea id="ecofriendly" cols="30" rows="6">Protégeons la nature : imprimez cet e-mail seulement si nécessaire et pensez à recycler votre papier.</textarea>

				<label for="privacy">Avis de confidentialité</label>
				<textarea id="privacy" cols="30" rows="6">Le présent message, ainsi que tout fichier qui y est joint, est destiné exclusivement à l’intention de son ou de ses destinataires. Il peut contenir des informations confidentielles. Si vous n'êtes pas le ou la destinataire de ce message, nous vous avisons par la présente que tout usage, reproduction ou diffusion de ce message et de tout fichier qui y est joint est strictement interdit. Si ce message vous a été transmis par erreur, veuillez en aviser sans délai l'expéditeur en lui retournant ledit message et ensuite le détruire, ainsi que tout fichier joint sans en conserver de copie.</textarea>
			</div>
		</div>
		<div class="w-2/3">

			<!-- Prévisualisation -->
			
		</div>
	</div>
</main>

<style>

	label:not(.checkbox) {
		display: block;
		font-weight: 600;
		margin-bottom: .25rem;
		margin-top: .5rem;
	}

	input[type="text"], input[type="url"], input[type="email"], textarea {
		border: 1px solid rgb(156, 163, 175);
		padding: .25rem .75rem;
		border-radius: .25rem;
		width: 100%;
	}

	textarea {
		min-height: 6rem;
		max-height: 15rem;
	}

</style>
