---
title: Mapping dell'interfaccia utente degli oggetti utente
description: Nelle tabelle seguenti vengono identificate le pagine delle proprietà fornite dallo snap-in Active Directory utenti e computer.
ms.assetid: f309c139-c957-40c4-b369-f527aa87157c
ms.tgt_platform: multiple
keywords:
- Active Directory User Object mapping AD
- Interfaccia utente mapping di Active Directory, oggetto utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc797be7c53ba7759051016ddd0548c8c7124cd2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472486"
---
# <a name="user-object-user-interface-mapping"></a>Mapping dell'interfaccia utente degli oggetti utente

Nelle tabelle seguenti vengono identificate le pagine delle proprietà fornite dallo snap-in Active Directory utenti e computer. Ogni tabella identifica gli elementi dell'interfaccia utente della pagina delle proprietà e l'attributo associato a tale elemento dell'interfaccia utente. Poiché le pagine delle proprietà visualizzate dallo snap-in Active Directory utenti e computer possono essere estese, non è possibile fornire questi dati per tutte le pagine visualizzate in una finestra delle proprietà.

## <a name="general-property-page"></a>Pagina delle proprietà generale

Nella tabella seguente sono elencate le etichette dell'interfaccia utente della pagina delle proprietà **generale** .



| Etichetta interfaccia utente         | Attributo in Active Directory Domain Services                           |
|------------------|-------------------------------------------------------------------------|
| Nome       | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                   |
| Cognome        | [**sn**](/windows/desktop/ADSchema/a-sn)                                                 |
| Iniziali         | [**iniziali**](/windows/desktop/ADSchema/a-initials)                                     |
| Nome visualizzato     | [**displayName**](/windows/desktop/ADSchema/a-displayname)                               |
| Descrizione      | [**Descrizione**](/windows/desktop/ADSchema/a-description)                               |
| Office           | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) |
| Telephone Number | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                       |
| Telefono: altro | [**otherTelephone**](/windows/desktop/ADSchema/a-othertelephone)                         |
| Posta elettronica           | [**Indirizzi di posta elettronica**](/windows/desktop/ADSchema/a-mail)                                 |
| Pagina Web         | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                               |
| Pagina Web: altro  | [**URL**](/windows/desktop/ADSchema/a-url)                                               |



 

## <a name="account-property-page"></a>Pagina delle proprietà dell'account

Nella tabella seguente sono elencate le etichette dell'interfaccia utente della pagina delle proprietà dell' **account** .



| Etichetta interfaccia utente                                | Attributo in Active Directory Domain Services                                                   | Commento                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome UserLogon                          | [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname)                                           | Questo campo viene ricavato da tutti gli elementi nell'attributo [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) che precede l'ultimo carattere "@". L'ultimo carattere "@" e tutti gli elementi successivi vengono inseriti nella casella combinata suffisso.                                                                                                                                                      |
| Nome di accesso utente (precedente a Windows 2000)      | [**sAMAccountname**](/windows/desktop/ADSchema/a-samaccountname)                                                 | Nessun commento.                                                                                                                                                                                                                                                                                                                                                                             |
| Orario di accesso                             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                         | Nessun commento.                                                                                                                                                                                                                                                                                                                                                                             |
| Accedi a                               | [**logonWorkstation**](/windows/desktop/ADSchema/a-logonworkstation)                                             | Nessun commento.                                                                                                                                                                                                                                                                                                                                                                             |
| Account bloccato                   | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) e [ **lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) | Se l'attributo [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) è diverso da zero, l'attributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) viene aggiunto a **lockoutTime** e viene confrontato con la data e l'ora correnti per determinare se l'account è bloccato.                                                                                                                                |
| Cambiamento obbligatorio password all'accesso successivo | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                         | Nessun commento.                                                                                                                                                                                                                                                                                                                                                                             |
| Cambiamento password non consentito             | N/D                                                                                             | Si tratta del controllo Change password nell'ACL.                                                                                                                                                                                                                                                                                                                                         |
| Altre opzioni account                   | [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)                                         | Gli elementi rimanenti in Opzioni account sono i bit nella maschera di bit dell'attributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) (flag in un DWORD).                                                                                                                                                                                                                                 |
| Scadenza account                         | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                 | Il controllo **scadenza account** Visualizza la data in cui l'account scadrà alla fine di. L'attributo [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) viene archiviato come data di scadenza dell'account. Per questo motivo, la data visualizzata nell' **account scadrà** il controllo verrà visualizzato come un giorno prima della data inclusa nell'attributo **accountExpires** . |



 

## <a name="address-property-page"></a>Pagina delle proprietà indirizzo

Nella tabella seguente sono elencate le etichette dell'interfaccia utente della pagina delle proprietà **Address** .



| Etichetta interfaccia utente        | Attributo in Active Directory Domain Services                                                 | Commento                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Indirizzo          | [**streetAddress**](/windows/desktop/ADSchema/a-streetaddress)                                                 | Nessun commento.                                               |
| Casella P. O.         | [**postOfficeBox**](/windows/desktop/ADSchema/a-postofficebox)                                                 | Nessun commento.                                               |
| City            | [**l**](/windows/desktop/ADSchema/a-l)                                                                         | Il nome dell'attributo **l** è una "l" minuscola come nelle impostazioni locali. |
| Provincia  | [**st**](/windows/desktop/ADSchema/a-st)                                                                       | Nessun commento.                                               |
| Cap | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                       | Nessun commento.                                               |
| Paese/Area geografica  | [**c**](/windows/desktop/ADSchema/a-c), [**co**](/windows/desktop/ADSchema/a-co)e [**CountryCode**](/windows/desktop/ADSchema/a-countrycode) | Nessun commento.                                               |



 

## <a name="member-of-property-page"></a>Membro della pagina delle proprietà

Nella tabella seguente sono elencate le etichette dell'interfaccia utente del **membro della pagina delle** proprietà.



| Etichetta interfaccia utente          | Attributo in Active Directory Domain Services   | Commento                                                                                                                                                                    |
|-------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Membro di         | [**memberOf**](/windows/desktop/ADSchema/a-memberof)             | Include tutti i gruppi nell'elenco dell'interfaccia utente, ad eccezione del gruppo primario, rappresentato nell'annuncio tramite l'attributo [**primaryGroupID**](/windows/desktop/ADSchema/a-primarygroupid) . |
| Imposta gruppo primario | [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) | LDAP: associato a [**PrimaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) del gruppo primario.                                                                                  |



 

## <a name="organization-property-page"></a>Pagina delle proprietà dell'organizzazione

Nella tabella seguente vengono illustrate le etichette dell'interfaccia utente della pagina delle proprietà dell' **organizzazione** .



| Etichetta interfaccia utente       | Attributo in Active Directory Domain Services | Commento     |
|----------------|-----------------------------------------------|-------------|
| Titolo          | [**title**](/windows/desktop/ADSchema/a-title)                 | Nessun commento. |
| department     | [**department**](/windows/desktop/ADSchema/a-department)       | Nessun commento. |
| Company        | [**azienda**](/windows/desktop/ADSchema/a-company)             | Nessun commento. |
| Responsabile: nome   | [**manager**](/windows/desktop/ADSchema/a-manager)             | Nessun commento. |
| Report diretti | [**directReports**](/windows/desktop/ADSchema/a-directreports) | Nessun commento. |



 

## <a name="profile-property-page"></a>Pagina delle proprietà del profilo

Nella tabella seguente sono elencate le etichette dell'interfaccia utente della pagina delle proprietà del **profilo** .



| Etichetta interfaccia utente                | Attributo in Active Directory Domain Services | Commento                                                                                                                 |
|-------------------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Percorso del profilo            | [**PercorsoProfilo**](/windows/desktop/ADSchema/a-profilepath)     | Nessun commento.                                                                                                             |
| Script di accesso            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)       | Nessun commento.                                                                                                             |
| Home directory: percorso locale | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | Se il **percorso locale** è selezionato, il percorso locale viene archiviato nell'attributo [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) . |
| Home directory: Connetti    | [**homeDrive**](/windows/desktop/ADSchema/a-homedrive)         | Se **Connetti** è selezionato, l'unità mappata viene archiviata nell'attributo [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) .          |
| Home directory: a         | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | Se si seleziona **Connetti** , il percorso viene archiviato nell'attributo [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) .          |



 

## <a name="telephones-property-page"></a>Pagina delle proprietà di telefoni

Nella tabella seguente sono elencati gli elementi dell'interfaccia utente della pagina delle proprietà dei **telefoni** e i relativi attributi di Active Directory.



| Etichetta interfaccia utente        | Attributo in Active Directory Domain Services                                 |
|-----------------|-------------------------------------------------------------------------------|
| Home page            | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                         |
| Home page: altro     | [**otherHomePhone**](/windows/desktop/ADSchema/a-otherhomephone)                               |
| Cercapersone           | [**pager**](/windows/desktop/ADSchema/a-pager)                                                 |
| Cercapersone: altro    | [**otherPager**](/windows/desktop/ADSchema/a-otherpager)                                       |
| Dispositivi mobili          | [**mobili**](/windows/desktop/ADSchema/a-mobile)                                               |
| Dispositivi mobili: altro   | [**otherMobile**](/windows/desktop/ADSchema/a-othermobile)                                     |
| Fax             | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)           |
| Fax: altro      | [**otherFacsimileTelephoneNumber**](/windows/desktop/ADSchema/a-otherfacsimiletelephonenumber) |
| Telefono IP        | [**ipPhone**](/windows/desktop/ADSchema/a-ipphone)                                             |
| Telefono IP: altro | [**otherIpPhone**](/windows/desktop/ADSchema/a-otheripphone)                                   |
| Note           | [**informazioni**](/windows/desktop/ADSchema/a-info)                                                   |



 

## <a name="environment-sessions-remote-control-and-terminal-services-profile-property-pages"></a>Ambiente, sessioni, controllo remoto e pagine delle proprietà del profilo di Servizi terminal

Per un oggetto utente per il supporto di Servizi terminal vengono fornite le pagine **ambiente**, **sessioni**, **controllo remoto** e **profilo Servizi terminal** . Gli elementi dell'interfaccia utente per queste pagine non corrispondono a singoli attributi. Al contrario, le impostazioni vengono archiviate in dati privati all'interno Active Directory Domain Services. È possibile accedere alle impostazioni di Servizi terminal con l'interfaccia [**IADsTsUserEx**](/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex) .

 

 