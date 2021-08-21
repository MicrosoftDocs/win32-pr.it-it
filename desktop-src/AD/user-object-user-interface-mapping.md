---
title: Mapping dell'interfaccia utente degli oggetti utente
description: Le tabelle seguenti identificano le pagine delle proprietà fornite Utenti e computer di Active Directory snap-in.
ms.assetid: f309c139-c957-40c4-b369-f527aa87157c
ms.tgt_platform: multiple
keywords:
- User Object Interfaccia utente Mapping ad
- Interfaccia utente Mapping di AD , oggetto utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656e8071b558b730ecb1fc0463834f6fbadb7eb9bf4c56b11640e2b95209735f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024500"
---
# <a name="user-object-user-interface-mapping"></a>Mapping dell'interfaccia utente degli oggetti utente

Le tabelle seguenti identificano le pagine delle proprietà fornite Utenti e computer di Active Directory snap-in. Ogni tabella identifica gli elementi dell'interfaccia utente della pagina delle proprietà e l'attributo associato a tale elemento dell'interfaccia utente. Poiché le pagine delle proprietà visualizzate dallo snap-in Utenti e computer di Active Directory possono essere estese, non è possibile fornire questi dati per tutte le pagine visualizzate in una finestra delle proprietà.

## <a name="general-property-page"></a>Pagina delle proprietà Generale

La tabella seguente elenca le etichette dell'interfaccia utente della **pagina delle** proprietà Generale.



| Etichetta dell'interfaccia utente         | Attributo in Active Directory Domain Services                           |
|------------------|-------------------------------------------------------------------------|
| Nome       | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                   |
| Cognome        | [**sn**](/windows/desktop/ADSchema/a-sn)                                                 |
| Iniziali         | [**Iniziali**](/windows/desktop/ADSchema/a-initials)                                     |
| Nome visualizzato     | [**displayName**](/windows/desktop/ADSchema/a-displayname)                               |
| Descrizione      | [**description**](/windows/desktop/ADSchema/a-description)                               |
| Office           | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) |
| Telephone Number | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                       |
| Telefono: Altro | [**otherTelephone**](/windows/desktop/ADSchema/a-othertelephone)                         |
| Posta elettronica           | [**Indirizzi di posta elettronica**](/windows/desktop/ADSchema/a-mail)                                 |
| Pagina Web         | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                               |
| Pagina Web: Altro  | [**Url**](/windows/desktop/ADSchema/a-url)                                               |



 

## <a name="account-property-page"></a>Pagina delle proprietà Account

La tabella seguente elenca le etichette dell'interfaccia utente della **pagina delle proprietà** Account.



| Etichetta dell'interfaccia utente                                | Attributo in Active Directory Domain Services                                                   | Commento                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UserLogon Name                          | [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname)                                           | Questo campo è tratto da tutti gli elementi [**dell'attributo userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) che precedono l'ultimo carattere '@'. L'ultimo carattere "@" e tutti gli elementi dopo che è stato inserito nella casella combinata dei suffissi.                                                                                                                                                      |
| Nome di accesso utente (versione Windows 2000)      | [**Samaccountname**](/windows/desktop/ADSchema/a-samaccountname)                                                 | Nessun commento.                                                                                                                                                                                                                                                                                                                                                                             |
| Orario di accesso                             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                         | Nessun commento.                                                                                                                                                                                                                                                                                                                                                                             |
| Accedi a                               | [**logonWorkstation**](/windows/desktop/ADSchema/a-logonworkstation)                                             | Nessun commento.                                                                                                                                                                                                                                                                                                                                                                             |
| Account bloccato                   | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) e [ **lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) | Se [**l'attributo lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) è diverso da zero, l'attributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) viene aggiunto a **lockoutTime** e confrontato con la data e l'ora correnti per determinare se l'account è bloccato.                                                                                                                                |
| Cambiamento obbligatorio password all'accesso successivo | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                         | Nessun commento.                                                                                                                                                                                                                                                                                                                                                                             |
| Cambiamento password non consentito             | N/A                                                                                             | Si tratta del controllo Cambia password nell'elenco di controllo di accesso.                                                                                                                                                                                                                                                                                                                                         |
| Altre opzioni dell'account                   | [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)                                         | Gli elementi rimanenti in Opzioni account attivano/disattivano i bit nella maschera di bit [**dell'attributo userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) (flag in un valore DWORD).                                                                                                                                                                                                                                 |
| Scadenza account                         | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                 | Il **controllo Scadenza account visualizza** la data di scadenza dell'account. [**L'attributo accountExpires**](/windows/desktop/ADSchema/a-accountexpires) viene archiviato come data di scadenza dell'account. Per questo modo, la data  visualizzata nel controllo Scadenza account verrà visualizzata come un giorno precedente alla data contenuta nell'attributo **accountExpires.** |



 

## <a name="address-property-page"></a>Pagina delle proprietà Indirizzo

La tabella seguente elenca le etichette dell'interfaccia utente della **pagina delle proprietà** Indirizzo.



| Etichetta dell'interfaccia utente        | Attributo in Active Directory Domain Services                                                 | Commento                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Indirizzo          | [**streetAddress**](/windows/desktop/ADSchema/a-streetaddress)                                                 | Nessun commento.                                               |
| P.o.box         | [**postOfficeBox**](/windows/desktop/ADSchema/a-postofficebox)                                                 | Nessun commento.                                               |
| City            | [**L**](/windows/desktop/ADSchema/a-l)                                                                         | Il nome dell'attributo **l** è una "L" minuscola come in Locale. |
| Provincia  | [**st**](/windows/desktop/ADSchema/a-st)                                                                       | Nessun commento.                                               |
| CAP | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                       | Nessun commento.                                               |
| Paese/Area geografica  | [**c**](/windows/desktop/ADSchema/a-c), [**co**](/windows/desktop/ADSchema/a-co)e [**countryCode**](/windows/desktop/ADSchema/a-countrycode) | Nessun commento.                                               |



 

## <a name="member-of-property-page"></a>Membro della pagina delle proprietà

Nella tabella seguente sono elencate le etichette dell'interfaccia utente **della pagina delle proprietà Membro** di .



| Etichetta dell'interfaccia utente          | Attributo in Active Directory Domain Services   | Commento                                                                                                                                                                    |
|-------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Membro di         | [**memberOf**](/windows/desktop/ADSchema/a-memberof)             | Include tutti i gruppi nell'elenco dell'interfaccia utente, ad eccezione del gruppo primario, rappresentato in Active Directory tramite [**l'attributo primaryGroupId.**](/windows/desktop/ADSchema/a-primarygroupid) |
| Impostare un gruppo primario | [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) | LDAP: associato a [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) del gruppo primario.                                                                                  |



 

## <a name="organization-property-page"></a>Pagina delle proprietà Organizzazione

La tabella seguente mostra le etichette dell'interfaccia utente della **pagina delle proprietà** Organizzazione.



| Etichetta dell'interfaccia utente       | Attributo in Active Directory Domain Services | Commento     |
|----------------|-----------------------------------------------|-------------|
| Titolo          | [**title**](/windows/desktop/ADSchema/a-title)                 | Nessun commento. |
| department     | [**department**](/windows/desktop/ADSchema/a-department)       | Nessun commento. |
| Company        | [**Azienda**](/windows/desktop/ADSchema/a-company)             | Nessun commento. |
| Manager:Name   | [**Manager**](/windows/desktop/ADSchema/a-manager)             | Nessun commento. |
| Report diretti | [**directReports**](/windows/desktop/ADSchema/a-directreports) | Nessun commento. |



 

## <a name="profile-property-page"></a>Pagina delle proprietà Profilo

Nella tabella seguente sono elencate le etichette dell'interfaccia utente della **pagina delle proprietà** Profilo.



| Etichetta dell'interfaccia utente                | Attributo in Active Directory Domain Services | Commento                                                                                                                 |
|-------------------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Percorso del profilo            | [**profilePath**](/windows/desktop/ADSchema/a-profilepath)     | Nessun commento.                                                                                                             |
| Script di accesso            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)       | Nessun commento.                                                                                                             |
| Cartella Home: Percorso locale | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | Se **si seleziona Percorso** locale, il percorso locale viene archiviato nell'attributo [**homeDirectory.**](/windows/desktop/ADSchema/a-homedirectory) |
| Home Cartella: Connessione    | [**Homedrive**](/windows/desktop/ADSchema/a-homedrive)         | Se **Connessione** selezionata, l'unità mappata viene archiviata nell'attributo [**homeDrive.**](/windows/desktop/ADSchema/a-homedrive)          |
| Home Cartella: a         | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | Se **Connessione** selezionata, il percorso viene archiviato nell'attributo [**homeDirectory.**](/windows/desktop/ADSchema/a-homedirectory)          |



 

## <a name="telephones-property-page"></a>Pagina delle proprietà Telefoni

Nella tabella seguente sono elencati gli elementi dell'interfaccia utente della **pagina delle proprietà Telefoni** e i relativi attributi di Active Directory corrispondenti.



| Etichetta dell'interfaccia utente        | Attributo in Active Directory Domain Services                                 |
|-----------------|-------------------------------------------------------------------------------|
| Home page            | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                         |
| Home: Altro     | [**otherHomePhone**](/windows/desktop/ADSchema/a-otherhomephone)                               |
| Cercapersone           | [**Pager**](/windows/desktop/ADSchema/a-pager)                                                 |
| Pager: Altro    | [**otherPager**](/windows/desktop/ADSchema/a-otherpager)                                       |
| Dispositivi mobili          | [**Mobile**](/windows/desktop/ADSchema/a-mobile)                                               |
| Mobile: Altro   | [**otherMobile**](/windows/desktop/ADSchema/a-othermobile)                                     |
| Fax             | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)           |
| Fax: Altro      | [**otherFacsimileTelephoneNumber**](/windows/desktop/ADSchema/a-otherfacsimiletelephonenumber) |
| Telefono IP        | [**ipPhone**](/windows/desktop/ADSchema/a-ipphone)                                             |
| Telefono IP: Altro | [**otherIpPhone**](/windows/desktop/ADSchema/a-otheripphone)                                   |
| Note           | [**Informazioni**](/windows/desktop/ADSchema/a-info)                                                   |



 

## <a name="environment-sessions-remote-control-and-terminal-services-profile-property-pages"></a>Pagine delle proprietà ambiente, sessioni, controllo remoto e profilo di Servizi terminal

Le **pagine Ambiente**, **Sessioni**, Controllo **remoto** e Profilo servizi **terminal** vengono fornite per un oggetto utente per supportare Servizi terminal. Gli elementi dell'interfaccia utente per queste pagine non corrispondono ai singoli attributi. Le impostazioni vengono invece archiviate in dati privati all'interno Active Directory Domain Services. È possibile accedere alle impostazioni di Servizi terminal con [**l'interfaccia IADsTsUserEx.**](/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex)

 

 