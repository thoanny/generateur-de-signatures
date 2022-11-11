<script>

	import { imask } from 'svelte-imask';
	import { color, inputs } from '../public/config.json';

	let addressline4 = null;
	updateAddressLine4();

	function updateAddressLine4() {
		let parts = [];

		if(inputs.zipcode.value) {
			parts.push(inputs.zipcode.value)
		}

		if(inputs.locality.value) {
			parts.push(inputs.locality.value)
		}

		if(inputs.country.value) {
			parts.push(inputs.country.value)
		}

		if(parts.length > 0) {
			addressline4 = parts.join(', ');
		} else {
			addressline4 = null;
		}

	}

</script>

<main>
	<div id="wrapper">
		<div id="sidebar">
			<div>

				<!-- Formulaire -->

				<h1 class="text-2xl font-semibold">Générateur de signatures</h1>

				<h4 class="text-lg font-semibold mt-4">Identité</h4>

				<form autocomplete="off">

					{#if inputs.photo.show}
						<label for="photo">Photographie (140&times;140)</label>
						<div class="input url">
							<input type="text" id="photo" bind:value={inputs.photo.value} />
						</div>
					{/if}

					{#if inputs.fullname.show}
						<label for="fullname">Prénom et nom</label>
						<div class="input text">
							<input type="text" id="fullname" bind:value={inputs.fullname.value} />
						</div>
					{/if}

					{#if inputs.logo.show}
						<label for="logo">Logo</label>
						<div class="input url">
							<input type="text" id="logo" bind:value={inputs.logo.value} />
						</div>
					{/if}

					{#if inputs.title.show}
						<label for="jobtitle">Titre ou poste</label>
						<div class="input text">
							<input type="text" id="title" bind:value={inputs.title.value} />
						</div>
					{/if}

					{#if inputs.department.show}
						<label for="department">Service</label>
						<div class="input text">
							<input type="text" id="department" bind:value={inputs.department.value} />
						</div>
					{/if}

					{#if inputs.company.show}
						<label for="company">Entreprise</label>
						<div class="input text">
							<input type="text" id="company" bind:value={inputs.company.value} />
						</div>
					{/if}

					{#if inputs.phone.show}
						<label for="phone">Téléphone</label>
						<div class="input phone">
							<input type="text" id="phone" bind:value={inputs.phone.value} use:imask={{ mask: '00 00 00 00 00' }} />
						</div>
					{/if}

					{#if inputs.mobile.show}
						<label for="mobile">Mobile</label>
						<div class="input phone">
							<input type="text" id="mobile" bind:value={inputs.mobile.value} use:imask={{ mask: '00 00 00 00 00' }} />
						</div>
					{/if}

					{#if inputs.email.show}
						<label for="email">E-mail</label>
						<div class="input email">
							<input type="email" id="email" bind:value={inputs.email.value} />
						</div>
					{/if}

					{#if inputs.website.show}
						<label for="website">Site internet</label>
						<div class="input url">
							<input type="url" id="website" bind:value={inputs.website.value} />
						</div>
					{/if}
		
					<h4>Adresse</h4>

					{#if inputs.addressline1.show}
						<label for="addressline1">Adresse ligne 1</label>
						<div class="input text">
							<input type="text" id="addressline1" bind:value={inputs.addressline1.value} />
						</div>
					{/if}

					{#if inputs.addressline2.show}
						<label for="addressline2">Adresse ligne 2</label>
						<div class="input text">
							<input type="text" id="addressline2" bind:value={inputs.addressline2.value} />
						</div>
					{/if}
	
					{#if inputs.addressline3.show}
						<label for="addressline3">Adresse ligne 3</label>
						<div class="input text">
							<input type="text" id="addressline3" bind:value={inputs.addressline3.value} />
						</div>
					{/if}

					{#if inputs.zipcode.show}
						<label for="zipcode">Code postal</label>
						<div class="input text">
							<input type="text" id="zipcode" bind:value={inputs.zipcode.value} on:keyup={updateAddressLine4} />
						</div>
					{/if}

					{#if inputs.locality.show}
						<label for="locality">Ville</label>
						<div class="input text">
							<input type="text" id="locality" bind:value={inputs.locality.value} on:keyup={updateAddressLine4} />
						</div>
					{/if}

					{#if inputs.country.show}
						<label for="country">Pays</label>
						<div class="input text">
							<input type="text" id="country" bind:value={inputs.country.value} on:keyup={updateAddressLine4}>
						</div>
					{/if}

					{#if inputs.facebook.show || inputs.twitter.show || inputs.linkedin.show || inputs.instagram.show || inputs.youtube.show}
						<h4>Réseaux sociaux numériques</h4>
					{/if}

					{#if inputs.facebook.show}
						<label for="facebook">Facebook</label>
						<div class="input url">
							<input type="url" id="facebook" bind:value={inputs.facebook.value} />
						</div>
					{/if}

					{#if inputs.twitter.show}
						<label for="twitter">Twitter</label>
						<div class="input url">
							<input type="url" id="twitter" bind:value={inputs.twitter.value} />
						</div>
					{/if}

					{#if inputs.linkedin.show}
						<label for="linkedin">LinkedIn</label>
						<div class="input url">
							<input type="url" id="linkedin" bind:value={inputs.linkedin.value} />
						</div>
					{/if}

					{#if inputs.instagram.show}
						<label for="instagram">Instagram</label>
						<div class="input url">
							<input type="url" id="instagram" bind:value={inputs.instagram.value} />
						</div>
					{/if}

					{#if inputs.youtube.show}
						<label for="youtube">YouTube</label>
						<div class="input url">
							<input type="url" id="youtube" bind:value={inputs.youtube.value} />
						</div>
					{/if}

					{#if inputs.bannerimg.show || inputs.bannerurl.show}
						<h4>Bannière</h4>
					{/if}

					{#if inputs.bannerimg.show}
						<label for="bannerimg">Image de la bannière (400&times;100)</label>
						<div class="input url">
							<input type="text" id="bannerimage" bind:value={inputs.bannerimg.value} />
						</div>
					{/if}

					{#if inputs.bannerurl.show}
						<label for="bannerurl">URL au clic</label>
						<div class="input url">
							<input type="url" id="bannerurl" bind:value={inputs.bannerurl.value} />
						</div>
					{/if}

					{#if inputs.ecofriendly.show ||inputs.privacy.show }
						<h4>Autres</h4>
					{/if}

					{#if inputs.ecofriendly.show}
						<label for="ecofriendly">Éco-responsable</label>
						<textarea id="ecofriendly" cols="30" rows="6" bind:value={inputs.ecofriendly.value}></textarea>
					{/if}

					{#if inputs.privacy.show}
						<label for="privacy">Avis de confidentialité</label>
						<textarea id="privacy" cols="30" rows="6" bind:value={inputs.privacy.value}></textarea>
					{/if}

				</form>

			</div>
		</div>
		<div id="preview">

			<div>
				<h2>Aperçu</h2>

				<!-- Prévisualisation -->
				<table cellpadding="0" cellspacing="0" style="vertical-align: -webkit-baseline-middle; font-size: medium; font-family: Arial;">
					<tbody>
					<tr>
						<td>
						<table cellpadding="0" cellspacing="0" style="vertical-align: -webkit-baseline-middle; font-size: medium; font-family: Arial;">
							<tbody>
							<tr>
								<td style="vertical-align: top;">
								<table cellpadding="0" cellspacing="0" style="vertical-align: -webkit-baseline-middle; font-size: medium; font-family: Arial;">
									<tbody>
										{#if inputs.photo.value}
											<tr>
												<td style="text-align: center;">
												<img src="{inputs.photo.value}" alt="Photographie" width="140" style="display: block; max-width: 140px;">
												</td>
											</tr>
											<tr>
												<td height="20"></td>
											</tr>
										{/if}
										{#if inputs.logo.value}
											<tr>
												<td style="text-align: center;">
												<img src="{inputs.logo.value}" alt="Logo" width="140" style="display: block; max-width: 140px;">
												</td>
											</tr>
											<tr>
												<td height="20"></td>
											</tr>
										{/if}
										<tr>
											<td style="text-align: center;">
											<table cellpadding="0" cellspacing="0" style="display: inline-block; vertical-align: -webkit-baseline-middle; font-size: medium; font-family: Arial;">
												<tbody>
												<tr style="text-align: center;">
													{#if inputs.facebook.value}
														<td>
															<a href="{inputs.facebook.value}" color="{color}" style="display: inline-block; padding: 0px; background-color: {color};">
																<img src="https://cdn2.hubspot.net/hubfs/53/tools/email-signature-generator/icons/facebook-icon-2x.png" alt="facebook" color="{color}" height="24" style="background-color: {color}; max-width: 135px; display: block;">
															</a>
														</td>
														<td width="5">
															<div></div>
														</td>
													{/if}
													{#if inputs.twitter.value}
														<td>
															<a href="{inputs.twitter.value}" color="{color}" style="display: inline-block; padding: 0px; background-color: {color};">
																<img src="https://cdn2.hubspot.net/hubfs/53/tools/email-signature-generator/icons/twitter-icon-2x.png" alt="twitter" color="{color}" height="24" style="background-color: {color}; max-width: 135px; display: block;">
															</a>
														</td>
														<td width="5">
															<div></div>
														</td>
													{/if}
													{#if inputs.linkedin.value}
														<td>
															<a href="{inputs.linkedin.value}" color="{color}" style="display: inline-block; padding: 0px; background-color: {color};">
																<img src="https://cdn2.hubspot.net/hubfs/53/tools/email-signature-generator/icons/linkedin-icon-2x.png" alt="linkedin" color="{color}" height="24" style="background-color: {color}; max-width: 135px; display: block;">
															</a>
														</td>
														<td width="5">
															<div></div>
														</td>
													{/if}
													{#if inputs.instagram.value}
														<td>
															<a href="{inputs.instagram.value}" color="{color}" style="display: inline-block; padding: 0px; background-color: {color};">
																<img src="https://cdn2.hubspot.net/hubfs/53/tools/email-signature-generator/icons/instagram-icon-2x.png" alt="instagram" color="{color}" height="24" style="background-color: {color}; max-width: 135px; display: block;">
															</a>
														</td>
														<td width="5">
															<div></div>
														</td>
													{/if}
													{#if inputs.youtube.value}
														<td>
															<a href="{inputs.youtube.value}" color="{color}" style="display: inline-block; padding: 0px; background-color: {color};">
																<img src="https://cdn2.hubspot.net/hubfs/53/tools/email-signature-generator/icons/instagram-icon-2x.png" alt="instagram" color="{color}" height="24" style="background-color: {color}; max-width: 135px; display: block;">
															</a>
														</td>
													{/if}
												</tr>
												</tbody>
											</table>
											</td>
										</tr>
										</tbody>
									</table>
									</td>
									<td width="30">
									<div></div>
									</td>
									<td style="padding: 0px; vertical-align: middle;">
									<h2 color="#000000" style="margin: 0px; font-size: 18px; color: rgb(0, 0, 0); font-weight: 600;">
										<span>{(inputs.fullname.value)?inputs.fullname.value:'John Doe'}</span>
									</h2>
									{#if inputs.title.value}
										<p color="#000000" font-size="medium" style="margin: 0px; color: rgb(0, 0, 0); font-size: 14px; line-height: 22px;">
											<span>{inputs.title.value}</span>
										</p>
									{/if}
									{#if inputs.department.value || inputs.company.value}
										<p color="#000000" font-size="medium" style="margin: 0px; font-weight: 500; color: rgb(0, 0, 0); font-size: 14px; line-height: 22px;">
											{#if inputs.department.value}<span>{inputs.department.value}</span>{/if}
											{#if inputs.department.value && inputs.company.value}
												<span>&nbsp;|&nbsp;</span>
											{/if}
											{#if inputs.company.value}<span>{inputs.company.value}</span>{/if}
										</p>
									{/if}
									<table cellpadding="0" cellspacing="0" style="width: 100%; vertical-align: -webkit-baseline-middle; font-size: medium; font-family: Arial;">
										<tbody>
										<tr>
											<td height="20"></td>
										</tr>
										</tbody>
									</table>
									<table cellpadding="0" cellspacing="0" style="vertical-align: -webkit-baseline-middle; font-size: medium; font-family: Arial;">
										<tbody>
											{#if inputs.phone.value}
												<tr height="25" style="vertical-align: middle;">
													<td width="30" style="vertical-align: middle;">
														<table cellpadding="0" cellspacing="0" style="vertical-align: -webkit-baseline-middle; font-size: medium; font-family: Arial;">
															<tbody>
															<tr>
																<td style="vertical-align: bottom;">
																	<span color="{color}" width="11" style="display: inline-block; background-color: {color};">
																		<img src="https://cdn2.hubspot.net/hubfs/53/tools/email-signature-generator/icons/phone-icon-2x.png" color="{color}" alt="mobilePhone" width="13" style="display: block; background-color: {color};">
																	</span>
																</td>
															</tr>
															</tbody>
														</table>
													</td>
													<td style="padding: 0px; color: rgb(0, 0, 0);">
														<a href="tel:0123456789" color="#000000" style="text-decoration: none; color: rgb(0, 0, 0); font-size: 12px;">
															<span>{inputs.phone.value}</span>
														</a>
													</td>
												</tr>
											{/if}
											{#if inputs.mobile.value}
												<tr height="25" style="vertical-align: middle;">
													<td width="30" style="vertical-align: middle;">
														<table cellpadding="0" cellspacing="0" style="vertical-align: -webkit-baseline-middle; font-size: medium; font-family: Arial;">
															<tbody>
																<tr>
																	<td style="vertical-align: bottom;">
																		<span color="{color}" width="11" style="display: inline-block; background-color: {color};">
																			<img src="https://cdn2.hubspot.net/hubfs/53/tools/email-signature-generator/icons/phone-icon-2x.png" color="{color}" alt="mobilePhone" width="13" style="display: block; background-color: {color};">
																		</span>
																	</td>
																</tr>
															</tbody>
														</table>
													</td>
													<td style="padding: 0px; color: rgb(0, 0, 0);">
														<a href="tel:0123456789" color="#000000" style="text-decoration: none; color: rgb(0, 0, 0); font-size: 12px;">
															<span>{inputs.mobile.value}</span>
														</a>
													</td>
												</tr>
											{/if}
											{#if inputs.email.value}
												<tr height="25" style="vertical-align: middle;">
													<td width="30" style="vertical-align: middle;">
														<table cellpadding="0" cellspacing="0" style="vertical-align: -webkit-baseline-middle; font-size: medium; font-family: Arial;">
															<tbody>
															<tr>
																<td style="vertical-align: bottom;">
																<span color="{color}" width="11" style="display: inline-block; background-color: {color};">
																	<img src="https://cdn2.hubspot.net/hubfs/53/tools/email-signature-generator/icons/email-icon-2x.png" color="{color}" alt="emailAddress" width="13" style="display: block; background-color: {color};">
																</span>
																</td>
															</tr>
															</tbody>
														</table>
													</td>
													<td style="padding: 0px;">
														<a href="mailto:{inputs.email.value}" color="#000000" style="text-decoration: none; color: rgb(0, 0, 0); font-size: 12px;">
															<span>{inputs.email.value}</span>
														</a>
													</td>
												</tr>
											{/if}
											{#if inputs.website.value}
												<tr height="25" style="vertical-align: middle;">
													<td width="30" style="vertical-align: middle;">
													<table cellpadding="0" cellspacing="0" style="vertical-align: -webkit-baseline-middle; font-size: medium; font-family: Arial;">
														<tbody>
														<tr>
															<td style="vertical-align: bottom;">
															<span color="{color}" width="11" style="display: inline-block; background-color: {color};">
																<img src="https://cdn2.hubspot.net/hubfs/53/tools/email-signature-generator/icons/link-icon-2x.png" color="{color}" alt="website" width="13" style="display: block; background-color: {color};">
															</span>
															</td>
														</tr>
														</tbody>
													</table>
													</td>
													<td style="padding: 0px;">
													<a href="//{inputs.website.value}" color="#000000" style="text-decoration: none; color: rgb(0, 0, 0); font-size: 12px;">
														<span>{inputs.website.value}</span>
													</a>
													</td>
												</tr>
											{/if}
											{#if inputs.addressline1.value || inputs.addressline2.value || inputs.addressline3.value || addressline4}
												<tr height="25" style="vertical-align: top;">
													<td width="30" style="vertical-align: top;">
														<table cellpadding="0" cellspacing="0" style="vertical-align: -webkit-baseline-middle; font-size: medium; font-family: Arial;">
															<tbody>
															<tr>
																<td style="vertical-align: bottom;">
																<span color="{color}" width="11" style="display: inline-block; background-color: {color};">
																	<img src="https://cdn2.hubspot.net/hubfs/53/tools/email-signature-generator/icons/address-icon-2x.png" color="{color}" alt="address" width="13" style="display: block; background-color: {color};">
																</span>
																</td>
															</tr>
															</tbody>
														</table>
													</td>
													<td style="padding: 0px;">
														<span color="#000000" style="font-size: 12px; color: rgb(0, 0, 0);">
															<span>
																{#if inputs.addressline1.value}{inputs.addressline1.value}<br />{/if}
																{#if inputs.addressline2.value}{inputs.addressline2.value}<br />{/if}
																{#if inputs.addressline3.value}{inputs.addressline3.value}<br />{/if}
																{(addressline4)?addressline4:''}
															</span>
														</span>
													</td>
												</tr>
											{/if}
										</tbody>
									</table>
									<table cellpadding="0" cellspacing="0" style="vertical-align: -webkit-baseline-middle; font-size: medium; font-family: Arial;">
										<tbody>
										<tr>
											<td height="20"></td>
										</tr>
										</tbody>
									</table>
									</td>
								</tr>
								</tbody>
							</table>
							</td>
						</tr>
						{#if inputs.bannerimg.value}
							<tr>
								<td>
								<table cellpadding="0" cellspacing="0" style="vertical-align: -webkit-baseline-middle; font-size: medium; font-family: Arial;">
									<tbody>
										<tr>
											<td height="20"></td>
										</tr>
										<tr>
											<span style="display: block; text-align: left;">
												{#if inputs.bannerurl.value}
												<a target="_blank" rel="noopener noreferrer" href="{inputs.bannerurl.value}" style="border-width: initial; border-style: none; border-color: initial; display: inline-block; background-color: transparent; color: rgb(255, 255, 255); font-weight: 700; text-decoration: none; text-align: center; line-height: 1; font-size: 12px; border-radius: 3px;">
													<img src="{inputs.bannerimg.value}" alt="Bannière" style="text-decoration: none; max-width:400px;">
												</a>
												{:else}
													<img src="{inputs.bannerimg.value}" alt="Bannière" style="text-decoration: none; max-width: 400px;">
												{/if}
											</span>
										</tr>
									</tbody>
								</table>
								</td>
							</tr>
						{/if}
						{#if inputs.ecofriendly.value}
							<tr>
								<td>
									<table width="600" cellpadding="0" cellspacing="0" style="vertical-align: -webkit-baseline-middle; font-size: small; font-family: Arial;">
										<tbody>
											<tr>
												<td height="20"></td>
											</tr>
											<tr height="25" style="vertical-align: top;">
												<td width="20" style="vertical-align: top;">
													<table cellpadding="0" cellspacing="0" style="vertical-align: -webkit-baseline-middle; font-size: medium; font-family: Arial;">
														<tbody>
														<tr>
															<td style="vertical-align: bottom;">
															<span color="{color}" width="14" style="display: inline-block; background-color: {color};">
																<img src="https://cdn2.hubspot.net/hubfs/53/tools/email-signature-generator/icons/address-icon-2x.png" color="{color}" alt="address" width="14" style="display: block; background-color: {color};">
															</span>
															</td>
														</tr>
														</tbody>
													</table>
												</td>
												<td style="padding: 0px;">
													<span color="#27ae60" style="font-size: 12px; line-height: 16px; color: #27ae60;">
														<span>
															{inputs.ecofriendly.value}
														</span>
													</span>
												</td>
											</tr>
										</tbody>
									</table>
								</td>
							</tr>
						{/if}
						{#if inputs.privacy.value}
							<tr>
								<td>
									<table width="600" cellpadding="0" cellspacing="0" style="vertical-align: -webkit-baseline-middle; font-size: small; font-family: Arial;">
										<tbody>
											<tr>
												<td height="20"></td>
											</tr>
											<tr height="25" style="vertical-align: top;">
												<td style="padding: 0px;">
													<span color="#999" style="font-size: 12px; line-height: 16px; color: #999;">
														<span>
															{inputs.privacy.value}
														</span>
													</span>
												</td>
											</tr>
										</tbody>
									</table>
								</td>
							</tr>
						{/if}
					</tbody>
				</table>
			</div>
		</div>
	</div>
</main>

<style>

	* {
		box-sizing: border-box;
		font-family: Arial, sans-serif;
	}

	h1, h2 {
		font-size: 1.5rem;
	}

	h4 {
		font-size: 1.25rem;
	}

	h1, h2, h4 {
		line-height: 1.2;
		margin: 0 0 1rem;
	}

	h4 {
		margin: 1rem 0;
	}

	#sidebar, input, textarea {
		font-family: Arial;
		font-size: 16px;
		line-height: 1.4rem;
	}

	label {
		font-size: .9rem;
		display: block;
		font-weight: 600;
		margin-bottom: .25rem;
		margin-top: .75rem;
	}

	input[type="text"], input[type="url"], input[type="email"], textarea {
		border: 1px solid #bdc3c7;
		padding: .5rem .75rem;
		border-radius: 0 .25rem .25rem 0;
		width: 100%;
		position: relative;
		border-left: 0;
	}

	textarea {
		border: 1px solid #bdc3c7;
		border-radius: .25rem;
	}

	.input {
		display: flex;
	}

	.input:before {
		content: '';
		display: block;
		width: auto;
		height: calc(2.5rem + 2px);
		aspect-ratio: 1/1;
		border-radius: .25rem 0 0 .25rem;
		background-color: #bdc3c7;
		background-size: 1rem;
		background-repeat: no-repeat;
		background-position: center;
	}

	.input.text:before {
		background-image: url('../public/text.svg');
	}

	.input.url:before {
		background-image: url('../public/url.svg');
	}

	.input.phone:before {
		background-image: url('../public/phone.svg');
	}

	.input.email:before {
		background-image: url('../public/email.svg');
	}

	textarea {
		min-height: 6rem;
		max-height: 15rem;
	}

	#wrapper {
		max-width: 80rem;
		margin: 1rem auto;
		display: flex;
		gap: 1rem;
		padding: 0 1rem;
	}

	#sidebar {
		width: 350px;
	}

	#sidebar > div {
		background: #ecf0f1;
		border-radius: .25rem;
		padding: 1rem;
	}

	#preview {
		width: calc(100% - 350px - 1rem);
		padding: 1rem;
	}

	#preview > div {
		position: sticky;
		top: 1rem;
	}

</style>
