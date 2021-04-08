---
title: Classe Organizational-Unit
description: Contenitore per l'archiviazione di utenti, computer e altri oggetti account.
ms.assetid: a5a99dc7-9000-478c-9545-473cfb6ddf6c
ms.tgt_platform: multiple
keywords:
- Schema di AD Organizational-Unit Class
- Schema di Active Directory della classe organizationalUnit
topic_type:
- apiref
api_name:
- Organizational-Unit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a02c893b09ec6a2292c0304c10e94cfda1616f91
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965028"
---
# <a name="organizational-unit-class"></a>Classe Organizational-Unit

Contenitore per l'archiviazione di utenti, computer e altri oggetti account.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Organizational-Unit                  |
| LDAP-Display-Name | organizationalUnit                   |
| Privilegio aggiornamento  | Chiunque può aggiornare questo oggetto.       |
| Frequenza di aggiornamento  | \-                                   |
| Schema-ID-GUID    | bf967aa5-0de6-11d0-a285-00aa003049e2 |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam-attributes)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attributes (Attributi)](#windows-2000-server-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                    |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                        |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                       |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                  |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                                                                                                                                                        |
| RDN-att-ID                  | [**Nome-unità-organizzativa**](a-ou.md)<br/>                                                                                                                                                                                                                                                      |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                          |
| Possibili superiori          | [**Dominio-organizzazione DNS**](c-domaindns.md)**-unità organizzativa**[](c-organization.md)                                                                                                                                                                                                           |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                                                                       |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                             |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (OA;; CCDC; bf967a86-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aba-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967a9c-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aa8-0de6-11D0-A285-00aa003049e2;; PO) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                               |



## <a name="windows-2000-server-attributes"></a>Attributi del server Windows 2000

Questa classe contiene gli attributi seguenti per Windows 2000 Server:



| Attributo                                                                 | Obbligatorio | Derivato da                    |
|---------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria aziendale**](a-businesscategory.md)                           | Falso     | **Unità organizzativa**         |
| [**Nome canonico**](a-canonicalname.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Codice paese**](a-countrycode.md)                                     | Falso     | **Unità organizzativa**         |
| [**Nome paese**](a-c.md)                                               | Falso     | **Unità organizzativa**         |
| [**Creazione timestamp**](a-createtimestamp.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Gruppo predefinito**](a-defaultgroup.md)                                   | Falso     | **Unità organizzativa**         |
| [**Descrizione**](a-description.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Profilo desktop**](a-desktopprofile.md)                               | Falso     | **Unità organizzativa**         |
| [**Indicatore di destinazione**](a-destinationindicator.md)                   | Falso     | **Unità organizzativa**         |
| [**Nome visualizzato**](a-displayname.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**DSA-firma**](a-dsasignature.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome estensione**](a-extensionname.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Fax-telefono-numero**](a-facsimiletelephonenumber.md)          | Falso     | **Unità organizzativa**         |
| [**Bandiere**](a-flags.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da-entry**](a-fromentry.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**GP-collegamento**](a-gplink.md)                                               | Falso     | **Unità organizzativa**         |
| [**GP-opzioni**](a-gpoptions.md)                                         | Falso     | **Unità organizzativa**         |
| [**Tipo di istanza**](a-instancetype.md)                                   | Vero      | [**In alto**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)            | Falso     | **Unità organizzativa**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Viene eliminato**](a-isdeleted.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-member-of-DL**](a-memberof.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome località**](a-l.md)                                              | Falso     | **Unità organizzativa**         |
| [**Logo**](a-thumbnaillogo.md)                                           | Falso     | **Unità organizzativa**         |
| [**Gestito da**](a-managedby.md)                                         | Falso     | **Unità organizzativa**         |
| [**Oggetti gestiti**](a-managedobjects.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-by**](a-masteredby.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica-timestamp**](a-modifytimestamp.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)    | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                  | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria oggetto**](a-objectcategory.md)                               | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe Object**](a-objectclass.md)                                     | Vero      | [**In alto**](c-top.md)<br/> |
| [**GUID oggetto**](a-objectguid.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome-unità-organizzativa**](a-ou.md)                                  | Vero      | **Unità organizzativa**         |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**Set di attributi parziali**](a-partialattributeset.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)     | Falso     | **Unità organizzativa**         |
| [**Possibili-inferiori**](a-possibleinferiors.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo postale**](a-postaladdress.md)                                 | Falso     | **Unità organizzativa**         |
| [**Codice postale**](a-postalcode.md)                                       | Falso     | **Unità organizzativa**         |
| [**Casella Post-Office**](a-postofficebox.md)                                | Falso     | **Unità organizzativa**         |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)            | Falso     | **Unità organizzativa**         |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-criteri-BL**](a-querypolicybl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo registrato**](a-registeredaddress.md)                         | Falso     | **Unità organizzativa**         |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-da**](a-repsfrom.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da Reps a**](a-repsto.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Guida alla ricerca**](a-searchguide.md)                                     | Falso     | **Unità organizzativa**         |
| [**Vedere anche**](a-seealso.md)                                             | Falso     | **Unità organizzativa**         |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Stato-o-provincia-nome**](a-st.md)                                    | Falso     | **Unità organizzativa**         |
| [**Indirizzo via**](a-street.md)                                        | Falso     | **Unità organizzativa**         |
| [**Riferimenti secondari**](a-subrefs.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Numero di telefono**](a-telephonenumber.md)                             | Falso     | **Unità organizzativa**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)        | Falso     | **Unità organizzativa**         |
| [**Numero telex**](a-telexnumber.md)                                     | Falso     | **Unità organizzativa**         |
| [**Testo-paese**](a-co.md)                                              | Falso     | **Unità organizzativa**         |
| [**Suffissi UPN**](a-upnsuffixes.md)                                     | Falso     | **Unità organizzativa**         |
| [**Password utente**](a-userpassword.md)                                   | Falso     | **Unità organizzativa**         |
| [**USN-modificato**](a-usnchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN creato**](a-usncreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-tra siti**](a-usnintersite.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-origine**](a-usnsource.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**WBEM-percorso**](a-wbempath.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando-modificato**](a-whenchanged.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Data di creazione**](a-whencreated.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-pagina-altro**](a-url.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**X121-indirizzo**](a-x121address.md)                                     | Falso     | **Unità organizzativa**         |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributes (Attributi)](#windows-server-2003-attributes)
-   [Diritti estesi](#windows-server-2003-extended-rights)



| Voce | Valore |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-att-ID                  | [**Nome-unità-organizzativa**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Possibili superiori          | [**Dominio-organizzazione DNS**](c-domaindns.md)**-unità organizzativa**[](c-organization.md)[](c-country.md)                                                                                                                                                                                                                                                    |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (OA;; CCDC; bf967a86-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aba-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967a9c-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aa8-0de6-11D0-A285-00aa003049e2;; PO) (A;; RPLCLORC;;; AU) (A;; LCRPLORC;;; ED) (OA;; CCDC; 4828CC14-1437-45bc-9B07-AD6F015E5F28;; Ao |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2003-attributes"></a>Attributi di Windows Server 2003

Questa classe contiene gli attributi seguenti per Windows Server 2003:



| Attributo                                                                   | Obbligatorio | Derivato da                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria aziendale**](a-businesscategory.md)                             | Falso     | **Unità organizzativa**         |
| [**Nome canonico**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Codice paese**](a-countrycode.md)                                       | Falso     | **Unità organizzativa**         |
| [**Nome paese**](a-c.md)                                                 | Falso     | **Unità organizzativa**         |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Gruppo predefinito**](a-defaultgroup.md)                                     | Falso     | **Unità organizzativa**         |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Profilo desktop**](a-desktopprofile.md)                                 | Falso     | **Unità organizzativa**         |
| [**Indicatore di destinazione**](a-destinationindicator.md)                     | Falso     | **Unità organizzativa**         |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**DSA-firma**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome estensione**](a-extensionname.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Fax-telefono-numero**](a-facsimiletelephonenumber.md)            | Falso     | **Unità organizzativa**         |
| [**Bandiere**](a-flags.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da-entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**GP-collegamento**](a-gplink.md)                                                 | Falso     | **Unità organizzativa**         |
| [**GP-opzioni**](a-gpoptions.md)                                           | Falso     | **Unità organizzativa**         |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | **Unità organizzativa**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Viene eliminato**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome località**](a-l.md)                                                | Falso     | **Unità organizzativa**         |
| [**Logo**](a-thumbnaillogo.md)                                             | Falso     | **Unità organizzativa**         |
| [**Gestito da**](a-managedby.md)                                           | Falso     | **Unità organizzativa**         |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-by**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica-timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)         | Falso     | **Unità organizzativa**         |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria oggetto**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe Object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/> |
| [**GUID oggetto**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome-unità-organizzativa**](a-ou.md)                                    | Vero      | **Unità organizzativa**         |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Set di attributi parziali**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falso     | **Unità organizzativa**         |
| [**Possibili-inferiori**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo postale**](a-postaladdress.md)                                   | Falso     | **Unità organizzativa**         |
| [**Codice postale**](a-postalcode.md)                                         | Falso     | **Unità organizzativa**         |
| [**Casella Post-Office**](a-postofficebox.md)                                  | Falso     | **Unità organizzativa**         |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)              | Falso     | **Unità organizzativa**         |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-criteri-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo registrato**](a-registeredaddress.md)                           | Falso     | **Unità organizzativa**         |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-da**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da Reps a**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Guida alla ricerca**](a-searchguide.md)                                       | Falso     | **Unità organizzativa**         |
| [**Vedere anche**](a-seealso.md)                                               | Falso     | **Unità organizzativa**         |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Stato-o-provincia-nome**](a-st.md)                                      | Falso     | **Unità organizzativa**         |
| [**Indirizzo via**](a-street.md)                                          | Falso     | **Unità organizzativa**         |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Numero di telefono**](a-telephonenumber.md)                               | Falso     | **Unità organizzativa**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falso     | **Unità organizzativa**         |
| [**Numero telex**](a-telexnumber.md)                                       | Falso     | **Unità organizzativa**         |
| [**Testo-paese**](a-co.md)                                                | Falso     | **Unità organizzativa**         |
| [**Suffissi UPN**](a-upnsuffixes.md)                                       | Falso     | **Unità organizzativa**         |
| [**Password utente**](a-userpassword.md)                                     | Falso     | **Unità organizzativa**         |
| [**USN-modificato**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN creato**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-tra siti**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-origine**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**WBEM-percorso**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando-modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Data di creazione**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-pagina-altro**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**X121-indirizzo**](a-x121address.md)                                       | Falso     | **Unità organizzativa**         |



## <a name="windows-server-2003-extended-rights"></a>Diritti estesi di Windows Server 2003

Questa classe contiene i seguenti diritti estesi per Windows Server 2003:



| Nome comune                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generazione-RSoP-registrazione**](r-generate-rsop-logging.md)   |



## <a name="adam"></a>ADAM

-   [Attributes (Attributi)](#adam-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                      |
| Object-Category             | 1                                                                                                                          |
| Default-Object-Category     | \-                                                                                                                         |
| Governs-Id                  | 2.5.6.5                                                                                                                    |
| Valore predefinito-nascondiglio        | 0                                                                                                                          |
| RDN-att-ID                  | [**Nome-unità-organizzativa**](a-ou.md)<br/>                                                                        |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                            |
| Possibili superiori          | [**Dominio-organizzazione DNS**](c-domaindns.md)**-unità organizzativa**[](c-organization.md)[](c-country.md) |
| Classi ausiliarie           | \-                                                                                                                         |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                               |
| Descrittore di sicurezza predefinito | D:S                                                                                                                       |
| System-Flags                | 0x00000010                                                                                                                 |



## <a name="adam-attributes"></a>Attributi ADAM

Questa classe contiene gli attributi seguenti per ADAM:



| Attributo                                                                   | Obbligatorio | Derivato da                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria aziendale**](a-businesscategory.md)                             | Falso     | **Unità organizzativa**         |
| [**Nome canonico**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Codice paese**](a-countrycode.md)                                       | Falso     | **Unità organizzativa**         |
| [**Nome paese**](a-c.md)                                                 | Falso     | **Unità organizzativa**         |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Gruppo predefinito**](a-defaultgroup.md)                                     | Falso     | **Unità organizzativa**         |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Profilo desktop**](a-desktopprofile.md)                                 | Falso     | **Unità organizzativa**         |
| [**Indicatore di destinazione**](a-destinationindicator.md)                     | Falso     | **Unità organizzativa**         |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**DSA-firma**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Fax-telefono-numero**](a-facsimiletelephonenumber.md)            | Falso     | **Unità organizzativa**         |
| [**Da-entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | **Unità organizzativa**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Viene eliminato**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome località**](a-l.md)                                                | Falso     | **Unità organizzativa**         |
| [**Logo**](a-thumbnaillogo.md)                                             | Falso     | **Unità organizzativa**         |
| [**Gestito da**](a-managedby.md)                                           | Falso     | **Unità organizzativa**         |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-by**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica-timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-service-account-BL**](a-msds-serviceaccountbl.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria oggetto**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe Object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/> |
| [**GUID oggetto**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome-unità-organizzativa**](a-ou.md)                                    | Vero      | **Unità organizzativa**         |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Set di attributi parziali**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falso     | **Unità organizzativa**         |
| [**Possibili-inferiori**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo postale**](a-postaladdress.md)                                   | Falso     | **Unità organizzativa**         |
| [**Codice postale**](a-postalcode.md)                                         | Falso     | **Unità organizzativa**         |
| [**Casella Post-Office**](a-postofficebox.md)                                  | Falso     | **Unità organizzativa**         |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)              | Falso     | **Unità organizzativa**         |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-criteri-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo registrato**](a-registeredaddress.md)                           | Falso     | **Unità organizzativa**         |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-da**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da Reps a**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Guida alla ricerca**](a-searchguide.md)                                       | Falso     | **Unità organizzativa**         |
| [**Vedere anche**](a-seealso.md)                                               | Falso     | **Unità organizzativa**         |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Stato-o-provincia-nome**](a-st.md)                                      | Falso     | **Unità organizzativa**         |
| [**Indirizzo via**](a-street.md)                                          | Falso     | **Unità organizzativa**         |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Numero di telefono**](a-telephonenumber.md)                               | Falso     | **Unità organizzativa**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falso     | **Unità organizzativa**         |
| [**Numero telex**](a-telexnumber.md)                                       | Falso     | **Unità organizzativa**         |
| [**Testo-paese**](a-co.md)                                                | Falso     | **Unità organizzativa**         |
| [**Suffissi UPN**](a-upnsuffixes.md)                                       | Falso     | **Unità organizzativa**         |
| [**Password utente**](a-userpassword.md)                                     | Falso     | **Unità organizzativa**         |
| [**USN-modificato**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN creato**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-tra siti**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-origine**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**WBEM-percorso**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando-modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Data di creazione**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-pagina-altro**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**X121-indirizzo**](a-x121address.md)                                       | Falso     | **Unità organizzativa**         |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributes (Attributi)](#windows-server-2003-r2-attributes)
-   [Diritti estesi](#windows-server-2003-r2-extended-rights)



| Voce | Valore |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-att-ID                  | [**Nome-unità-organizzativa**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Possibili superiori          | [**Dominio-organizzazione DNS**](c-domaindns.md)**-unità organizzativa**[](c-organization.md)[](c-country.md)                                                                                                                                                                                                                                                    |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (OA;; CCDC; bf967a86-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aba-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967a9c-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aa8-0de6-11D0-A285-00aa003049e2;; PO) (A;; RPLCLORC;;; AU) (A;; LCRPLORC;;; ED) (OA;; CCDC; 4828CC14-1437-45bc-9B07-AD6F015E5F28;; Ao |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2003-r2-attributes"></a>Attributi di Windows Server 2003 R2

Questa classe contiene gli attributi seguenti per Windows Server 2003 R2:



| Attributo                                                                   | Obbligatorio | Derivato da                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria aziendale**](a-businesscategory.md)                             | Falso     | **Unità organizzativa**         |
| [**Nome canonico**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Codice paese**](a-countrycode.md)                                       | Falso     | **Unità organizzativa**         |
| [**Nome paese**](a-c.md)                                                 | Falso     | **Unità organizzativa**         |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Gruppo predefinito**](a-defaultgroup.md)                                     | Falso     | **Unità organizzativa**         |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Profilo desktop**](a-desktopprofile.md)                                 | Falso     | **Unità organizzativa**         |
| [**Indicatore di destinazione**](a-destinationindicator.md)                     | Falso     | **Unità organizzativa**         |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**DSA-firma**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome estensione**](a-extensionname.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Fax-telefono-numero**](a-facsimiletelephonenumber.md)            | Falso     | **Unità organizzativa**         |
| [**Bandiere**](a-flags.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da-entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**GP-collegamento**](a-gplink.md)                                                 | Falso     | **Unità organizzativa**         |
| [**GP-opzioni**](a-gpoptions.md)                                           | Falso     | **Unità organizzativa**         |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | **Unità organizzativa**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Viene eliminato**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome località**](a-l.md)                                                | Falso     | **Unità organizzativa**         |
| [**Logo**](a-thumbnaillogo.md)                                             | Falso     | **Unità organizzativa**         |
| [**Gestito da**](a-managedby.md)                                           | Falso     | **Unità organizzativa**         |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-by**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica-timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)         | Falso     | **Unità organizzativa**         |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria oggetto**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe Object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/> |
| [**GUID oggetto**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome-unità-organizzativa**](a-ou.md)                                    | Vero      | **Unità organizzativa**         |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Set di attributi parziali**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falso     | **Unità organizzativa**         |
| [**Possibili-inferiori**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo postale**](a-postaladdress.md)                                   | Falso     | **Unità organizzativa**         |
| [**Codice postale**](a-postalcode.md)                                         | Falso     | **Unità organizzativa**         |
| [**Casella Post-Office**](a-postofficebox.md)                                  | Falso     | **Unità organizzativa**         |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)              | Falso     | **Unità organizzativa**         |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-criteri-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo registrato**](a-registeredaddress.md)                           | Falso     | **Unità organizzativa**         |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-da**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da Reps a**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Guida alla ricerca**](a-searchguide.md)                                       | Falso     | **Unità organizzativa**         |
| [**Vedere anche**](a-seealso.md)                                               | Falso     | **Unità organizzativa**         |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Stato-o-provincia-nome**](a-st.md)                                      | Falso     | **Unità organizzativa**         |
| [**Indirizzo via**](a-street.md)                                          | Falso     | **Unità organizzativa**         |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Numero di telefono**](a-telephonenumber.md)                               | Falso     | **Unità organizzativa**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falso     | **Unità organizzativa**         |
| [**Numero telex**](a-telexnumber.md)                                       | Falso     | **Unità organizzativa**         |
| [**Testo-paese**](a-co.md)                                                | Falso     | **Unità organizzativa**         |
| [**Suffissi UPN**](a-upnsuffixes.md)                                       | Falso     | **Unità organizzativa**         |
| [**Password utente**](a-userpassword.md)                                     | Falso     | **Unità organizzativa**         |
| [**USN-modificato**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN creato**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-tra siti**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-origine**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**WBEM-percorso**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando-modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Data di creazione**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-pagina-altro**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**X121-indirizzo**](a-x121address.md)                                       | Falso     | **Unità organizzativa**         |



## <a name="windows-server-2003-r2-extended-rights"></a>Diritti estesi di Windows Server 2003 R2

Questa classe contiene i seguenti diritti estesi per Windows Server 2003 R2:



| Nome comune                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generazione-RSoP-registrazione**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributes (Attributi)](#windows-server-2008-attributes)
-   [Diritti estesi](#windows-server-2008-extended-rights)



| Voce | Valore |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-att-ID                  | [**Nome-unità-organizzativa**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Possibili superiori          | [**Dominio-organizzazione DNS**](c-domaindns.md)**-unità organizzativa**[](c-organization.md)[](c-country.md)                                                                                                                                                                                                                                                    |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (OA;; CCDC; bf967a86-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aba-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967a9c-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aa8-0de6-11D0-A285-00aa003049e2;; PO) (A;; RPLCLORC;;; AU) (A;; LCRPLORC;;; ED) (OA;; CCDC; 4828CC14-1437-45bc-9B07-AD6F015E5F28;; Ao |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2008-attributes"></a>Attributi di Windows Server 2008

Questa classe contiene gli attributi seguenti per Windows Server 2008:



| Attributo                                                                      | Obbligatorio | Derivato da                    |
|--------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria aziendale**](a-businesscategory.md)                                | Falso     | **Unità organizzativa**         |
| [**Nome canonico**](a-canonicalname.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Codice paese**](a-countrycode.md)                                          | Falso     | **Unità organizzativa**         |
| [**Nome paese**](a-c.md)                                                    | Falso     | **Unità organizzativa**         |
| [**Creazione timestamp**](a-createtimestamp.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Gruppo predefinito**](a-defaultgroup.md)                                        | Falso     | **Unità organizzativa**         |
| [**Descrizione**](a-description.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Profilo desktop**](a-desktopprofile.md)                                    | Falso     | **Unità organizzativa**         |
| [**Indicatore di destinazione**](a-destinationindicator.md)                        | Falso     | **Unità organizzativa**         |
| [**Nome visualizzato**](a-displayname.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**DSA-firma**](a-dsasignature.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome estensione**](a-extensionname.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Fax-telefono-numero**](a-facsimiletelephonenumber.md)               | Falso     | **Unità organizzativa**         |
| [**Bandiere**](a-flags.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da-entry**](a-fromentry.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**GP-collegamento**](a-gplink.md)                                                    | Falso     | **Unità organizzativa**         |
| [**GP-opzioni**](a-gpoptions.md)                                              | Falso     | **Unità organizzativa**         |
| [**Tipo di istanza**](a-instancetype.md)                                        | Vero      | [**In alto**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                 | Falso     | **Unità organizzativa**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Viene eliminato**](a-isdeleted.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-member-of-DL**](a-memberof.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome località**](a-l.md)                                                   | Falso     | **Unità organizzativa**         |
| [**Logo**](a-thumbnaillogo.md)                                                | Falso     | **Unità organizzativa**         |
| [**Gestito da**](a-managedby.md)                                              | Falso     | **Unità organizzativa**         |
| [**Oggetti gestiti**](a-managedobjects.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-by**](a-masteredby.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)            | Falso     | **Unità organizzativa**         |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)         | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                       | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria oggetto**](a-objectcategory.md)                                    | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe Object**](a-objectclass.md)                                          | Vero      | [**In alto**](c-top.md)<br/> |
| [**GUID oggetto**](a-objectguid.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome-unità-organizzativa**](a-ou.md)                                       | Vero      | **Unità organizzativa**         |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Set di attributi parziali**](a-partialattributeset.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)          | Falso     | **Unità organizzativa**         |
| [**Possibili-inferiori**](a-possibleinferiors.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo postale**](a-postaladdress.md)                                      | Falso     | **Unità organizzativa**         |
| [**Codice postale**](a-postalcode.md)                                            | Falso     | **Unità organizzativa**         |
| [**Casella Post-Office**](a-postofficebox.md)                                     | Falso     | **Unità organizzativa**         |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)                 | Falso     | **Unità organizzativa**         |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-criteri-BL**](a-querypolicybl.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo registrato**](a-registeredaddress.md)                              | Falso     | **Unità organizzativa**         |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-da**](a-repsfrom.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da Reps a**](a-repsto.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Guida alla ricerca**](a-searchguide.md)                                          | Falso     | **Unità organizzativa**         |
| [**Vedere anche**](a-seealso.md)                                                  | Falso     | **Unità organizzativa**         |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Stato-o-provincia-nome**](a-st.md)                                         | Falso     | **Unità organizzativa**         |
| [**Indirizzo via**](a-street.md)                                             | Falso     | **Unità organizzativa**         |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riferimenti secondari**](a-subrefs.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Numero di telefono**](a-telephonenumber.md)                                  | Falso     | **Unità organizzativa**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)             | Falso     | **Unità organizzativa**         |
| [**Numero telex**](a-telexnumber.md)                                          | Falso     | **Unità organizzativa**         |
| [**Testo-paese**](a-co.md)                                                   | Falso     | **Unità organizzativa**         |
| [**Suffissi UPN**](a-upnsuffixes.md)                                          | Falso     | **Unità organizzativa**         |
| [**Password utente**](a-userpassword.md)                                        | Falso     | **Unità organizzativa**         |
| [**USN-modificato**](a-usnchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN creato**](a-usncreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-tra siti**](a-usnintersite.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-origine**](a-usnsource.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**WBEM-percorso**](a-wbempath.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando-modificato**](a-whenchanged.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Data di creazione**](a-whencreated.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-pagina-altro**](a-url.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**X121-indirizzo**](a-x121address.md)                                          | Falso     | **Unità organizzativa**         |



## <a name="windows-server-2008-extended-rights"></a>Diritti estesi di Windows Server 2008

Questa classe contiene i seguenti diritti estesi per Windows Server 2008:



| Nome comune                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generazione-RSoP-registrazione**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributes (Attributi)](#windows-server-2008-r2-attributes)
-   [Diritti estesi](#windows-server-2008-r2-extended-rights)



| Voce | Valore |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-att-ID                  | [**Nome-unità-organizzativa**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Possibili superiori          | [**Dominio-organizzazione DNS**](c-domaindns.md)**-unità organizzativa**[](c-organization.md)[](c-country.md)                                                                                                                                                                                                                                                    |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (OA;; CCDC; bf967a86-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aba-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967a9c-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aa8-0de6-11D0-A285-00aa003049e2;; PO) (A;; RPLCLORC;;; AU) (A;; LCRPLORC;;; ED) (OA;; CCDC; 4828CC14-1437-45bc-9B07-AD6F015E5F28;; Ao |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2008-r2-attributes"></a>Attributi di Windows Server 2008 R2

Questa classe contiene gli attributi seguenti per Windows Server 2008 R2:



| Attributo                                                                        | Obbligatorio | Derivato da                    |
|----------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria aziendale**](a-businesscategory.md)                                  | Falso     | **Unità organizzativa**         |
| [**Nome canonico**](a-canonicalname.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Codice paese**](a-countrycode.md)                                            | Falso     | **Unità organizzativa**         |
| [**Nome paese**](a-c.md)                                                      | Falso     | **Unità organizzativa**         |
| [**Creazione timestamp**](a-createtimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Gruppo predefinito**](a-defaultgroup.md)                                          | Falso     | **Unità organizzativa**         |
| [**Descrizione**](a-description.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Profilo desktop**](a-desktopprofile.md)                                      | Falso     | **Unità organizzativa**         |
| [**Indicatore di destinazione**](a-destinationindicator.md)                          | Falso     | **Unità organizzativa**         |
| [**Nome visualizzato**](a-displayname.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**DSA-firma**](a-dsasignature.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome estensione**](a-extensionname.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Fax-telefono-numero**](a-facsimiletelephonenumber.md)                 | Falso     | **Unità organizzativa**         |
| [**Bandiere**](a-flags.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da-entry**](a-fromentry.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**GP-collegamento**](a-gplink.md)                                                      | Falso     | **Unità organizzativa**         |
| [**GP-opzioni**](a-gpoptions.md)                                                | Falso     | **Unità organizzativa**         |
| [**Tipo di istanza**](a-instancetype.md)                                          | Vero      | [**In alto**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                   | Falso     | **Unità organizzativa**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Viene eliminato**](a-isdeleted.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-member-of-DL**](a-memberof.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riciclato**](a-isrecycled.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome località**](a-l.md)                                                     | Falso     | **Unità organizzativa**         |
| [**Logo**](a-thumbnaillogo.md)                                                  | Falso     | **Unità organizzativa**         |
| [**Gestito da**](a-managedby.md)                                                | Falso     | **Unità organizzativa**         |
| [**Oggetti gestiti**](a-managedobjects.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-by**](a-masteredby.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)              | Falso     | **Unità organizzativa**         |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)           | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Enabled-feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-host-Service-account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-ultimo-noto-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-locale-effettivo-eliminazione-ora**](a-msds-localeffectivedeletiontime.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-local-effective-riciclo-tempo**](a-msds-localeffectiverecycletime.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                         | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria oggetto**](a-objectcategory.md)                                      | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe Object**](a-objectclass.md)                                            | Vero      | [**In alto**](c-top.md)<br/> |
| [**GUID oggetto**](a-objectguid.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome-unità-organizzativa**](a-ou.md)                                         | Vero      | **Unità organizzativa**         |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Set di attributi parziali**](a-partialattributeset.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)            | Falso     | **Unità organizzativa**         |
| [**Possibili-inferiori**](a-possibleinferiors.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo postale**](a-postaladdress.md)                                        | Falso     | **Unità organizzativa**         |
| [**Codice postale**](a-postalcode.md)                                              | Falso     | **Unità organizzativa**         |
| [**Casella Post-Office**](a-postofficebox.md)                                       | Falso     | **Unità organizzativa**         |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)                   | Falso     | **Unità organizzativa**         |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-criteri-BL**](a-querypolicybl.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo registrato**](a-registeredaddress.md)                                | Falso     | **Unità organizzativa**         |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-da**](a-repsfrom.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da Reps a**](a-repsto.md)                                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Guida alla ricerca**](a-searchguide.md)                                            | Falso     | **Unità organizzativa**         |
| [**Vedere anche**](a-seealso.md)                                                    | Falso     | **Unità organizzativa**         |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Stato-o-provincia-nome**](a-st.md)                                           | Falso     | **Unità organizzativa**         |
| [**Indirizzo via**](a-street.md)                                               | Falso     | **Unità organizzativa**         |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riferimenti secondari**](a-subrefs.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Numero di telefono**](a-telephonenumber.md)                                    | Falso     | **Unità organizzativa**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)               | Falso     | **Unità organizzativa**         |
| [**Numero telex**](a-telexnumber.md)                                            | Falso     | **Unità organizzativa**         |
| [**Testo-paese**](a-co.md)                                                     | Falso     | **Unità organizzativa**         |
| [**Suffissi UPN**](a-upnsuffixes.md)                                            | Falso     | **Unità organizzativa**         |
| [**Password utente**](a-userpassword.md)                                          | Falso     | **Unità organizzativa**         |
| [**USN-modificato**](a-usnchanged.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN creato**](a-usncreated.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-tra siti**](a-usnintersite.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-origine**](a-usnsource.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**WBEM-percorso**](a-wbempath.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando-modificato**](a-whenchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Data di creazione**](a-whencreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-pagina-altro**](a-url.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**X121-indirizzo**](a-x121address.md)                                            | Falso     | **Unità organizzativa**         |



## <a name="windows-server-2008-r2-extended-rights"></a>Diritti estesi di Windows Server 2008 R2

Questa classe contiene i seguenti diritti estesi per Windows Server 2008 R2:



| Nome comune                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generazione-RSoP-registrazione**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributes (Attributi)](#windows-server-2012-attributes)
-   [Diritti estesi](#windows-server-2012-extended-rights)



| Voce | Valore |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-att-ID                  | [**Nome-unità-organizzativa**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Possibili superiori          | [**Dominio-organizzazione DNS**](c-domaindns.md)**-unità organizzativa**[](c-organization.md)[](c-country.md)                                                                                                                                                                                                                                                    |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (OA;; CCDC; bf967a86-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aba-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967a9c-0de6-11D0-A285-00aa003049e2;; AO) (OA;; CCDC; bf967aa8-0de6-11D0-A285-00aa003049e2;; PO) (A;; RPLCLORC;;; AU) (A;; LCRPLORC;;; ED) (OA;; CCDC; 4828CC14-1437-45bc-9B07-AD6F015E5F28;; Ao |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2012-attributes"></a>Attributi di Windows Server 2012

Questa classe contiene gli attributi seguenti per Windows Server 2012:



| Attributo                                                                                    | Obbligatorio | Derivato da                    |
|----------------------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria aziendale**](a-businesscategory.md)                                              | Falso     | **Unità organizzativa**         |
| [**Nome canonico**](a-canonicalname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Codice paese**](a-countrycode.md)                                                        | Falso     | **Unità organizzativa**         |
| [**Nome paese**](a-c.md)                                                                  | Falso     | **Unità organizzativa**         |
| [**Creazione timestamp**](a-createtimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Gruppo predefinito**](a-defaultgroup.md)                                                      | Falso     | **Unità organizzativa**         |
| [**Descrizione**](a-description.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Profilo desktop**](a-desktopprofile.md)                                                  | Falso     | **Unità organizzativa**         |
| [**Indicatore di destinazione**](a-destinationindicator.md)                                      | Falso     | **Unità organizzativa**         |
| [**Nome visualizzato**](a-displayname.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**DSA-firma**](a-dsasignature.md)                                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome estensione**](a-extensionname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Fax-telefono-numero**](a-facsimiletelephonenumber.md)                             | Falso     | **Unità organizzativa**         |
| [**Bandiere**](a-flags.md)                                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da-entry**](a-fromentry.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**GP-collegamento**](a-gplink.md)                                                                  | Falso     | **Unità organizzativa**         |
| [**GP-opzioni**](a-gpoptions.md)                                                            | Falso     | **Unità organizzativa**         |
| [**Tipo di istanza**](a-instancetype.md)                                                      | Vero      | [**In alto**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                               | Falso     | **Unità organizzativa**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Viene eliminato**](a-isdeleted.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-member-of-DL**](a-memberof.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riciclato**](a-isrecycled.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome località**](a-l.md)                                                                 | Falso     | **Unità organizzativa**         |
| [**Logo**](a-thumbnaillogo.md)                                                              | Falso     | **Unità organizzativa**         |
| [**Gestito da**](a-managedby.md)                                                            | Falso     | **Unità organizzativa**         |
| [**Oggetti gestiti**](a-managedobjects.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-by**](a-masteredby.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)                          | Falso     | **Unità organizzativa**         |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Claim-shares-possible-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Enabled-feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-host-Service-account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-primary-computer-for**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-ultimo-noto-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-locale-effettivo-eliminazione-ora**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-local-effective-riciclo-tempo**](a-msds-localeffectiverecycletime.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-TDO-uscita-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-TDO-ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-valore-tipo-riferimento-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                                     | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria oggetto**](a-objectcategory.md)                                                  | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe Object**](a-objectclass.md)                                                        | Vero      | [**In alto**](c-top.md)<br/> |
| [**GUID oggetto**](a-objectguid.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome-unità-organizzativa**](a-ou.md)                                                     | Vero      | **Unità organizzativa**         |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Set di attributi parziali**](a-partialattributeset.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)                        | Falso     | **Unità organizzativa**         |
| [**Possibili-inferiori**](a-possibleinferiors.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo postale**](a-postaladdress.md)                                                    | Falso     | **Unità organizzativa**         |
| [**Codice postale**](a-postalcode.md)                                                          | Falso     | **Unità organizzativa**         |
| [**Casella Post-Office**](a-postofficebox.md)                                                   | Falso     | **Unità organizzativa**         |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)                               | Falso     | **Unità organizzativa**         |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-criteri-BL**](a-querypolicybl.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo registrato**](a-registeredaddress.md)                                            | Falso     | **Unità organizzativa**         |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-da**](a-repsfrom.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da Reps a**](a-repsto.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Guida alla ricerca**](a-searchguide.md)                                                        | Falso     | **Unità organizzativa**         |
| [**Vedere anche**](a-seealso.md)                                                                | Falso     | **Unità organizzativa**         |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Stato-o-provincia-nome**](a-st.md)                                                       | Falso     | **Unità organizzativa**         |
| [**Indirizzo via**](a-street.md)                                                           | Falso     | **Unità organizzativa**         |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riferimenti secondari**](a-subrefs.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Numero di telefono**](a-telephonenumber.md)                                                | Falso     | **Unità organizzativa**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)                           | Falso     | **Unità organizzativa**         |
| [**Numero telex**](a-telexnumber.md)                                                        | Falso     | **Unità organizzativa**         |
| [**Testo-paese**](a-co.md)                                                                 | Falso     | **Unità organizzativa**         |
| [**Suffissi UPN**](a-upnsuffixes.md)                                                        | Falso     | **Unità organizzativa**         |
| [**Password utente**](a-userpassword.md)                                                      | Falso     | **Unità organizzativa**         |
| [**USN-modificato**](a-usnchanged.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN creato**](a-usncreated.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-tra siti**](a-usnintersite.md)                                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-origine**](a-usnsource.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**WBEM-percorso**](a-wbempath.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando-modificato**](a-whenchanged.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Data di creazione**](a-whencreated.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-pagina-altro**](a-url.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**X121-indirizzo**](a-x121address.md)                                                        | Falso     | **Unità organizzativa**         |



## <a name="windows-server-2012-extended-rights"></a>Diritti estesi di Windows Server 2012

Questa classe contiene i seguenti diritti estesi per Windows Server 2012:



| Nome comune                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generazione-RSoP-registrazione**](r-generate-rsop-logging.md)   |



 

 





