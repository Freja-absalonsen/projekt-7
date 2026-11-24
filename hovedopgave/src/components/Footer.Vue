<template>
    <footer class="footer">
        <div class="footer__content">
            <!-- Kolonne 1: Kontakt -->
            <section class="footer__column" aria-labelledby="footer-contact-heading">
                <h2 id="footer-contact-heading" class="footer__heading">Broby<br>Sportsefterskole</h2>

                <ul class="footer__contact">
                    <li class="footer__contact-item">
                        <img class="footer__icon" src="../assets/Icon/Pin.svg" alt="Pin ikon" width="20" height="20">
                        <a 
                            class="footer__contact-text footer__contact-text-link" 
                            href="https://www.google.com/maps/place/Broby+Sportsefterskole/@55.2503472,10.2209578,17z/data=!3m1!4b1!4m6!3m5!1s0x464cd9e533741701:0x2faf67eaaf784d76!8m2!3d55.2503472!4d10.2209578!16s%2Fg%2F1thq8gf2?entry=ttu&g_ep=EgoyMDI2MTEyMi4wIKXMDSoASAFQAw%3D%3D"
                            target="_blank"
                            rel="noopener noreferrer"
                            aria-label="Find Vesterågade 60, 5672 Broby på Google Maps (åbner i nyt vindue)"
                        >
                            <address class="footer__contact-text">Vesterågade 60<br>5672 Broby</address>
                        </a>
                    </li>
                    <li class="footer__contact-item">
                        <img class="footer__icon" src="../assets/Icon/Mail.svg" alt="Mail icon" width="20" height="20">
                        <a class="footer__contact-text footer__contact-text-link" href="mailto:info@brobysportsefterskole.dk" aria-label="Send en e-mail til info@brobysportsefterskole.dk">info@brobysportsefterskole.dk</a>
                    </li>
                    <li class="footer__contact-item">
                        <img class="footer__icon" src="../assets/Icon/Mobil.svg" alt="Telefon icon" width="20" height="20">
                        <a class="footer__contact-text footer__contact-text-link" href="tel:+4562631458" aria-label="Ring til +45 62 63 14 58">+45 62 63 14 58</a>
                    </li>
                </ul>

                <ul class="footer__socials" aria-label="Sociale medier">
                    <li class="footer__socials-item">
                        <a class="footer__social-link" href="https://www.facebook.com/Broby.Sportsefterskole" target="_blank" rel="noopener noreferrer" aria-label="Broby Sportsefterskole på Facebook (åbner i nyt vindue)">
                            <img class="footer__social-icon" src="../assets/Icon/Facebook.svg" alt="Facebook icon" width="16" height="16">
                        </a>
                    </li>
                    <li class="footer__socials-item">
                        <a class="footer__social-link" href="https://www.youtube.com/user/BrobyVideo" target="_blank" rel="noopener noreferrer" aria-label="Broby Sportsefterskole på Youtube (åbner i nyt vindue)">
                            <img class="footer__social-icon" src="../assets/Icon/Youtube.svg" alt="Youtube icon" width="16" height="16">
                        </a>
                    </li>
                    <li class="footer__socials-item">
                        <a class="footer__social-link" href="https://www.instagram.com/BrobySportsefterskole" target="_blank" rel="noopener noreferrer" aria-label="Broby Sportsefterskole på Instagram (åbner i nyt vindue)">
                            <img class="footer__social-icon" src="../assets/Icon/Instagram.svg" alt="Instagram icon" width="16" height="16">
                        </a>
                    </li>
                    <li class="footer__socials-item">
                        <a class="footer__social-link" href="https://www.tiktok.com/@brobysportsefterskole" target="_blank" rel="noopener noreferrer" aria-label="Broby Sportsefterskole på Tiktok (åbner i nyt vindue)">
                            <img class="footer__social-icon" src="../assets/Icon/TikTok.svg" alt="Tiktok icon" width="16" height="16">
                        </a>
                    </li>
                </ul>
            </section>

            <!-- Kolonne 2: links -->
            <nav class="footer__column" aria-labelledby="footer-link-heading">
                <h2 id="footer-link-heading" class="footer__heading">Link</h2>
                <ul class="footer__links">
                    <li class="footer__links-item"><RouterLink class="footer__link" active-class="footer__link--active" :to="{name:'Om skolen'}">Om skolen</RouterLink></li>
                    <li class="footer__links-item"><RouterLink class="footer__link" active-class="footer__link--active" :to="{name:'Presse'}">Presse</RouterLink></li>
                    <li class="footer__links-item"><RouterLink class="footer__link" active-class="footer__link--active" :to="{name:'Gamle elever'}">Gamle elever</RouterLink></li>
                    <li class="footer__links-item"><RouterLink class="footer__link" active-class="footer__link--active" :to="{name:'Livet på Broby'}">Livet på Broby</RouterLink></li>
                    <li class="footer__links-item"><RouterLink class="footer__link" active-class="footer__link--active" :to="{name:'Sportsfag'}">Sportsfag</RouterLink></li>
                    <li class="footer__links-item"><RouterLink class="footer__link" active-class="footer__link--active" :to="{name:'Ny elev'}">Ny elev</RouterLink></li>
                    <li class="footer__links-item"><RouterLink class="footer__link" active-class="footer__link--active" :to="{name:'Kontakt'}">Kontakt</RouterLink></li>
                    <li class="footer__links-item"><RouterLink class="footer__link" active-class="footer__link--active" :to="{name:'Infoskærme'}">Infoskærme</RouterLink></li>
                    <li class="footer__links-item"><RouterLink class="footer__link" active-class="footer__link--active" :to="{name:'Handelsbetingelser'}">Handelsbetingelser</RouterLink></li>
                    <li class="footer__links-item">
                        <a class="footer__link footer__link--external" href="https://broby.viggo.dk/Basic/Account/Login?returnUrl=%2F" target="_blank" rel="noopener noreferrer" aria-label="Gå til Viggo (åbner i nyt vindue)">Gå til Viggo</a>
                    </li>
                </ul>
            </nav>

            <!-- Kolonne 3: Om skolen -->
            <section class="footer__column footer__column--about" aria-labelledby="footer-about-heading">
                <RouterLink class="footer__logo" :to="{name: 'home'}" aria-label="Broby Sportsefterskole - gå til forside">
                    <img class="footer__logo-image" src="../assets/logo.png" alt="Broby Sportsefterskole logo" height="100" width="auto">
                </RouterLink>

                <h3 id="footer-about-heading" class="footer__title">Efterskolen med muligheder</h3>
                <p class="footer__text">Vi vil være en efterskole, der giver dig rigtig mange muligheder for at vælge mellem vores mange valgfag. Du har mulighed for at vælge mindst tre forskellige valgfag om ugen.
                    <RouterLink class="footer__text-link" :to="{name:''}">fodbold</RouterLink>, <RouterLink class="footer__text-link" :to="{name:''}">Spring</RouterLink>, <RouterLink class="footer__text-link" :to="{name:''}">pigefodbold</RouterLink>, <RouterLink class="footer__text-link" :to="{name:''}">badminton</RouterLink>,
                    <RouterLink class="footer__text-link" :to="{name:''}">beachvolley</RouterLink>, <RouterLink class="footer__text-link" :to="{name:''}">dans</RouterLink>, <RouterLink class="footer__text-link" :to="{name:''}">madlavning</RouterLink>, <RouterLink class="footer__text-link" :to="{name:''}">fitness</RouterLink>,
                    <RouterLink class="footer__text-link" :to="{name:''}">håndbold</RouterLink>, <RouterLink class="footer__text-link" :to="{name:''}">løb</RouterLink>, <RouterLink class="footer__text-link" :to="{name:''}">kajak</RouterLink>, <RouterLink class="footer__text-link" :to="{name:''}">surf og kite</RouterLink>,
                    <RouterLink class="footer__text-link" :to="{name:''}">mountainbike</RouterLink>, <RouterLink class="footer__text-link" :to="{name:''}">musik</RouterLink>, <RouterLink class="footer__text-link" :to="{name:''}">crossfit</RouterLink>, <RouterLink class="footer__text-link" :to="{name:''}">spinning</RouterLink>,
                    <RouterLink class="footer__text-link" :to="{name:''}">styrketræning</RouterLink> og <RouterLink class="footer__text-link" :to="{name:''}">svømning</RouterLink>.
                </p>
                <p class="footer__text">Er du sporty og vil have mange valg, så er Broby Sportsefterskole lige dig.</p>
                <img class="footer__script" src="../assets/" alt="Vi ses på Broby">
            </section>
        </div>

        <div class="footer__bottom">
            <p class="footer__copyright">Copyright © Broby sportsefterskole | Designet af 
                <a class="footer__copyright-link" href="https://www.odensemediedesign.dk/" target="_blank" rel="noopener noreferrer" aria-label="Odense Media Design (åbner i nyt vindue)">Odense Medie Design</a>
            </p>
            <img class="footer__payments" src="../assets/" alt="Vi modtager Dankort, Visa, Mastercard og Maestro">

        </div>

    </footer>
</template>