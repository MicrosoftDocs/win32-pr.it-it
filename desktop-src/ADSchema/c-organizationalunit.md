---
title: Organizational-Unit classe
description: Contenitore per l'archiviazione di utenti, computer e altri oggetti account.
ms.assetid: a5a99dc7-9000-478c-9545-473cfb6ddf6c
ms.tgt_platform: multiple
keywords:
- Organizational-Unit schema AD della classe
- Schema AD della classe organizationalUnit
topic_type:
- apiref
api_name:
- Organizational-Unit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79807cc71f5e7690aca04b80f0d5560399b8b5415fc1d7f3cf9654884b7b9c1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065291"
---
# <a name="organizational-unit-class"></a>Organizational-Unit classe

Contenitore per l'archiviazione di utenti, computer e altri oggetti account.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Organizational-Unit                  |
| Ldap-Display-Name | organizationalUnit                   |
| Privilegio di aggiornamento  | Chiunque può aggiornare questo oggetto.       |
| Frequenza di aggiornamento  | \-                                   |
| Schema-Id-Guid    | bf967aa5-0de6-11d0-a285-00aa003049e2 |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam-attributes)
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
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                        |
| Rdn-Att-Id                  | [**Organizational-Unit-Name**](a-ou.md)<br/>                                                                                                                                                                                                                                                      |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                          |
| Possibili superiori          | [**Domain-DNS**](c-domaindns.md)**Organizational-Unit**[**Organization**](c-organization.md)                                                                                                                                                                                                           |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                             |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;;; Au) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                               |



## <a name="windows-2000-server-attributes"></a>Windows 2000 Server Attributes

Questa classe contiene gli attributi seguenti per Windows 2000 Server:



| Attributo                                                                 | Obbligatorio | Derivato da                    |
|---------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Description**](a-admindescription.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria di business**](a-businesscategory.md)                           | Falso     | **Unità organizzativa**         |
| [**Canonical-Name**](a-canonicalname.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Codice paese**](a-countrycode.md)                                     | Falso     | **Unità organizzativa**         |
| [**Nome paese**](a-c.md)                                               | Falso     | **Unità organizzativa**         |
| [**Create-Time-Stamp**](a-createtimestamp.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Gruppo predefinito**](a-defaultgroup.md)                                   | Falso     | **Unità organizzativa**         |
| [**Descrizione**](a-description.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Profilo desktop**](a-desktopprofile.md)                               | Falso     | **Unità organizzativa**         |
| [**Indicatore di destinazione**](a-destinationindicator.md)                   | Falso     | **Unità organizzativa**         |
| [**Nome visualizzato**](a-displayname.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Extension-Name**](a-extensionname.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)          | Falso     | **Unità organizzativa**         |
| [**Bandiere**](a-flags.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Collegamento a Criteri di gruppo**](a-gplink.md)                                               | Falso     | **Unità organizzativa**         |
| [**Opzioni di Criteri di gruppo**](a-gpoptions.md)                                         | Falso     | **Unità organizzativa**         |
| [**Tipo di istanza**](a-instancetype.md)                                   | Vero      | [**In alto**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)            | Falso     | **Unità organizzativa**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Member-Of-DL**](a-memberof.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Titolare del privilegio Is**](a-isprivilegeholder.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                              | Falso     | **Unità organizzativa**         |
| [**Logo**](a-thumbnaillogo.md)                                           | Falso     | **Unità organizzativa**         |
| [**Gestito da**](a-managedby.md)                                         | Falso     | **Unità organizzativa**         |
| [**Oggetti gestiti**](a-managedobjects.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica timestamp**](a-modifytimestamp.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria di oggetti**](a-objectcategory.md)                               | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe object**](a-objectclass.md)                                     | Vero      | [**In alto**](c-top.md)<br/> |
| [**Guid oggetto**](a-objectguid.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome unità organizzativa**](a-ou.md)                                  | Vero      | **Unità organizzativa**         |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)     | Falso     | **Unità organizzativa**         |
| [**Possibili eserezioni**](a-possibleinferiors.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo postale**](a-postaladdress.md)                                 | Falso     | **Unità organizzativa**         |
| [**Codice postale**](a-postalcode.md)                                       | Falso     | **Unità organizzativa**         |
| [**Post-Office-Box**](a-postofficebox.md)                                | Falso     | **Unità organizzativa**         |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)            | Falso     | **Unità organizzativa**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo registrato**](a-registeredaddress.md)                         | Falso     | **Unità organizzativa**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Guida alla ricerca**](a-searchguide.md)                                     | Falso     | **Unità organizzativa**         |
| [**Vedere anche**](a-seealso.md)                                             | Falso     | **Unità organizzativa**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                    | Falso     | **Unità organizzativa**         |
| [**Via e indirizzo**](a-street.md)                                        | Falso     | **Unità organizzativa**         |
| [**Sottori ref**](a-subrefs.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Numero di telefono**](a-telephonenumber.md)                             | Falso     | **Unità organizzativa**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)        | Falso     | **Unità organizzativa**         |
| [**Telex-Number**](a-telexnumber.md)                                     | Falso     | **Unità organizzativa**         |
| [**Text-Country**](a-co.md)                                              | Falso     | **Unità organizzativa**         |
| [**SUFFISSI UPN**](a-upnsuffixes.md)                                     | Falso     | **Unità organizzativa**         |
| [**User-Password**](a-userpassword.md)                                   | Falso     | **Unità organizzativa**         |
| [**Modifica di USN**](a-usnchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creato da USN**](a-usncreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene modificato**](a-whenchanged.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene creato**](a-whencreated.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Www-Home-Page**](a-wwwhomepage.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**X121-Address**](a-x121address.md)                                     | Falso     | **Unità organizzativa**         |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributes (Attributi)](#windows-server-2003-attributes)
-   [Diritti estesi](#windows-server-2003-extended-rights)



| Voce | Valore |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| Rdn-Att-Id                  | [**Organizational-Unit-Name**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Possibili superiori          | [**Domain-DNS**](c-domaindns.md)**Organizational-Unit**[**Organization**](c-organization.md)[**Country**](c-country.md)                                                                                                                                                                                                                                                    |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                  |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;; AU)(A;; LCRPLORC;;; ED)(OA;; CCDC;4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2003-attributes"></a>Windows Attributi di Server 2003

Questa classe contiene gli attributi seguenti per Windows Server 2003:



| Attributo                                                                   | Obbligatorio | Derivato da                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Descrizione dell'amministratore**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria business**](a-businesscategory.md)                             | Falso     | **Unità organizzativa**         |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Codice paese**](a-countrycode.md)                                       | Falso     | **Unità organizzativa**         |
| [**Nome paese**](a-c.md)                                                 | Falso     | **Unità organizzativa**         |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Gruppo predefinito**](a-defaultgroup.md)                                     | Falso     | **Unità organizzativa**         |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Profilo desktop**](a-desktopprofile.md)                                 | Falso     | **Unità organizzativa**         |
| [**Indicatore di destinazione**](a-destinationindicator.md)                     | Falso     | **Unità organizzativa**         |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Extension-Name**](a-extensionname.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)            | Falso     | **Unità organizzativa**         |
| [**Bandiere**](a-flags.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Collegamento a CRITERI di gruppo**](a-gplink.md)                                                 | Falso     | **Unità organizzativa**         |
| [**Opzioni di Criteri di gruppo**](a-gpoptions.md)                                           | Falso     | **Unità organizzativa**         |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | **Unità organizzativa**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Membro di DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Titolare del privilegio**](a-isprivilegeholder.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                                | Falso     | **Unità organizzativa**         |
| [**Logo**](a-thumbnaillogo.md)                                             | Falso     | **Unità organizzativa**         |
| [**Gestito da**](a-managedby.md)                                           | Falso     | **Unità organizzativa**         |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)         | Falso     | **Unità organizzativa**         |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria di oggetti**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/> |
| [**Object-Guid**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Organizational-Unit-Name**](a-ou.md)                                    | Vero      | **Unità organizzativa**         |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falso     | **Unità organizzativa**         |
| [**Possibili inevasi**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo postale**](a-postaladdress.md)                                   | Falso     | **Unità organizzativa**         |
| [**Codice postale**](a-postalcode.md)                                         | Falso     | **Unità organizzativa**         |
| [**Post-Office-Box**](a-postofficebox.md)                                  | Falso     | **Unità organizzativa**         |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)              | Falso     | **Unità organizzativa**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo registrato**](a-registeredaddress.md)                           | Falso     | **Unità organizzativa**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Guida alla ricerca**](a-searchguide.md)                                       | Falso     | **Unità organizzativa**         |
| [**Vedere anche**](a-seealso.md)                                               | Falso     | **Unità organizzativa**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**State-Or-Province-Name**](a-st.md)                                      | Falso     | **Unità organizzativa**         |
| [**Via**](a-street.md)                                          | Falso     | **Unità organizzativa**         |
| [**Classe structural-object**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Sottori ref**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Numero di telefono**](a-telephonenumber.md)                               | Falso     | **Unità organizzativa**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falso     | **Unità organizzativa**         |
| [**Telex-Number**](a-telexnumber.md)                                       | Falso     | **Unità organizzativa**         |
| [**Text-Country**](a-co.md)                                                | Falso     | **Unità organizzativa**         |
| [**SUFFISSI UPN**](a-upnsuffixes.md)                                       | Falso     | **Unità organizzativa**         |
| [**User-Password**](a-userpassword.md)                                     | Falso     | **Unità organizzativa**         |
| [**Modifica di USN**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creato da USN**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene creato**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Www-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**X121-Address**](a-x121address.md)                                       | Falso     | **Unità organizzativa**         |



## <a name="windows-server-2003-extended-rights"></a>Windows Diritti estesi di Server 2003

Questa classe contiene i diritti estesi seguenti per Windows Server 2003:



| Nome comune                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generate-RSoP-Logging**](r-generate-rsop-logging.md)   |



## <a name="adam"></a>Adam

-   [Attributes (Attributi)](#adam-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                      |
| Object-Category             | 1                                                                                                                          |
| Default-Object-Category     | \-                                                                                                                         |
| Governs-Id                  | 2.5.6.5                                                                                                                    |
| Default-Hiding-Value        | 0                                                                                                                          |
| Rdn-Att-Id                  | [**Organizational-Unit-Name**](a-ou.md)<br/>                                                                        |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                            |
| Possibili superiori          | [**Domain-DNS**](c-domaindns.md)**Organizational-Unit**[**Organization**](c-organization.md)[**Country**](c-country.md) |
| Classi ausiliarie           | \-                                                                                                                         |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                               |
| Descrittore di sicurezza predefinito | D:S:                                                                                                                       |
| System-Flags                | 0x00000010                                                                                                                 |



## <a name="adam-attributes"></a>Attributi ADAM

Questa classe contiene gli attributi seguenti per ADAM:



| Attributo                                                                   | Obbligatorio | Derivato da                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Descrizione dell'amministratore**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria business**](a-businesscategory.md)                             | Falso     | **Unità organizzativa**         |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Codice paese**](a-countrycode.md)                                       | Falso     | **Unità organizzativa**         |
| [**Nome paese**](a-c.md)                                                 | Falso     | **Unità organizzativa**         |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Gruppo predefinito**](a-defaultgroup.md)                                     | Falso     | **Unità organizzativa**         |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Profilo desktop**](a-desktopprofile.md)                                 | Falso     | **Unità organizzativa**         |
| [**Indicatore di destinazione**](a-destinationindicator.md)                     | Falso     | **Unità organizzativa**         |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)            | Falso     | **Unità organizzativa**         |
| [**From-Entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | **Unità organizzativa**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Membro di DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                                | Falso     | **Unità organizzativa**         |
| [**Logo**](a-thumbnaillogo.md)                                             | Falso     | **Unità organizzativa**         |
| [**Gestito da**](a-managedby.md)                                           | Falso     | **Unità organizzativa**         |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria di oggetti**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/> |
| [**Object-Guid**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Organizational-Unit-Name**](a-ou.md)                                    | Vero      | **Unità organizzativa**         |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falso     | **Unità organizzativa**         |
| [**Possibili inevasi**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo postale**](a-postaladdress.md)                                   | Falso     | **Unità organizzativa**         |
| [**Codice postale**](a-postalcode.md)                                         | Falso     | **Unità organizzativa**         |
| [**Post-Office-Box**](a-postofficebox.md)                                  | Falso     | **Unità organizzativa**         |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)              | Falso     | **Unità organizzativa**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo registrato**](a-registeredaddress.md)                           | Falso     | **Unità organizzativa**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Guida alla ricerca**](a-searchguide.md)                                       | Falso     | **Unità organizzativa**         |
| [**Vedere anche**](a-seealso.md)                                               | Falso     | **Unità organizzativa**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                      | Falso     | **Unità organizzativa**         |
| [**Via e indirizzo**](a-street.md)                                          | Falso     | **Unità organizzativa**         |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Numero di telefono**](a-telephonenumber.md)                               | Falso     | **Unità organizzativa**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falso     | **Unità organizzativa**         |
| [**Telex-Number**](a-telexnumber.md)                                       | Falso     | **Unità organizzativa**         |
| [**Text-Country**](a-co.md)                                                | Falso     | **Unità organizzativa**         |
| [**Suffissi UPN**](a-upnsuffixes.md)                                       | Falso     | **Unità organizzativa**         |
| [**Password utente**](a-userpassword.md)                                     | Falso     | **Unità organizzativa**         |
| [**USN modificato**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creato da USN**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN intersito**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene creato**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Www-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**X121-Address**](a-x121address.md)                                       | Falso     | **Unità organizzativa**         |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributes (Attributi)](#windows-server-2003-r2-attributes)
-   [Diritti estesi](#windows-server-2003-r2-extended-rights)



| Voce | Valore |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| Rdn-Att-Id                  | [**Organizational-Unit-Name**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Possibili superiori          | [**Domain-DNS**](c-domaindns.md)**Organizational-Unit**[**Organization**](c-organization.md)[**Country**](c-country.md)                                                                                                                                                                                                                                                    |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                  |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;;; AU)(A;; LCRPLORC;;; ED)(OA;; CCDC;4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2003-r2-attributes"></a>Windows Attributi di Server 2003 R2

Questa classe contiene gli attributi seguenti per Windows Server 2003 R2:



| Attributo                                                                   | Obbligatorio | Derivato da                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Description**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria di business**](a-businesscategory.md)                             | Falso     | **Unità organizzativa**         |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Codice paese**](a-countrycode.md)                                       | Falso     | **Unità organizzativa**         |
| [**Nome paese**](a-c.md)                                                 | Falso     | **Unità organizzativa**         |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Gruppo predefinito**](a-defaultgroup.md)                                     | Falso     | **Unità organizzativa**         |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Profilo desktop**](a-desktopprofile.md)                                 | Falso     | **Unità organizzativa**         |
| [**Indicatore di destinazione**](a-destinationindicator.md)                     | Falso     | **Unità organizzativa**         |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Extension-Name**](a-extensionname.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)            | Falso     | **Unità organizzativa**         |
| [**Bandiere**](a-flags.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Collegamento a CRITERI di gruppo**](a-gplink.md)                                                 | Falso     | **Unità organizzativa**         |
| [**Opzioni di Criteri di gruppo**](a-gpoptions.md)                                           | Falso     | **Unità organizzativa**         |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)              | Falso     | **Unità organizzativa**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Membro di DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Titolare dei privilegi**](a-isprivilegeholder.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                                | Falso     | **Unità organizzativa**         |
| [**Logo**](a-thumbnaillogo.md)                                             | Falso     | **Unità organizzativa**         |
| [**Gestito da**](a-managedby.md)                                           | Falso     | **Unità organizzativa**         |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)         | Falso     | **Unità organizzativa**         |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria di oggetti**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/> |
| [**Object-Guid**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Organizational-Unit-Name**](a-ou.md)                                    | Vero      | **Unità organizzativa**         |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Falso     | **Unità organizzativa**         |
| [**Possibili inevasi**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo postale**](a-postaladdress.md)                                   | Falso     | **Unità organizzativa**         |
| [**Codice postale**](a-postalcode.md)                                         | Falso     | **Unità organizzativa**         |
| [**Post-Office-Box**](a-postofficebox.md)                                  | Falso     | **Unità organizzativa**         |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)              | Falso     | **Unità organizzativa**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo registrato**](a-registeredaddress.md)                           | Falso     | **Unità organizzativa**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Guida alla ricerca**](a-searchguide.md)                                       | Falso     | **Unità organizzativa**         |
| [**Vedere anche**](a-seealso.md)                                               | Falso     | **Unità organizzativa**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**State-Or-Province-Name**](a-st.md)                                      | Falso     | **Unità organizzativa**         |
| [**Via**](a-street.md)                                          | Falso     | **Unità organizzativa**         |
| [**Classe structural-object**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Sottori ref**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Numero di telefono**](a-telephonenumber.md)                               | Falso     | **Unità organizzativa**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falso     | **Unità organizzativa**         |
| [**Telex-Number**](a-telexnumber.md)                                       | Falso     | **Unità organizzativa**         |
| [**Text-Country**](a-co.md)                                                | Falso     | **Unità organizzativa**         |
| [**SUFFISSI UPN**](a-upnsuffixes.md)                                       | Falso     | **Unità organizzativa**         |
| [**User-Password**](a-userpassword.md)                                     | Falso     | **Unità organizzativa**         |
| [**Modifica di USN**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creato da USN**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando creato**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Www-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo X121**](a-x121address.md)                                       | Falso     | **Unità organizzativa**         |



## <a name="windows-server-2003-r2-extended-rights"></a>Windows Diritti estesi di Server 2003 R2

Questa classe contiene i seguenti diritti estesi per Windows Server 2003 R2:



| Nome comune                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generate-RSoP-Logging**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributes (Attributi)](#windows-server-2008-attributes)
-   [Diritti estesi](#windows-server-2008-extended-rights)



| Voce | Valore |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| Rdn-Att-Id                  | [**Nome unità organizzativa**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Possibili superiori          | [**Domain-DNS**](c-domaindns.md)**Organizational-Unit**[**Organization**](c-organization.md)[**Country**](c-country.md)                                                                                                                                                                                                                                                    |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                  |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;;; AU)(A;; LCRPLORC;;; ED)(OA;; CCDC;4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2008-attributes"></a>Windows Attributi di Server 2008

Questa classe contiene gli attributi seguenti per Windows Server 2008:



| Attributo                                                                      | Obbligatorio | Derivato da                    |
|--------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Descrizione dell'amministratore**](a-admindescription.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria business**](a-businesscategory.md)                                | Falso     | **Unità organizzativa**         |
| [**Canonical-Name**](a-canonicalname.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Codice paese**](a-countrycode.md)                                          | Falso     | **Unità organizzativa**         |
| [**Nome paese**](a-c.md)                                                    | Falso     | **Unità organizzativa**         |
| [**Creazione timestamp**](a-createtimestamp.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Gruppo predefinito**](a-defaultgroup.md)                                        | Falso     | **Unità organizzativa**         |
| [**Descrizione**](a-description.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Profilo desktop**](a-desktopprofile.md)                                    | Falso     | **Unità organizzativa**         |
| [**Indicatore di destinazione**](a-destinationindicator.md)                        | Falso     | **Unità organizzativa**         |
| [**Nome visualizzato**](a-displayname.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Extension-Name**](a-extensionname.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)               | Falso     | **Unità organizzativa**         |
| [**Bandiere**](a-flags.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Collegamento a Criteri di gruppo**](a-gplink.md)                                                    | Falso     | **Unità organizzativa**         |
| [**Opzioni di Criteri di gruppo**](a-gpoptions.md)                                              | Falso     | **Unità organizzativa**         |
| [**Tipo di istanza**](a-instancetype.md)                                        | Vero      | [**In alto**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                 | Falso     | **Unità organizzativa**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Member-Of-DL**](a-memberof.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Titolare di privilegi is**](a-isprivilegeholder.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                                   | Falso     | **Unità organizzativa**         |
| [**Logo**](a-thumbnaillogo.md)                                                | Falso     | **Unità organizzativa**         |
| [**Gestito da**](a-managedby.md)                                              | Falso     | **Unità organizzativa**         |
| [**Oggetti gestiti**](a-managedobjects.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica timestamp**](a-modifytimestamp.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)            | Falso     | **Unità organizzativa**         |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria di oggetti**](a-objectcategory.md)                                    | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe object**](a-objectclass.md)                                          | Vero      | [**In alto**](c-top.md)<br/> |
| [**Guid oggetto**](a-objectguid.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome unità organizzativa**](a-ou.md)                                       | Vero      | **Unità organizzativa**         |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)          | Falso     | **Unità organizzativa**         |
| [**Possibili eserezioni**](a-possibleinferiors.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo postale**](a-postaladdress.md)                                      | Falso     | **Unità organizzativa**         |
| [**Codice postale**](a-postalcode.md)                                            | Falso     | **Unità organizzativa**         |
| [**Post-Office-Box**](a-postofficebox.md)                                     | Falso     | **Unità organizzativa**         |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)                 | Falso     | **Unità organizzativa**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo registrato**](a-registeredaddress.md)                              | Falso     | **Unità organizzativa**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Guida alla ricerca**](a-searchguide.md)                                          | Falso     | **Unità organizzativa**         |
| [**Vedere anche**](a-seealso.md)                                                  | Falso     | **Unità organizzativa**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                         | Falso     | **Unità organizzativa**         |
| [**Via e indirizzo**](a-street.md)                                             | Falso     | **Unità organizzativa**         |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riferimenti secondari**](a-subrefs.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Numero di telefono**](a-telephonenumber.md)                                  | Falso     | **Unità organizzativa**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)             | Falso     | **Unità organizzativa**         |
| [**Telex-Number**](a-telexnumber.md)                                          | Falso     | **Unità organizzativa**         |
| [**Text-Country**](a-co.md)                                                   | Falso     | **Unità organizzativa**         |
| [**Suffissi UPN**](a-upnsuffixes.md)                                          | Falso     | **Unità organizzativa**         |
| [**Password utente**](a-userpassword.md)                                        | Falso     | **Unità organizzativa**         |
| [**USN modificato**](a-usnchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creato da USN**](a-usncreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN intersito**](a-usnintersite.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene modificato**](a-whenchanged.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando creato**](a-whencreated.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Www-Home-Page**](a-wwwhomepage.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo X121**](a-x121address.md)                                          | Falso     | **Unità organizzativa**         |



## <a name="windows-server-2008-extended-rights"></a>Windows Diritti estesi di Server 2008

Questa classe contiene i seguenti diritti estesi per Windows Server 2008:



| Nome comune                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generate-RSoP-Logging**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributes (Attributi)](#windows-server-2008-r2-attributes)
-   [Diritti estesi](#windows-server-2008-r2-extended-rights)



| Voce | Valore |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| Rdn-Att-Id                  | [**Nome unità organizzativa**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Possibili superiori          | [**Domain-DNS**](c-domaindns.md)**Organizational-Unit**[**Organization**](c-organization.md)[**Country**](c-country.md)                                                                                                                                                                                                                                                    |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                  |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;;; AU)(A;; LCRPLORC;;; ED)(OA;; CCDC;4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2008-r2-attributes"></a>Windows Attributi di Server 2008 R2

Questa classe contiene gli attributi seguenti per Windows Server 2008 R2:



| Attributo                                                                        | Obbligatorio | Derivato da                    |
|----------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Descrizione dell'amministratore**](a-admindescription.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria business**](a-businesscategory.md)                                  | Falso     | **Unità organizzativa**         |
| [**Canonical-Name**](a-canonicalname.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Codice paese**](a-countrycode.md)                                            | Falso     | **Unità organizzativa**         |
| [**Nome paese**](a-c.md)                                                      | Falso     | **Unità organizzativa**         |
| [**Creazione timestamp**](a-createtimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Gruppo predefinito**](a-defaultgroup.md)                                          | Falso     | **Unità organizzativa**         |
| [**Descrizione**](a-description.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Profilo desktop**](a-desktopprofile.md)                                      | Falso     | **Unità organizzativa**         |
| [**Indicatore di destinazione**](a-destinationindicator.md)                          | Falso     | **Unità organizzativa**         |
| [**Nome visualizzato**](a-displayname.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Extension-Name**](a-extensionname.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)                 | Falso     | **Unità organizzativa**         |
| [**Bandiere**](a-flags.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Collegamento a CRITERI di gruppo**](a-gplink.md)                                                      | Falso     | **Unità organizzativa**         |
| [**Opzioni di Criteri di gruppo**](a-gpoptions.md)                                                | Falso     | **Unità organizzativa**         |
| [**Tipo di istanza**](a-instancetype.md)                                          | Vero      | [**In alto**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                   | Falso     | **Unità organizzativa**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Member-Of-DL**](a-memberof.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Titolare del privilegio Is**](a-isprivilegeholder.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Recycled**](a-isrecycled.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                                     | Falso     | **Unità organizzativa**         |
| [**Logo**](a-thumbnaillogo.md)                                                  | Falso     | **Unità organizzativa**         |
| [**Gestito da**](a-managedby.md)                                                | Falso     | **Unità organizzativa**         |
| [**Oggetti gestiti**](a-managedobjects.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica timestamp**](a-modifytimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)              | Falso     | **Unità organizzativa**         |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria di oggetti**](a-objectcategory.md)                                      | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe object**](a-objectclass.md)                                            | Vero      | [**In alto**](c-top.md)<br/> |
| [**Object-Guid**](a-objectguid.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Organizational-Unit-Name**](a-ou.md)                                         | Vero      | **Unità organizzativa**         |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)            | Falso     | **Unità organizzativa**         |
| [**Possibili eserezioni**](a-possibleinferiors.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo postale**](a-postaladdress.md)                                        | Falso     | **Unità organizzativa**         |
| [**Codice postale**](a-postalcode.md)                                              | Falso     | **Unità organizzativa**         |
| [**Post-Office-Box**](a-postofficebox.md)                                       | Falso     | **Unità organizzativa**         |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)                   | Falso     | **Unità organizzativa**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo registrato**](a-registeredaddress.md)                                | Falso     | **Unità organizzativa**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Guida alla ricerca**](a-searchguide.md)                                            | Falso     | **Unità organizzativa**         |
| [**Vedere anche**](a-seealso.md)                                                    | Falso     | **Unità organizzativa**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                           | Falso     | **Unità organizzativa**         |
| [**Via e indirizzo**](a-street.md)                                               | Falso     | **Unità organizzativa**         |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riferimenti secondari**](a-subrefs.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Numero di telefono**](a-telephonenumber.md)                                    | Falso     | **Unità organizzativa**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)               | Falso     | **Unità organizzativa**         |
| [**Telex-Number**](a-telexnumber.md)                                            | Falso     | **Unità organizzativa**         |
| [**Text-Country**](a-co.md)                                                     | Falso     | **Unità organizzativa**         |
| [**Suffissi UPN**](a-upnsuffixes.md)                                            | Falso     | **Unità organizzativa**         |
| [**Password utente**](a-userpassword.md)                                          | Falso     | **Unità organizzativa**         |
| [**USN modificato**](a-usnchanged.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creato da USN**](a-usncreated.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN intersito**](a-usnintersite.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene modificato**](a-whenchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando creato**](a-whencreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Www-Home-Page**](a-wwwhomepage.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo X121**](a-x121address.md)                                            | Falso     | **Unità organizzativa**         |



## <a name="windows-server-2008-r2-extended-rights"></a>Windows Diritti estesi di Server 2008 R2

Questa classe contiene i seguenti diritti estesi per Windows Server 2008 R2:



| Nome comune                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generate-RSoP-Logging**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributes (Attributi)](#windows-server-2012-attributes)
-   [Diritti estesi](#windows-server-2012-extended-rights)



| Voce | Valore |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| Rdn-Att-Id                  | [**Nome unità organizzativa**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Possibili superiori          | [**Domain-DNS**](c-domaindns.md)**Organizational-Unit**[**Organization**](c-organization.md)[**Country**](c-country.md)                                                                                                                                                                                                                                                    |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                  |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(OA;; CCDC;bf967a86-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;; AO)(OA;; CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;; PO)(A;; RPLCLORC;;; AU)(A;; LCRPLORC;;; ED)(OA;; CCDC;4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attributi

Questa classe contiene gli attributi seguenti per Windows Server 2012:



| Attributo                                                                                    | Obbligatorio | Derivato da                    |
|----------------------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Descrizione dell'amministratore**](a-admindescription.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria business**](a-businesscategory.md)                                              | Falso     | **Unità organizzativa**         |
| [**Canonical-Name**](a-canonicalname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Codice paese**](a-countrycode.md)                                                        | Falso     | **Unità organizzativa**         |
| [**Nome paese**](a-c.md)                                                                  | Falso     | **Unità organizzativa**         |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Gruppo predefinito**](a-defaultgroup.md)                                                      | Falso     | **Unità organizzativa**         |
| [**Descrizione**](a-description.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Profilo desktop**](a-desktopprofile.md)                                                  | Falso     | **Unità organizzativa**         |
| [**Indicatore di destinazione**](a-destinationindicator.md)                                      | Falso     | **Unità organizzativa**         |
| [**Nome visualizzato**](a-displayname.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Extension-Name**](a-extensionname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Facsimile-Telephone-Number**](a-facsimiletelephonenumber.md)                             | Falso     | **Unità organizzativa**         |
| [**Bandiere**](a-flags.md)                                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Collegamento a Criteri di gruppo**](a-gplink.md)                                                                  | Falso     | **Unità organizzativa**         |
| [**Opzioni di Criteri di gruppo**](a-gpoptions.md)                                                            | Falso     | **Unità organizzativa**         |
| [**Tipo di istanza**](a-instancetype.md)                                                      | Vero      | [**In alto**](c-top.md)<br/> |
| [**International-ISDN-Number**](a-internationalisdnnumber.md)                               | Falso     | **Unità organizzativa**         |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Member-Of-DL**](a-memberof.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Titolare del privilegio Is**](a-isprivilegeholder.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Recycled**](a-isrecycled.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Locality-Name**](a-l.md)                                                                 | Falso     | **Unità organizzativa**         |
| [**Logo**](a-thumbnaillogo.md)                                                              | Falso     | **Unità organizzativa**         |
| [**Gestito da**](a-managedby.md)                                                            | Falso     | **Unità organizzativa**         |
| [**Oggetti gestiti**](a-managedobjects.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica timestamp**](a-modifytimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-UserPartitionSetLink**](a-mscom-userpartitionsetlink.md)                          | Falso     | **Unità organizzativa**         |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-Domain-For**](a-msds-isdomainfor.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria di oggetti**](a-objectcategory.md)                                                  | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe object**](a-objectclass.md)                                                        | Vero      | [**In alto**](c-top.md)<br/> |
| [**Guid oggetto**](a-objectguid.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome unità organizzativa**](a-ou.md)                                                     | Vero      | **Unità organizzativa**         |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Physical-Delivery-Office-Name**](a-physicaldeliveryofficename.md)                        | Falso     | **Unità organizzativa**         |
| [**Possibili eserezioni**](a-possibleinferiors.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo postale**](a-postaladdress.md)                                                    | Falso     | **Unità organizzativa**         |
| [**Codice postale**](a-postalcode.md)                                                          | Falso     | **Unità organizzativa**         |
| [**Post-Office-Box**](a-postofficebox.md)                                                   | Falso     | **Unità organizzativa**         |
| [**Metodo di recapito preferito**](a-preferreddeliverymethod.md)                               | Falso     | **Unità organizzativa**         |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo registrato**](a-registeredaddress.md)                                            | Falso     | **Unità organizzativa**         |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Guida alla ricerca**](a-searchguide.md)                                                        | Falso     | **Unità organizzativa**         |
| [**Vedere anche**](a-seealso.md)                                                                | Falso     | **Unità organizzativa**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**State-or-Province-Name**](a-st.md)                                                       | Falso     | **Unità organizzativa**         |
| [**Via e indirizzo**](a-street.md)                                                           | Falso     | **Unità organizzativa**         |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riferimenti secondari**](a-subrefs.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Numero di telefono**](a-telephonenumber.md)                                                | Falso     | **Unità organizzativa**         |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)                           | Falso     | **Unità organizzativa**         |
| [**Telex-Number**](a-telexnumber.md)                                                        | Falso     | **Unità organizzativa**         |
| [**Text-Country**](a-co.md)                                                                 | Falso     | **Unità organizzativa**         |
| [**Suffissi UPN**](a-upnsuffixes.md)                                                        | Falso     | **Unità organizzativa**         |
| [**Password utente**](a-userpassword.md)                                                      | Falso     | **Unità organizzativa**         |
| [**USN modificato**](a-usnchanged.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creato da USN**](a-usncreated.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN intersito**](a-usnintersite.md)                                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene modificato**](a-whenchanged.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creazione in data e ora**](a-whencreated.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Www-Home-Page**](a-wwwhomepage.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzo X121**](a-x121address.md)                                                        | Falso     | **Unità organizzativa**         |



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012 Diritti estesi

Questa classe contiene i seguenti diritti estesi per Windows Server 2012:



| Nome comune                                                |
|------------------------------------------------------------|
| [**Generate-RSoP-Planning**](r-generate-rsop-planning.md) |
| [**Generate-RSoP-Logging**](r-generate-rsop-logging.md)   |



 

 





