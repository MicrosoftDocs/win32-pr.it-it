---
title: Organizational-Person classe
description: Questa classe viene utilizzata per gli oggetti che contengono informazioni organizzative su un utente, ad esempio il numero del dipendente, il reparto, il responsabile, la posizione, l'indirizzo dell'ufficio e così via.
ms.assetid: dbcecb0d-e7ab-4005-82ad-5ffe9b06a380
ms.tgt_platform: multiple
keywords:
- Organizational-Person schema AD della classe
- Schema AD della classe organizationalPerson
topic_type:
- apiref
api_name:
- Organizational-Person
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba9be35cfca3d08336c8b75bcb9a7f21fc2139e835fc6b74686e7f1e0a8a4202
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753201"
---
# <a name="organizational-person-class"></a>Organizational-Person classe

Questa classe viene utilizzata per gli oggetti che contengono informazioni organizzative su un utente, ad esempio il numero del dipendente, il reparto, il responsabile, la posizione, l'indirizzo dell'ufficio e così via.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Organizational-Person                |
| Ldap-Display-Name | organizationalPerson                 |
| Aggiorna privilegio  | Chiunque può aggiornare questo oggetto.       |
| Frequenza di aggiornamento  | \-                                   |
| Schema-Id-Guid    | bf967aa4-0de6-11d0-a285-00aa003049e2 |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attributes (Attributi)](#windows-2000-server-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | [**Persona**](c-person.md)<br/>                                                        |
| Governs-Id                  | 2.5.6.7                                                                                      |
| Default-Hiding-Value        | 0                                                                                            |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | [**Persona**](c-person.md)<br/>                                                        |
| Possibili superiori          | [**Contenitore**](c-container.md)                                                             |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; Au) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>attributi Windows server di Windows 2000

Questa classe contiene gli attributi seguenti per Windows 2000 Server:



| Attributo                                                                 | Obbligatorio | Derivato da                                                          |
|---------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Indirizzo**](a-streetaddress.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Indirizzo-Home**](a-homepostaladdress.md)                               | Falso     | **Organizational-Person**                                             |
| [**Descrizione dell'amministratore**](a-admindescription.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Attributi consentiti**](a-allowedattributes.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Assistente**](a-assistant.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Canonical-Name**](a-canonicalname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Nome comune**](a-cn.md)                                               | Vero      | [**Persona**](c-person.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Company**](a-company.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Codice paese**](a-countrycode.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Nome paese**](a-c.md)                                               | Falso     | **Organizational-Person**                                             |
| [**Create-Time-Stamp**](a-createtimestamp.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Dipartimento**](a-department.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Descrizione**](a-description.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indicatore di destinazione**](a-destinationindicator.md)                   | Falso     | **Organizational-Person**                                             |
| [**Nome visualizzato**](a-displayname.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Display-Name-Printable**](a-displaynameprintable.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Divisione**](a-division.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Firma DSA**](a-dsasignature.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzi di posta elettronica**](a-mail.md)                                        | Falso     | **Organizational-Person**                                             |
| [**ID dipendente**](a-employeeid.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Extension-Name**](a-extensionname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)          | Falso     | **Organizational-Person**                                             |
| [**Bandiere**](a-flags.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**From-Entry**](a-fromentry.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Qualificatore di generazione**](a-generationqualifier.md)                     | Falso     | **Organizational-Person**                                             |
| [**Nome specificato**](a-givenname.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Iniziali**](a-initials.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Tipo di istanza**](a-instancetype.md)                                   | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)            | Falso     | **Organizational-Person**                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Is-Deleted**](a-isdeleted.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Is-Member-Of-DL**](a-memberof.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Titolare di privilegi is**](a-isprivilegeholder.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Locality-Name**](a-l.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Logo**](a-thumbnaillogo.md)                                           | Falso     | **Organizational-Person**                                             |
| [**Oggetti gestiti**](a-managedobjects.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Mastered-By**](a-masteredby.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Modifica timestamp**](a-modifytimestamp.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Categoria di oggetti**](a-objectcategory.md)                               | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Classe object**](a-objectclass.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Object-Guid**](a-objectguid.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Versione oggetto**](a-objectversion.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Organizational-Unit-Name**](a-ou.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Nome organizzazione**](a-o.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Altre cassette postali**](a-othermailbox.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Other-Name**](a-middlename.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md) | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Titolo personale**](a-personaltitle.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Telefono-Fax-Other**](a-otherfacsimiletelephonenumber.md)                | Falso     | **Organizational-Person**                                             |
| [**Telefono-Home-Other**](a-otherhomephone.md)                              | Falso     | **Organizational-Person**                                             |
| [**Telefono-Home-Primary**](a-homephone.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Telefono-Ip-Other**](a-otheripphone.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Telefono-Ip-Primary**](a-ipphone.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Telefono-ISDN-Primary**](a-primaryinternationalisdnnumber.md)            | Falso     | **Organizational-Person**                                             |
| [**Telefono-Mobile-Other**](a-othermobile.md)                               | Falso     | **Organizational-Person**                                             |
| [**Telefono-Mobile-Primary**](a-mobile.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Telefono-Office-Other**](a-othertelephone.md)                            | Falso     | **Organizational-Person**                                             |
| [**Telefono-Pager-Other**](a-otherpager.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Telefono-Pager-Primary**](a-pager.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)     | Falso     | **Organizational-Person**                                             |
| [**Immagine**](a-thumbnailphoto.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Possibili inevasi**](a-possibleinferiors.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzo postale**](a-postaladdress.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Codice postale**](a-postalcode.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                | Falso     | **Organizational-Person**                                             |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)            | Falso     | **Organizational-Person**                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzi proxy**](a-proxyaddresses.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Rdn**](a-name.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzo registrato**](a-registeredaddress.md)                         | Falso     | **Organizational-Person**                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Report**](a-directreports.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Reps-From**](a-repsfrom.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Reps-To**](a-repsto.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Revisione**](a-revision.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Vedere anche**](a-seealso.md)                                             | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**State-Or-Province-Name**](a-st.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Via**](a-street.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Sottori ref**](a-subrefs.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Cognome**](a-sn.md)                                                   | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Flag di sistema**](a-systemflags.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Numero di telefono**](a-telephonenumber.md)                             | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)        | Falso     | **Organizational-Person**                                             |
| [**Telex-Number**](a-telexnumber.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Telex-Primary**](a-primarytelexnumber.md)                             | Falso     | **Organizational-Person**                                             |
| [**Text-Country**](a-co.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Titolo**](a-title.md)                                                  | Falso     | **Organizational-Person**                                             |
| [**Commento utente**](a-comment.md)                                         | Falso     | **Organizational-Person**                                             |
| [**User-Password**](a-userpassword.md)                                   | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Modifica di USN**](a-usnchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Creato da USN**](a-usncreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Intersite**](a-usnintersite.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Source**](a-usnsource.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Wbem-Path**](a-wbempath.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Oggetti noti**](a-wellknownobjects.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Quando viene modificato**](a-whenchanged.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Quando viene creato**](a-whencreated.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Www-Home-Page**](a-wwwhomepage.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**WWW-Page-Other**](a-url.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**X121-Address**](a-x121address.md)                                     | Falso     | **Organizational-Person**                                             |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributes (Attributi)](#windows-server-2003-attributes)



| Voce | Valore |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Default-Object-Category     | [**Persona**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Default-Hiding-Value        | 1                                                                                                                         |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                    |
| Sottoclasse di                 | [**Persona**](c-person.md)<br/>                                                                                     |
| Possibili superiori          | [**Unità**](c-container.md)[**organizzativa dell'organizzazione**](c-organization.md)[**contenitore**](c-organizationalunit.md) |
| Classi ausiliarie           | \-                                                                                                                        |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                              |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; Au)                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2003-attributes"></a>Windows Attributi di Server 2003

Questa classe contiene gli attributi seguenti per Windows Server 2003:



| Attributo                                                                   | Obbligatorio | Derivato da                                                          |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Indirizzo**](a-streetaddress.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Indirizzo-Home**](a-homepostaladdress.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Admin-Description**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Assistente**](a-assistant.md)                                            | Falso     | **Organizational-Person**                                             |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Nome comune**](a-cn.md)                                                 | Vero      | [**Persona**](c-person.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Codice paese**](a-countrycode.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Nome paese**](a-c.md)                                                 | Falso     | **Organizational-Person**                                             |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Dipartimento**](a-department.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indicatore di destinazione**](a-destinationindicator.md)                     | Falso     | **Organizational-Person**                                             |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Divisione**](a-division.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzi di posta elettronica**](a-mail.md)                                          | Falso     | **Organizational-Person**                                             |
| [**ID dipendente**](a-employeeid.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Extension-Name**](a-extensionname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)            | Falso     | **Organizational-Person**                                             |
| [**Bandiere**](a-flags.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**From-Entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Qualificatore di generazione**](a-generationqualifier.md)                       | Falso     | **Organizational-Person**                                             |
| [**Given-Name**](a-givenname.md)                                           | Falso     | **Organizational-Person**                                             |
| [**houseIdentifier**](a-houseidentifier.md)                                | Falso     | **Organizational-Person**                                             |
| [**Iniziali**](a-initials.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | **Organizational-Person**                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Titolare di privilegi is**](a-isprivilegeholder.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Locality-Name**](a-l.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Logo**](a-thumbnaillogo.md)                                             | Falso     | **Organizational-Person**                                             |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Modifica timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Allowed-To-Delegate-To**](a-msds-allowedtodelegateto.md)          | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | Falso     | **Organizational-Person**                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Categoria di oggetti**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Classe object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Guid oggetto**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Nome unità organizzativa**](a-ou.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Nome organizzazione**](a-o.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Altre cassette postali**](a-othermailbox.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Altro nome**](a-middlename.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Titolo personale**](a-personaltitle.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefono-Fax-Other**](a-otherfacsimiletelephonenumber.md)                  | Falso     | **Organizational-Person**                                             |
| [**Telefono-Home-Other**](a-otherhomephone.md)                                | Falso     | **Organizational-Person**                                             |
| [**Telefono-Home-Primary**](a-homephone.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefono-Ip-Other**](a-otheripphone.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Telefono-Ip-Primary**](a-ipphone.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Telefono-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | Falso     | **Organizational-Person**                                             |
| [**Telefono-Mobile-Other**](a-othermobile.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Telefono-Mobile-Primary**](a-mobile.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Telefono-Office-Other**](a-othertelephone.md)                              | Falso     | **Organizational-Person**                                             |
| [**Telefono-Pager-Other**](a-otherpager.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefono-Pager-Primary**](a-pager.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falso     | **Organizational-Person**                                             |
| [**Immagine**](a-thumbnailphoto.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Possibili eserezioni**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzo postale**](a-postaladdress.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Codice postale**](a-postalcode.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)              | Falso     | **Organizational-Person**                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Rdn**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzo registrato**](a-registeredaddress.md)                           | Falso     | **Organizational-Person**                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Report**](a-directreports.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Vedere anche**](a-seealso.md)                                               | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Numero di serie**](a-serialnumber.md)                                     | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**State-Or-Province-Name**](a-st.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Via**](a-street.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Classe structural-object**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Sottori ref**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Cognome**](a-sn.md)                                                     | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Numero di telefono**](a-telephonenumber.md)                               | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falso     | **Organizational-Person**                                             |
| [**Telex-Number**](a-telexnumber.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Telex-Primary**](a-primarytelexnumber.md)                               | Falso     | **Organizational-Person**                                             |
| [**Text-Country**](a-co.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Titolo**](a-title.md)                                                    | Falso     | **Organizational-Person**                                             |
| [**Commento utente**](a-comment.md)                                           | Falso     | **Organizational-Person**                                             |
| [**User-Password**](a-userpassword.md)                                     | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Modifica di USN**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Creato da USN**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Quando viene modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Quando viene creato**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Www-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**X121-Address**](a-x121address.md)                                       | Falso     | **Organizational-Person**                                             |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributes (Attributi)](#windows-server-2003-r2-attributes)



| Voce | Valore |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Default-Object-Category     | [**Persona**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Default-Hiding-Value        | 1                                                                                                                         |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                    |
| Sottoclasse di                 | [**Persona**](c-person.md)<br/>                                                                                     |
| Possibili superiori          | [**Unità**](c-container.md)[**organizzativa dell'organizzazione**](c-organization.md)[**contenitore**](c-organizationalunit.md) |
| Classi ausiliarie           | \-                                                                                                                        |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                              |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; Au)                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2003-r2-attributes"></a>Windows Attributi di Server 2003 R2

Questa classe contiene gli attributi seguenti per Windows Server 2003 R2:



| Attributo                                                                   | Obbligatorio | Derivato da                                                          |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Indirizzo**](a-streetaddress.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Indirizzo-Home**](a-homepostaladdress.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Admin-Description**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Assistente**](a-assistant.md)                                            | Falso     | **Organizational-Person**                                             |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Nome comune**](a-cn.md)                                                 | Vero      | [**Persona**](c-person.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Codice paese**](a-countrycode.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Nome paese**](a-c.md)                                                 | Falso     | **Organizational-Person**                                             |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Dipartimento**](a-department.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indicatore di destinazione**](a-destinationindicator.md)                     | Falso     | **Organizational-Person**                                             |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Divisione**](a-division.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzi di posta elettronica**](a-mail.md)                                          | Falso     | **Organizational-Person**                                             |
| [**ID dipendente**](a-employeeid.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Extension-Name**](a-extensionname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)            | Falso     | **Organizational-Person**                                             |
| [**Bandiere**](a-flags.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**From-Entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Qualificatore di generazione**](a-generationqualifier.md)                       | Falso     | **Organizational-Person**                                             |
| [**Nome specificato**](a-givenname.md)                                           | Falso     | **Organizational-Person**                                             |
| [**houseIdentifier**](a-houseidentifier.md)                                | Falso     | **Organizational-Person**                                             |
| [**Iniziali**](a-initials.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | **Organizational-Person**                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Titolare di privilegi is**](a-isprivilegeholder.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Locality-Name**](a-l.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Logo**](a-thumbnaillogo.md)                                             | Falso     | **Organizational-Person**                                             |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Modifica timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Allowed-To-Delegate-To**](a-msds-allowedtodelegateto.md)          | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                 | Falso     | **Organizational-Person**                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Categoria di oggetti**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Classe object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Guid oggetto**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Nome unità organizzativa**](a-ou.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Nome organizzazione**](a-o.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Altre cassette postali**](a-othermailbox.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Altro nome**](a-middlename.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Titolo personale**](a-personaltitle.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefono-Fax-Other**](a-otherfacsimiletelephonenumber.md)                  | Falso     | **Organizational-Person**                                             |
| [**Telefono-Home-Other**](a-otherhomephone.md)                                | Falso     | **Organizational-Person**                                             |
| [**Telefono-Home-Primary**](a-homephone.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefono-Ip-Other**](a-otheripphone.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Telefono-Ip-Primary**](a-ipphone.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Telefono-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | Falso     | **Organizational-Person**                                             |
| [**Telefono-Mobile-Other**](a-othermobile.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Telefono-Mobile-Primary**](a-mobile.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Telefono-Office-Other**](a-othertelephone.md)                              | Falso     | **Organizational-Person**                                             |
| [**Telefono-Pager-Other**](a-otherpager.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefono-Pager-Primary**](a-pager.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falso     | **Organizational-Person**                                             |
| [**Immagine**](a-thumbnailphoto.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Possibili eserezioni**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzo postale**](a-postaladdress.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Codice postale**](a-postalcode.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)              | Falso     | **Organizational-Person**                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Rdn**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzo registrato**](a-registeredaddress.md)                           | Falso     | **Organizational-Person**                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Report**](a-directreports.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Vedere anche**](a-seealso.md)                                               | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Numero di serie**](a-serialnumber.md)                                     | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**State-Or-Province-Name**](a-st.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Via**](a-street.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Classe structural-object**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Sottori ref**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Cognome**](a-sn.md)                                                     | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Numero di telefono**](a-telephonenumber.md)                               | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falso     | **Organizational-Person**                                             |
| [**Telex-Number**](a-telexnumber.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Telex-Primary**](a-primarytelexnumber.md)                               | Falso     | **Organizational-Person**                                             |
| [**Text-Country**](a-co.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Titolo**](a-title.md)                                                    | Falso     | **Organizational-Person**                                             |
| [**Commento utente**](a-comment.md)                                           | Falso     | **Organizational-Person**                                             |
| [**User-Password**](a-userpassword.md)                                     | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Modifica di USN**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Creato da USN**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Quando viene modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Quando viene creato**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Www-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**X121-Address**](a-x121address.md)                                       | Falso     | **Organizational-Person**                                             |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributes (Attributi)](#windows-server-2008-attributes)



| Voce | Valore |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Default-Object-Category     | [**Persona**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Default-Hiding-Value        | 1                                                                                                                         |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                    |
| Sottoclasse di                 | [**Persona**](c-person.md)<br/>                                                                                     |
| Possibili superiori          | [**Unità**](c-container.md)[**organizzativa dell'organizzazione**](c-organization.md)[**contenitore**](c-organizationalunit.md) |
| Classi ausiliarie           | \-                                                                                                                        |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                              |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; Au)                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2008-attributes"></a>Windows Attributi di Server 2008

Questa classe contiene gli attributi seguenti per Windows Server 2008:



| Attributo                                                                      | Obbligatorio | Derivato da                                                          |
|--------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Indirizzo**](a-streetaddress.md)                                             | Falso     | **Organizational-Person**                                             |
| [**Indirizzo-Home**](a-homepostaladdress.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Admin-Description**](a-admindescription.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Attributi consentiti**](a-allowedattributes.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Assistente**](a-assistant.md)                                               | Falso     | **Organizational-Person**                                             |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)       | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Canonical-Name**](a-canonicalname.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Nome comune**](a-cn.md)                                                    | Vero      | [**Persona**](c-person.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                   | Falso     | **Organizational-Person**                                             |
| [**Codice paese**](a-countrycode.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Nome paese**](a-c.md)                                                    | Falso     | **Organizational-Person**                                             |
| [**Creazione timestamp**](a-createtimestamp.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Dipartimento**](a-department.md)                                             | Falso     | **Organizational-Person**                                             |
| [**Descrizione**](a-description.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indicatore di destinazione**](a-destinationindicator.md)                        | Falso     | **Organizational-Person**                                             |
| [**Nome visualizzato**](a-displayname.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Display-Name-Printable**](a-displaynameprintable.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Divisione**](a-division.md)                                                 | Falso     | **Organizational-Person**                                             |
| [**Firma DSA**](a-dsasignature.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzi di posta elettronica**](a-mail.md)                                             | Falso     | **Organizational-Person**                                             |
| [**ID dipendente**](a-employeeid.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Extension-Name**](a-extensionname.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)               | Falso     | **Organizational-Person**                                             |
| [**Bandiere**](a-flags.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**From-Entry**](a-fromentry.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Qualificatore di generazione**](a-generationqualifier.md)                          | Falso     | **Organizational-Person**                                             |
| [**Given-Name**](a-givenname.md)                                              | Falso     | **Organizational-Person**                                             |
| [**houseIdentifier**](a-houseidentifier.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Iniziali**](a-initials.md)                                                 | Falso     | **Organizational-Person**                                             |
| [**Tipo di istanza**](a-instancetype.md)                                        | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                 | Falso     | **Organizational-Person**                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Is-Deleted**](a-isdeleted.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Membro di DL**](a-memberof.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Titolare dei privilegi**](a-isprivilegeholder.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Locality-Name**](a-l.md)                                                   | Falso     | **Organizational-Person**                                             |
| [**Logo**](a-thumbnaillogo.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Oggetti gestiti**](a-managedobjects.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                   | Falso     | **Organizational-Person**                                             |
| [**Mastered-By**](a-masteredby.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Modifica timestamp**](a-modifytimestamp.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Allowed-To-Delegate-To**](a-msds-allowedtodelegateto.md)             | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-HAB-Seniority-Index**](a-msds-habseniorityindex.md)                  | Falso     | **Organizational-Person**                                             |
| [**ms-DS-is-Domain-For**](a-msds-isdomainfor.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)              | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                 | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)              | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                  | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                    | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                    | Falso     | **Organizational-Person**                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Categoria di oggetti**](a-objectcategory.md)                                    | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Classe object**](a-objectclass.md)                                          | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Object-Guid**](a-objectguid.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Versione oggetto**](a-objectversion.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Organizational-Unit-Name**](a-ou.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Nome organizzazione**](a-o.md)                                               | Falso     | **Organizational-Person**                                             |
| [**Altre cassette postali**](a-othermailbox.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Other-Name**](a-middlename.md)                                             | Falso     | **Organizational-Person**                                             |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Titolo personale**](a-personaltitle.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Telefono-Fax-Other**](a-otherfacsimiletelephonenumber.md)                     | Falso     | **Organizational-Person**                                             |
| [**Telefono-Home-Other**](a-otherhomephone.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefono-Home-Primary**](a-homephone.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Telefono-Ip-Other**](a-otheripphone.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Telefono-Ip-Primary**](a-ipphone.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Telefono-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                 | Falso     | **Organizational-Person**                                             |
| [**Telefono-Mobile-Other**](a-othermobile.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Telefono-Mobile-Primary**](a-mobile.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Telefono-Office-Other**](a-othertelephone.md)                                 | Falso     | **Organizational-Person**                                             |
| [**Telefono-Pager-Other**](a-otherpager.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Telefono-Pager-Primary**](a-pager.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)          | Falso     | **Organizational-Person**                                             |
| [**Immagine**](a-thumbnailphoto.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Possibili eserezioni**](a-possibleinferiors.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzo postale**](a-postaladdress.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Codice postale**](a-postalcode.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)                 | Falso     | **Organizational-Person**                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Rdn**](a-name.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzo registrato**](a-registeredaddress.md)                              | Falso     | **Organizational-Person**                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Report**](a-directreports.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Reps-From**](a-repsfrom.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Reps-To**](a-repsto.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Revisione**](a-revision.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Vedere anche**](a-seealso.md)                                                  | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Numero di serie**](a-serialnumber.md)                                        | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**State-or-Province-Name**](a-st.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Via e indirizzo**](a-street.md)                                             | Falso     | **Organizational-Person**                                             |
| [**Classe structural-object**](a-structuralobjectclass.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Sottori ref**](a-subrefs.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Cognome**](a-sn.md)                                                        | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Flag di sistema**](a-systemflags.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Numero di telefono**](a-telephonenumber.md)                                  | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)             | Falso     | **Organizational-Person**                                             |
| [**Telex-Number**](a-telexnumber.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Telex-Primary**](a-primarytelexnumber.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Text-Country**](a-co.md)                                                   | Falso     | **Organizational-Person**                                             |
| [**Titolo**](a-title.md)                                                       | Falso     | **Organizational-Person**                                             |
| [**Commento utente**](a-comment.md)                                              | Falso     | **Organizational-Person**                                             |
| [**User-Password**](a-userpassword.md)                                        | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Modifica di USN**](a-usnchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Creato da USN**](a-usncreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Intersite**](a-usnintersite.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Source**](a-usnsource.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Wbem-Path**](a-wbempath.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Oggetti noti**](a-wellknownobjects.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Quando viene modificato**](a-whenchanged.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Quando viene creato**](a-whencreated.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Www-Home-Page**](a-wwwhomepage.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**WWW-Page-Other**](a-url.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**X121-Address**](a-x121address.md)                                          | Falso     | **Organizational-Person**                                             |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributes (Attributi)](#windows-server-2008-r2-attributes)



| Voce | Valore |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Default-Object-Category     | [**Persona**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Default-Hiding-Value        | 1                                                                                                                         |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                    |
| Sottoclasse di                 | [**Persona**](c-person.md)<br/>                                                                                     |
| Possibili superiori          | [**Unità**](c-container.md)[**organizzativa dell'organizzazione**](c-organization.md)[**contenitore**](c-organizationalunit.md) |
| Classi ausiliarie           | \-                                                                                                                        |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                              |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; Au)                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2008-r2-attributes"></a>Windows Attributi di Server 2008 R2

Questa classe contiene gli attributi seguenti per Windows Server 2008 R2:



| Attributo                                                                        | Obbligatorio | Derivato da                                                          |
|----------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Indirizzo**](a-streetaddress.md)                                               | Falso     | **Organizational-Person**                                             |
| [**Indirizzo-Home**](a-homepostaladdress.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Descrizione dell'amministratore**](a-admindescription.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Attributi consentiti**](a-allowedattributes.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Assistente**](a-assistant.md)                                                 | Falso     | **Organizational-Person**                                             |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)         | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Canonical-Name**](a-canonicalname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Nome comune**](a-cn.md)                                                      | Vero      | [**Persona**](c-person.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                     | Falso     | **Organizational-Person**                                             |
| [**Codice paese**](a-countrycode.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Nome paese**](a-c.md)                                                      | Falso     | **Organizational-Person**                                             |
| [**Creazione timestamp**](a-createtimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Dipartimento**](a-department.md)                                               | Falso     | **Organizational-Person**                                             |
| [**Descrizione**](a-description.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indicatore di destinazione**](a-destinationindicator.md)                          | Falso     | **Organizational-Person**                                             |
| [**Nome visualizzato**](a-displayname.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Divisione**](a-division.md)                                                   | Falso     | **Organizational-Person**                                             |
| [**Firma DSA**](a-dsasignature.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzi di posta elettronica**](a-mail.md)                                               | Falso     | **Organizational-Person**                                             |
| [**ID dipendente**](a-employeeid.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Extension-Name**](a-extensionname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)                 | Falso     | **Organizational-Person**                                             |
| [**Bandiere**](a-flags.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**From-Entry**](a-fromentry.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Qualificatore di generazione**](a-generationqualifier.md)                            | Falso     | **Organizational-Person**                                             |
| [**Given-Name**](a-givenname.md)                                                | Falso     | **Organizational-Person**                                             |
| [**houseIdentifier**](a-houseidentifier.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Iniziali**](a-initials.md)                                                   | Falso     | **Organizational-Person**                                             |
| [**Tipo di istanza**](a-instancetype.md)                                          | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                   | Falso     | **Organizational-Person**                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Membro di DL**](a-memberof.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Titolare dei privilegi**](a-isprivilegeholder.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Viene riciclato**](a-isrecycled.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Locality-Name**](a-l.md)                                                     | Falso     | **Organizational-Person**                                             |
| [**Logo**](a-thumbnaillogo.md)                                                  | Falso     | **Organizational-Person**                                             |
| [**Oggetti gestiti**](a-managedobjects.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                     | Falso     | **Organizational-Person**                                             |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Modifica timestamp**](a-modifytimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Allowed-To-Delegate-To**](a-msds-allowedtodelegateto.md)               | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-HAB-Seniority-Index**](a-msds-habseniorityindex.md)                    | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)                | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                   | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                    | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                      | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                      | Falso     | **Organizational-Person**                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Categoria di oggetti**](a-objectcategory.md)                                      | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Classe object**](a-objectclass.md)                                            | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Guid oggetto**](a-objectguid.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Versione oggetto**](a-objectversion.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Nome unità organizzativa**](a-ou.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Nome organizzazione**](a-o.md)                                                 | Falso     | **Organizational-Person**                                             |
| [**Altre cassette postali**](a-othermailbox.md)                                          | Falso     | **Organizational-Person**                                             |
| [**Altro nome**](a-middlename.md)                                               | Falso     | **Organizational-Person**                                             |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Titolo personale**](a-personaltitle.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Telefono-Fax-Other**](a-otherfacsimiletelephonenumber.md)                       | Falso     | **Organizational-Person**                                             |
| [**Telefono-Home-Other**](a-otherhomephone.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Telefono-Home-Primary**](a-homephone.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Telefono-Ip-Other**](a-otheripphone.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Telefono-Ip-Primary**](a-ipphone.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Telefono-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                   | Falso     | **Organizational-Person**                                             |
| [**Telefono-Mobile-Other**](a-othermobile.md)                                      | Falso     | **Organizational-Person**                                             |
| [**Telefono-Mobile-Primary**](a-mobile.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Telefono-Office-Other**](a-othertelephone.md)                                   | Falso     | **Organizational-Person**                                             |
| [**Telefono-Pager-Other**](a-otherpager.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Telefono-Pager-Primary**](a-pager.md)                                           | Falso     | **Organizational-Person**                                             |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)            | Falso     | **Organizational-Person**                                             |
| [**Immagine**](a-thumbnailphoto.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Possibili eserezioni**](a-possibleinferiors.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzo postale**](a-postaladdress.md)                                        | Falso     | **Organizational-Person**                                             |
| [**Codice postale**](a-postalcode.md)                                              | Falso     | **Organizational-Person**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)                   | Falso     | **Organizational-Person**                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Rdn**](a-name.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzo registrato**](a-registeredaddress.md)                                | Falso     | **Organizational-Person**                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Report**](a-directreports.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Reps-From**](a-repsfrom.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Reps-To**](a-repsto.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Revisione**](a-revision.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Vedere anche**](a-seealso.md)                                                    | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Numero di serie**](a-serialnumber.md)                                          | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**State-or-Province-Name**](a-st.md)                                           | Falso     | **Organizational-Person**                                             |
| [**Via e indirizzo**](a-street.md)                                               | Falso     | **Organizational-Person**                                             |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Riferimenti secondari**](a-subrefs.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Cognome**](a-sn.md)                                                          | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Flag di sistema**](a-systemflags.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Numero di telefono**](a-telephonenumber.md)                                    | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)               | Falso     | **Organizational-Person**                                             |
| [**Telex-Number**](a-telexnumber.md)                                            | Falso     | **Organizational-Person**                                             |
| [**Telex-Primary**](a-primarytelexnumber.md)                                    | Falso     | **Organizational-Person**                                             |
| [**Text-Country**](a-co.md)                                                     | Falso     | **Organizational-Person**                                             |
| [**Titolo**](a-title.md)                                                         | Falso     | **Organizational-Person**                                             |
| [**Commento utente**](a-comment.md)                                                | Falso     | **Organizational-Person**                                             |
| [**User-Password**](a-userpassword.md)                                          | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Modifica di USN**](a-usnchanged.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Creato da USN**](a-usncreated.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Intersite**](a-usnintersite.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Oggetti noti**](a-wellknownobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Quando viene modificato**](a-whenchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Quando viene creato**](a-whencreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Www-Home-Page**](a-wwwhomepage.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**X121-Address**](a-x121address.md)                                            | Falso     | **Organizational-Person**                                             |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributes (Attributi)](#windows-server-2012-attributes)



| Voce | Valore |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| Default-Object-Category     | [**Persona**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| Default-Hiding-Value        | 1                                                                                                                         |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                    |
| Sottoclasse di                 | [**Persona**](c-person.md)<br/>                                                                                     |
| Possibili superiori          | [**Unità**](c-container.md)[**organizzativa dell'organizzazione**](c-organization.md)[**contenitore**](c-organizationalunit.md) |
| Classi ausiliarie           | \-                                                                                                                        |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                              |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;; Au)                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attributi

Questa classe contiene gli attributi seguenti per Windows Server 2012:



| Attributo                                                                                              | Obbligatorio | Derivato da                                                          |
|--------------------------------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Indirizzo**](a-streetaddress.md)                                                                     | Falso     | **Organizational-Person**                                             |
| [**Indirizzo-Home**](a-homepostaladdress.md)                                                            | Falso     | **Organizational-Person**                                             |
| [**Admin-Description**](a-admindescription.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Admin-Display-Name**](a-admindisplayname.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Attributi consentiti**](a-allowedattributes.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Assistente**](a-assistant.md)                                                                       | Falso     | **Organizational-Person**                                             |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)                               | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Canonical-Name**](a-canonicalname.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Nome comune**](a-cn.md)                                                                            | Vero      | [**Persona**](c-person.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                                           | Falso     | **Organizational-Person**                                             |
| [**Codice paese**](a-countrycode.md)                                                                  | Falso     | **Organizational-Person**                                             |
| [**Nome paese**](a-c.md)                                                                            | Falso     | **Organizational-Person**                                             |
| [**Creazione timestamp**](a-createtimestamp.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Dipartimento**](a-department.md)                                                                     | Falso     | **Organizational-Person**                                             |
| [**Descrizione**](a-description.md)                                                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indicatore di destinazione**](a-destinationindicator.md)                                                | Falso     | **Organizational-Person**                                             |
| [**Nome visualizzato**](a-displayname.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Divisione**](a-division.md)                                                                         | Falso     | **Organizational-Person**                                             |
| [**Firma DSA**](a-dsasignature.md)                                                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzi di posta elettronica**](a-mail.md)                                                                     | Falso     | **Organizational-Person**                                             |
| [**ID dipendente**](a-employeeid.md)                                                                    | Falso     | **Organizational-Person**                                             |
| [**Extension-Name**](a-extensionname.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)                                       | Falso     | **Organizational-Person**                                             |
| [**Bandiere**](a-flags.md)                                                                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**From-Entry**](a-fromentry.md)                                                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Qualificatore di generazione**](a-generationqualifier.md)                                                  | Falso     | **Organizational-Person**                                             |
| [**Given-Name**](a-givenname.md)                                                                      | Falso     | **Organizational-Person**                                             |
| [**houseIdentifier**](a-houseidentifier.md)                                                           | Falso     | **Organizational-Person**                                             |
| [**Iniziali**](a-initials.md)                                                                         | Falso     | **Organizational-Person**                                             |
| [**Tipo di istanza**](a-instancetype.md)                                                                | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Is-Deleted**](a-isdeleted.md)                                                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Membro di DL**](a-memberof.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Titolare del privilegio**](a-isprivilegeholder.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Viene riciclato**](a-isrecycled.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Locality-Name**](a-l.md)                                                                           | Falso     | **Organizational-Person**                                             |
| [**Logo**](a-thumbnaillogo.md)                                                                        | Falso     | **Organizational-Person**                                             |
| [**Oggetti gestiti**](a-managedobjects.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                                           | Falso     | **Organizational-Person**                                             |
| [**Mastered-By**](a-masteredby.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MHS-OR-Address**](a-mhsoraddress.md)                                                               | Falso     | **Organizational-Person**                                             |
| [**Modifica timestamp**](a-modifytimestamp.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity**](a-msds-allowedtoactonbehalfofotheridentity.md) | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Allowed-To-Delegate-To**](a-msds-allowedtodelegateto.md)                                     | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md)           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-HAB-Seniority-Index**](a-msds-habseniorityindex.md)                                          | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Phonetic-Company-Name**](a-msds-phoneticcompanyname.md)                                      | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-Department**](a-msds-phoneticdepartment.md)                                         | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                                      | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-First-Name**](a-msds-phoneticfirstname.md)                                          | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Phonetic-Last-Name**](a-msds-phoneticlastname.md)                                            | Falso     | **Organizational-Person**                                             |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**ms-Exch-House-Identifier**](a-msexchhouseidentifier.md)                                            | Falso     | **Organizational-Person**                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                               | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                           | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Categoria di oggetti**](a-objectcategory.md)                                                            | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Classe object**](a-objectclass.md)                                                                  | Vero      | [**In alto**](c-top.md)<br/>                                       |
| [**Guid oggetto**](a-objectguid.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Versione oggetto**](a-objectversion.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Nome unità organizzativa**](a-ou.md)                                                               | Falso     | **Organizational-Person**                                             |
| [**Nome organizzazione**](a-o.md)                                                                       | Falso     | **Organizational-Person**                                             |
| [**Altre cassette postali**](a-othermailbox.md)                                                                | Falso     | **Organizational-Person**                                             |
| [**Altro nome**](a-middlename.md)                                                                     | Falso     | **Organizational-Person**                                             |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Titolo personale**](a-personaltitle.md)                                                              | Falso     | **Organizational-Person**                                             |
| [**Telefono-Fax-Other**](a-otherfacsimiletelephonenumber.md)                                             | Falso     | **Organizational-Person**                                             |
| [**Telefono-Home-Other**](a-otherhomephone.md)                                                           | Falso     | **Organizational-Person**                                             |
| [**Telefono-Home-Primary**](a-homephone.md)                                                              | Falso     | **Organizational-Person**                                             |
| [**Telefono-Ip-Other**](a-otheripphone.md)                                                               | Falso     | **Organizational-Person**                                             |
| [**Telefono-Ip-Primary**](a-ipphone.md)                                                                  | Falso     | **Organizational-Person**                                             |
| [**Telefono-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Telefono-Mobile-Other**](a-othermobile.md)                                                            | Falso     | **Organizational-Person**                                             |
| [**Telefono-Mobile-Primary**](a-mobile.md)                                                               | Falso     | **Organizational-Person**                                             |
| [**Telefono-Office-Other**](a-othertelephone.md)                                                         | Falso     | **Organizational-Person**                                             |
| [**Telefono-Pager-Other**](a-otherpager.md)                                                              | Falso     | **Organizational-Person**                                             |
| [**Telefono-Pager-Primary**](a-pager.md)                                                                 | Falso     | **Organizational-Person**                                             |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)                                  | Falso     | **Organizational-Person**                                             |
| [**Immagine**](a-thumbnailphoto.md)                                                                    | Falso     | **Organizational-Person**                                             |
| [**Possibili eserezioni**](a-possibleinferiors.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzo postale**](a-postaladdress.md)                                                              | Falso     | **Organizational-Person**                                             |
| [**Codice postale**](a-postalcode.md)                                                                    | Falso     | **Organizational-Person**                                             |
| [**Post-Office-Box**](a-postofficebox.md)                                                             | Falso     | **Organizational-Person**                                             |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)                                         | Falso     | **Organizational-Person**                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Rdn**](a-name.md)                                                                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Indirizzo registrato**](a-registeredaddress.md)                                                      | Falso     | **Organizational-Person**                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Report**](a-directreports.md)                                                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Reps-From**](a-repsfrom.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Reps-To**](a-repsto.md)                                                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Revisione**](a-revision.md)                                                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Vedere anche**](a-seealso.md)                                                                          | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Numero di serie**](a-serialnumber.md)                                                                | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                               | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**State-Or-Province-Name**](a-st.md)                                                                 | Falso     | **Organizational-Person**                                             |
| [**Via**](a-street.md)                                                                     | Falso     | **Organizational-Person**                                             |
| [**Classe structural-object**](a-structuralobjectclass.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Sottori ref**](a-subrefs.md)                                                                          | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Cognome**](a-sn.md)                                                                                | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Flag di sistema**](a-systemflags.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Numero di telefono**](a-telephonenumber.md)                                                          | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)                                     | Falso     | **Organizational-Person**                                             |
| [**Telex-Number**](a-telexnumber.md)                                                                  | Falso     | **Organizational-Person**                                             |
| [**Telex-Primary**](a-primarytelexnumber.md)                                                          | Falso     | **Organizational-Person**                                             |
| [**Text-Country**](a-co.md)                                                                           | Falso     | **Organizational-Person**                                             |
| [**Titolo**](a-title.md)                                                                               | Falso     | **Organizational-Person**                                             |
| [**Commento utente**](a-comment.md)                                                                      | Falso     | **Organizational-Person**                                             |
| [**User-Password**](a-userpassword.md)                                                                | Falso     | [**Persona**](c-person.md)<br/>                                 |
| [**Modifica di USN**](a-usnchanged.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Creato da USN**](a-usncreated.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Intersite**](a-usnintersite.md)                                                                | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**USN-Source**](a-usnsource.md)                                                                      | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Wbem-Path**](a-wbempath.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Oggetti noti**](a-wellknownobjects.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Quando viene modificato**](a-whenchanged.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Quando viene creato**](a-whencreated.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**Www-Home-Page**](a-wwwhomepage.md)                                                                 | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**WWW-Page-Other**](a-url.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/>                                       |
| [**X121-Address**](a-x121address.md)                                                                  | Falso     | **Organizational-Person**                                             |



 

 





