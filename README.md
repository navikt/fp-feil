![](https://github.com/navikt/fp-feil/workflows/Build/badge.svg) 
[![Sonarcloud Status](https://sonarcloud.io/api/project_badges/measure?project=navikt_fp-feil&metric=alert_status)](https://sonarcloud.io/dashboard?id=navikt_fp-feil) 
[![SonarCloud Bugs](https://sonarcloud.io/api/project_badges/measure?project=navikt_fp-feil&metric=bugs)](https://sonarcloud.io/component_measures/metric/reliability_rating/list?id=navikt_fp-feil)
[![SonarCloud Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=navikt_fp-feil&metric=vulnerabilities)](https://sonarcloud.io/component_measures/metric/security_rating/list?id=navikt_fp-feil)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/navikt/fp-feil)
![GitHub](https://img.shields.io/github/license/navikt/fp-feil)

# fp-feil 

Denne pakken inneholder felles Exception for å håndtere feilmeldinger og feilkoder som logges i løsningene til foreldrepenger.

Feilkoder som logges er unike og stabile og kan benyttes i dokumentasjon (f.eks. i forbindelse med troubleshooting av systemet).

Exceptions som applikasjonen selv kaster er subklasser av en av 4 typer:
<ul>
<li><b>FunksjonellException</b> - Denne presenteres bruker, men logges normalt ikke</li>
<li><b>TekniskException</b> - logges alltid, som WARN eller ERROR. Bruker får en feilmelding sammen med en CallId som kanbenyttes til å søke opp feilmelding i logger</li>
<li><b>IntegrasjonException</b> - en spesiell TekniskException knyttet til kall mot andre tjenester</li>
<li><b>ManglerTilgangException</b> - en spesiell Exception knyttet til tilgangsstyring.</li>
</ul>

### Lisens
MIT
