+++
title = "Identity and Access Management Overview"
+++

<!-- Slide TITLE -->
<!--: .wrap .text-landing bg=bg-black bg=aligncenter bgimage=https://images.unsplash.com/photo-1614064641938-3bbee52942c7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1950&q=80 -->

{{< div class="content-center" >}}
# **IAM Overview**  
[{{% fontawesome github %}} Github](https://github.com/20100701/infra)
{{< /div >}}

---
<!-- Slide ABOUT -->
{{< div class="content-left" >}}

#### Avant-propos
<small>
*Ce contenu a pour objectif de faire découvrir les concepts de l'*Identity and Access Management*. Certains aspects sont simplifiés dans le but de rester compréhensible par un public voulant appréhender ce sujet sans en devenir des experts.*
</small>

#### Contexte
<small>
Ce contenu a été créé pour les étudiants de la licence <a href="https://uniform.unicaen.fr/catalogue/formation/licences-pro/5236-licence-pro-metiers-informatique---administration-securite-systemes-et-reseaux-parcours-audit-securite-reseaux-sys-info?s=iut-caen&r=1291046129051">Audit et Sécurité des Réseaux et des Systèmes d'Information</a> (aka ASRSI) de l'<a href="http://www.unicaen.fr/">Université de Caen</a>.
</small>

#### Objectif
<small>
Ce contenu doit permettre aux étudiants d'appréhender les concepts de l'*Identity and Access Management* ainsi que les solutions techniques misent en œuvre.<br>
Il sert donc de support pour un module d'enseignement de l'*Identity and Access Management* aussi bien pour les parties théoriques que pratiques. Il limite au maximum le temps passé sur la phase de déploiement des environnements afin de laissé le plus de temps possible à la compréhension de l'*Identity and Access Management* et aux échanges entre étudiants et formateurs.
</small>
{{< /div >}}


<figure class="content-right">
  <img alt="Screenshot" src="https://images.unsplash.com/photo-1519452635265-7b1fbfd1e4e0?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=934&q=80">
</figure>


---
<!-- Slide 3 -->
<!--: .wrap -->
### **Identity and Access Management**
La gestion des identités et des accès (Identity and Access Management aka **IAM**) est un aspect important de la sécurité en entreprise.<br>
Elle rassemble les processus qui permettent de gérer les identités et les habilitations qui donnent accès aux ressources du système d'information.

Cela englobe l'ensemble du cycle de vie (création, modification, suppression et audit) des informations  liées aux identités numériques et droits d'accès associés.

Opérationnellement, l'ensemble des solutions qui permettent le contrôle et la protection de ces informations sont liées à l'Identity and Access Management.

##### Les 4 composantes de base
Il existe 4 sujets qui doivent être traités pour avoir une gestion homogène de la sécurité dans le cadre de l'IAM.<br>
- **Identité** : gestion du cycle de vie des informations liées aux identités numériques sans prendre en compte les droits et les accès.<br>
- **Authentification** : l'ensemble des moyens permettant de vérifier que la demande d'accès est effectuée par une entité légitime  (humain ou machine) et d'y associer une identité numérique.<br>
- **Autorisation** : Gestion des droits et politiques d'accès aux ressources.<br>
- **Fédération d'identité** : ensemble des processus et mécanismes qui permettent d'échanger de manière sécurisée l'identité d'une entité (humain ou machine).<br>

---
<!-- Slide 4 -->
<!--: .wrap -->
### **Les enjeux de l'IAM**
{{< div class="content-left" >}}
Le déploiement d'un système de gestion IAM est onéreux mais il y a des avantages :<br>
- **financier** : réduction coûts grâce un système spécialisé, dédié<br>
- **sécurité** : gestion centralisée de l'authentification des utilisateurs, qualité des données<br>
- **productivité** : augmente la productivité des utilisateurs, par exemple grâce au mécanisme de Single Sign-On (aka <a href=https://en.wikipedia.org/wiki/Single_sign-on>SSO</a>)<br>
- **souplesse** : permet d'augmenter l'agilité du système d'information, scalabilité<br>
- **conformité** : les logs généres et les règles implémentées peuvent servir comme preuves lors d'audits<br>
<br>
Aujourd'hui toutes les entreprises de ce monde s'intéressent à l'IAM, et c'est encore plus vrai depuis les vagues de cyber-attaques de ces dernières années.
{{< /div >}}

<figure class="content-right">
  <img alt="auth" src="https://images.unsplash.com/photo-1564353779909-9140fd426002?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=944&q=80">
</figure>



---
<!-- Slide 5 -->
<!--: .wrap -->
### **Identité**
{{< div class="content-left" >}}
Une identité est l'ensemble des données qui permettent d'individualiser quelqu'un.<br>
Une personne physique possède **plusieurs identités numériques**.<br>
En effet, en fonction des ressources auxquelles elle veut accéder, l'identité peut varier :<br>
<small>
- un nom de famille<br>
- un identifiant unique<br>
- une adresse mail<br>
- une appartenance à une entité<br>
- un certificat utilisateur (X509)<br>
- ...<br>
</small>

Au sein du système d'information, les **cycles de vie** des identités sont gérés par :<br>
<small>
- une gouvernance<br>
- des processus<br>
- une traçabilité/auditabilité<br>
- des formats<br>
</small>
{{< /div >}}

<figure class="content-right">
  <img alt="auth" src="https://images.unsplash.com/photo-1613243556956-4946e3189a3f?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80">
</figure>

---
<!-- Slide 6 -->
<!--: .wrap -->
### **Authentification**
{{< div class="content-left" >}}
L'authentification dans un système d'information est un processus qui permet à un système de s'assurer qu'une demande d'accès est effectuée par un **utilisateur légitime** (humain ou machine).<br><br>
Au terme de ce processus le système passe à la **phase d'identification**, il associe une identité à l'utilisateur. Cette identité peut-être attribuée par le système ou fournit lors de l'authentification.<br>

Pour authentifier un utilisateur, un système lui demande une ou des **preuves**, elles sont aussi appelées "**facteurs d'authentification**", elles peuvent prendre plusieurs formes :<br>
<small>
- un secret (ex: mot de passe, code PIN)<br>
- un certificat (ex: X509)<br>
- un équipement (ex: smartphone, carte SIM)<br>
- biométrique (ex: empreinte digitale)<br>
- l'accès à une ressource précise (ex: une boîte mail)<br>
- ...<br>
</small>
{{< /div >}}

<figure class="content-right">
  <img alt="auth" src="https://images.unsplash.com/photo-1617704716344-8d987ac681a4?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1567&q=80
">
</figure>

---
<!-- Slide 7 -->
<!--: .wrap -->
### **Autorisation**
{{< div class="content-left" >}}
Elle intervient **après la phase d'authentification**.<br><br>
L'autorisation est le mécanisme qui permet d'autoriser un utilisateur à accéder à une **ressource/information** en fonction des règles de contrôle d'accès.<br><br>
Ces règles sont la déclinaison de la politique d'accès aux ressources/informations de l'entreprise.<br><br>
Il existe plusieurs possibilités pour définir une politique d'accès, les plus courantes sont :<br>
- <a href=https://en.wikipedia.org/wiki/Role-based_access_control>RBAC</a> : Role-Based Access Control<br>
- <a href=https://en.wikipedia.org/wiki/Attribute-based_access_control>ABAC</a> : Attribute-Based Access Control<br>
{{< /div >}}

<figure class="content-right">
  <img alt="AZ" src="https://image.freepik.com/photos-gratuite/out-interdiction-sign_1232-2709.jpg">
</figure>

---
<!-- Slide 8 -->
<!--: .wrap -->
### **Fédération d'identité**
{{< div class="content-left" >}}
Elle est utilisée lorsqu'un utilisateur veut accéder à des ressources gérées par un système de gestion des identités différents du sien.<br>

Les différentes phases sont partagées en fédération d'identité :<br>
<small>
a) l'utilisateur s'authentifie auprès de son système d'IAM qui va lui fournir une **preuve d'identité**<br>
b) l'utilisateur fournit cette **preuve d'identité** au système d'IAM de la ressource à laquelle il veut accéder<br> 
</small>
<br>

La fédération d'identité est basée sur un principe de **confiance** entre le système IAM de l'utilisateur et celui de la ressource à laquelle ce dernier veut accéder. Cette confiance prend souvent à minima la forme d'une **signature cryptographique** de la preuve d'identité.

Techniquement, la fédération d'identité prend la forme de protocole dont les plus utilisés sont :<br>
<small>
- <a href=https://wiki.oasis-open.org/security/FrontPage#SAML_V2.0_Standard>SAML 2.0</a><br>
- <a href=https://openid.net/connect/>OpenID</a> / <a href=https://oauth.net/2/>OAuth 2.0</a><br>
</small>

Le protocole SAML 2.0 est fait pour répondre aux cas d'usage B2B. Contrairement au couple OIDC/Oauth 2.0 qui se retrouve dans des cas d'usage grand public, mais aussi B2B. En fonction du contexte, il est intéressant d'utiliser l'un ou l'autre de ces protocoles.<br>
{{< /div >}}

<figure class="content-right">
  <img alt="fed" src="https://images.unsplash.com/photo-1607000975509-de2f74eb8d36?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1567&q=80">
</figure>

---
<!-- Slide 9-->
<!--: .wrap -->
### **Exemples de solutions techniques**
Les acteurs commerciaux ou open source couvrent souvent plusieurs aspects de l'IAM.<br>

Le Gartner fournit une liste (non exhaustive) des solutions commerciales de gestion des identités consultable <a href=https://www.gartner.com/reviews/market/identity-governance-administration>ici</a> et une liste (non exhaustive) des solutions de gestion des accès consultable <a href=https://www.gartner.com/reviews/market/access-management/>là</a>.<br>

Il existe de plus en plus de solution open source :<br>
- <a href=https://www.keycloak.org/>Keycloak</a><br>
- <a href=https://www.univention.com/>Univention Corporate Server</a><br>
- <a href=https://syncope.apache.org/>Apache Syncope</a><br>
- <a href=https://www.gluu.org/>Gluu</a><br>
- <a href=http://directory.apache.org/fortress/>Apache Fortress</a><br>
- ...

---
<!-- Slide 10 -->
<!--: .wrap -->
### **Focus : contrôle d'accès**

{{< div class="content-left" >}}
#### Qu'est-ce qu'un contrôle d'accès ?
Les contrôles d'accès sont des éléments de sécurité du SI.<br>
Ils doivent donc posséder les caractéristiques suivantes :<br>
<small>
- assurer la confidentialité des flux/informations qu'ils traitent<br>
- assurer l'intégrité des flux/informations qu'ils traitent<br>
- être disponible afin que les ressources qu'ils protègent soient accessibles<br>
</small>

#### Qu'est-ce qu'un contrôle d'accès HTTP ?
Un contrôle d'accès HTTP permet de donner l'accès à une ressource HTTP uniquement aux utilisateurs (humain ou machine) légitimes.<br>
Il porte les fonctions de :<br>
<small>
- authentification<br>
- identification<br>
- autorisation<br>
</small>

#### Qu'est-ce qu'un contrôle d'accès HTTP mutualisé ?
La mise en oeuvre de ce type de service est souvent onéreuse car il y a plusieurs aspects qui doivent être pris en compte :<br>
<small>
- la mise en oeuvre de la solution technique<br>
- le maintien en condition opérationnelle (MCO) de cette solution technique<br>
- la mise en place d'outils et de processus liés au cycle de vie des identités et des droits<br>
- les outils et processus de traçabilité et d'auditabilité<br>
</small>

Il est donc intéressant de mutualiser cette fonction pour limiter les coûts et centraliser les problématiques liées à l'IAM.<br>
{{< /div >}}

<figure class="content-right">
  <img alt="ctrlaccess" src="https://image.freepik.com/vecteurs-libre/camera-surveillance-fond-realiste_1284-24308.jpg">
</figure>

<small> *note : les contrôles d'accès ne sont pas un besoin lié au cœur de métier des entreprises, il est donc fréquent de les classer dans les services d'infrastructure. Car ils fournissent un service essentiel au fonctionnement des SI au même titre que le NTP, le DNS, les proxies, ...* </small>

---
<!-- Slide 11 -->
<!--: .wrap bg=bg-white -->

<figure class="content-center">
  <img alt="ctrlaccess" src="https://20100701.github.io/infra/static/images/saml-2.0.png">
</figure>

---
<!-- Slide 12 -->
<!--: .wrap -->
### **Security Assertion Markup Language**
<a href=https://www.oasis-open.org/standards#samlv2.0>SAML</a> est un protocole de fédération d'identité standardisé par l'<a href=https://www.oasis-open.org>OASIS</a>. Il est principalement utilisé dans sa version 2.0 qui a été finalisée en 2012.
Le nombre des composants en jeu et les échanges entre ces derniers font de SAML un protocole simple à appréhender. Il a permis de simplifier la mise en œuvre de la fédération d'identité, pour comprendre pourquoi un Executive Overview est disponible <a href=https://www.oasis-open.org/committees/download.php/13525/sstc-saml-exec-overview-2.0-cd-01-2col.pdf>ici</a>.

Dans la suite du document sont brièvement expliquer les concepts à l'oeuvre dans SAML. Pour aller plus loin dans la compréhension du protocole il est conseillé de se référer au Technical Overview (disponible <a href=https://www.oasis-open.org/committees/download.php/27819/sstc-saml-tech-overview-2.0-cd-02.pdf>ici</a>) ou bien aux <a href=http://saml.xml.org/saml-specifications>spécifications SAML</a>.

#### Les composants : IDP et SP
Le protocole définit 2 composants :<br> 
- Identity Provider aka **IDP**<br>
- Service Provider aka **SP**<br>

**L'Identity Provider**<br>
L'IDP est le composant qui est en charge de générer la **preuve d'identité** conformément au **contrat d'interface** prédéfinit avec le SP. Il porte également la responsabilité de la phase d'authentification de l'utilisateur.

**Le Service Provider**<br>
Ce composant consomme la **preuve d'identité** générée par l'IDP, il vérifie l'intégrité de la preuve et y récupère l'**identité** de l'utilisateur ainsi que toutes autres informations transmises dans la "preuve d'identité" qui lui sont nécessaires.

---
<!-- Slide 13 -->
<!--: .wrap -->
{{< div class="content-left" >}}
#### Le contrat d'interface : partenariat
Le contrat d'interface définit entre l'IDP et le SP est appelé **partenariat**.<br>
Il sert à définir les informations relatives à l'utilisateur qui seront transmises dans chaque preuve d'identité et leurs formats.<br>
Il contient à minima les informations relatives à la sécurité (ex : algorithmes de chiffrement et de signature à utiliser), il prend la forme de "<a href=http://docs.oasis-open.org/security/saml/v2.0/saml-metadata-2.0-os.pdf>**metadata**</a>".

#### La preuve d'identité : assertion
Le protocole SAML appelle "<a href=http://docs.oasis-open.org/security/saml/v2.0/saml-core-2.0-os.pdf>**assertion**</a>" la preuve d'identité.<br>
Elle est générée par l'IDP et contient les informations relatives à l'utilisateur dans les formats définis dans le partenariat.<br>
Elle peut aussi contenir des informations complémentaires.
{{< /div >}}

{{< div class="content-right" >}}
<small>L'image ci-dessous représente un exemple d'assertion SAML 2.0 (*source : oasis-open.org*).</small><br>
![assertion](http://docs.oasis-open.org/security/saml/Post2.0/sstc-saml-tech-overview-2.0-cd-02_html_m928aca6.gif)

{{< /div >}}

---
<!-- Slide 14 -->
<!--: .wrap -->
### **Les cas d'usage**
{{< div class="content-left" >}}
Nous allons uniquement nous concentrer sur 2 cas d'usage SAML 2.0 :<br>
- <a href="http://docs.oasis-open.org/security/saml/Post2.0/sstc-saml-tech-overview-2.0-cd-02.html#5.1.4.IdP-Initiated SSO:  POST Binding|outline">IDP initiated SSO : Post binding</a><br>
- <a href="http://docs.oasis-open.org/security/saml/Post2.0/sstc-saml-tech-overview-2.0-cd-02.html#5.1.2.SP-Initiated SSO:  Redirect/POST Bindings|outline">SP initiated SSO : Redirect/Post bindings</a><br>
<br>
Il existe d'autres cas d'usage disponibles (ex : *just in time provisioning*) avec SAML 2.0, mais à ma connaissance ils sont peu utilisés.<br>
Mais ils peuvent être intéressant dans certains contextes.
{{< /div >}}

<figure class="content-right">
  <img alt="uc-saml" src="https://images.unsplash.com/photo-1516981879613-9f5da904015f?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1567&q=80">
</figure>

---
<!-- Slide 15 -->
<!--: .wrap -->
### **IDP initiated SSO : Post binding**
Ce cas d'usage est le plus simple d'un point de vue protocolaire. L'utilisateur appelle en première intention une ressource de son IDP en passant en paramètre un identifiant correspondant au SP qu'il veut atteindre.
L'IDP va demander à l'utilisateur de s'authentifier afin de générer une assertion contenant l'identité de l'utilisateur et conforme au partenariat définit avec le SP demandé.
Une fois l'assertion générée, l'IDP va transmettre l'assertion à l'utilisateur et le redirige vers le SP demandé.

### IDP Initiated (simplifié)

<!--: .flexblock gallery -->
- {{< gallery title="idpinit" href="https://20100701.github.io/infra/static/images/idp-init.png" src="https://20100701.github.io/infra/static/images/idp-init.png" >}}{{< /gallery >}}

---
<!-- Slide 16 -->
<!--: .wrap -->
### **SP initiated SSO : Redirect/Post bindings**
Dans ce cas d'usage, l'utilisateur appelle en première intention un SP. Comme l'utilisateur ne posséde pas d'assertion, le SP le redirige vers son IDP qui va l'authentifier, générer l'assertion et le rediriger vers le SP.
Il est à noter que le SP fournit une information dans la requête de redirection qui permettra à l'IDP de rediriger l'utilisateur vers le SP demandé initialement. Le schéma ci-dessous représente une vue fonctionnelle simplifiée des échanges entre les différents acteurs.

<!--: .flexblock gallery -->
- {{< gallery title="sppinit" href="https://20100701.github.io/infra/static/images/sp-init.png" src="https://20100701.github.io/infra/static/images/sp-init.png" >}}{{< /gallery >}}

---
<!-- Slide 17 -->
<!--: .wrap .text-landing bg=bg-white bg=aligncenter bgimage=https://openid.net/wordpress-content/uploads/2011/09/OPENID_CONNECT_NEW-Logo-1024x474.jpg -->

---
<!-- Slide 16 -->
<!--: .wrap -->
### Open ID Connect overview
{{< div class="content-left" >}}
<A href="https://openid.net/connect/">OpenID Connect</A> (aka OIDC) est une couche d'authentification au dessus de <A href="https://oauth.net/2/">OAuth 2.0</A> qui est un protocole d'autorisation.

Concrétement OIDC est une API HTTP <a href=https://tools.ietf.org/html/rfc6690>Restfull</a> qui utilise le format <a href=https://tools.ietf.org/html/rfc7159>JSON</a> pour la partie donnée.

OIDC est intéressant car il permet d'être utilisé dans plusieurs cas d'usage : Web based, mobile, Javascript client.
{{< /div >}}

<figure class="content-right">
  <img alt="oidc" src="https://openid.net/wordpress-content/uploads/2014/02/OpenIDConnect-Map-4Feb2014.png">
</figure>


---
<!-- Slide XX -->
<!--: .wrap -->
### GET userinfo

~~~
GET /userinfo HTTP/1.1
Host: myservice.com
Authorization: Bearer Gp7b5hiURKpWffczofpgMJP38EnYimgxlBC1PpS2zGXUqe
~~~

<br>

~~~
HTTP/1.1 200 OK
Content-Type: application/json

{
 "sub"         : "2azdz761001",
 "name"        : "Jane Doe"
 "given_name"  : "Jane",
 "family_name" : "Doe",
 "email"       : "janedoe@example.com",
 "picture"     : "http://example.com/janedoe/myface.jpg"
}
~~~

---
<!-- Slide XX -->
<!--: .wrap -->
### Claims
Les *claims* sont des informations sur le *end-user* ou l'authentification. Une liste de *claims* standards sont définis dans la spécification.<br>

https://openid.net/specs/openid-connect-core-1_0.html#StandardClaims

---
<!-- Slide END -->
<!--: .wrap .text-landing bg=bg-white bg=aligncenter bgimage=https://images.unsplash.com/photo-1583791031153-d55e79f7f115?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1867&q=80 -->
# **Thank you for your attention**
