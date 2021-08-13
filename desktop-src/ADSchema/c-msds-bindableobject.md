---
title: Classe ms-DS-Bindable-Object
description: Classe ausiliaria per rappresentare un oggetto associabile. Qualsiasi classe definita dall'utente che rappresenta un'entità che può essere usata per l'associazione alla directory (ovvero un utente) deve includere questa classe ausiliaria.
ms.assetid: 181b3e2b-9442-4f11-9af7-4697491115f3
ms.tgt_platform: multiple
keywords:
- Schema AD della classe ms-DS-Bindable-Object
- Schema AD della classe msDS-BindableObject
topic_type:
- apiref
api_name:
- ms-DS-Bindable-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b702a26c61920f5a3868ccc479b1f8578a3075907b5dc5bc2eb9d070321c91d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118680781"
---
# <a name="ms-ds-bindable-object-class"></a>Classe ms-DS-Bindable-Object

Classe ausiliaria per rappresentare un oggetto associabile. Qualsiasi classe definita dall'utente che rappresenta un'entità che può essere usata per l'associazione alla directory (ovvero un utente) deve includere questa classe ausiliaria.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Ms-DS-Bindable-Object                |
| Ldap-Display-Name | msDS-BindableObject                  |
| Aggiorna privilegio  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Schema-Id-Guid    | 89f4a69f-4416-6b49-821d-6e3c4a0ff802 |



## <a name="implementations"></a>Implementazioni

-   [**Adam**](#adam-attributes)

## <a name="adam"></a>Adam

-   [Attributes (Attributi)](#adam-attributes)



| Voce | Valore |
|-----------------------------|--------------------------------------------------------------|
| System-Only                 | Falso                                                        |
| Object-Category             | 3                                                            |
| Default-Object-Category     | \-                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.244                                       |
| Default-Hiding-Value        | 1                                                            |
| Rdn-Att-Id                  | \-                                                           |
| Sottoclasse di                 | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |
| Possibili superiori          | \-                                                           |
| Classi ausiliarie           | \-                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                 |
| Descrittore di sicurezza predefinito | \-                                                           |
| System-Flags                | 0x00000010                                                   |



## <a name="adam-attributes"></a>Attributi ADAM

Questa classe contiene gli attributi seguenti per ADAM:



| Attributo                                                                                      | Obbligatorio | Derivato da                                                                                 |
|------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Scadenza account**](a-accountexpires.md)                                                    | Falso     | **Ms-DS-Bindable-Object**                                                                    |
| [**Descrizione dell'amministratore**](a-admindescription.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Attributi consentiti**](a-allowedattributes.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Ora password non valida**](a-badpasswordtime.md)                                                 | Falso     | **Ms-DS-Bindable-Object**                                                                    |
| [**Bad-Pwd-Count**](a-badpwdcount.md)                                                         | Falso     | **Ms-DS-Bindable-Object**                                                                    |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Canonical-Name**](a-canonicalname.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Nome comune**](a-cn.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Creazione timestamp**](a-createtimestamp.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Descrizione**](a-description.md)                                                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Nome visualizzato**](a-displayname.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Firma DSA**](a-dsasignature.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**From-Entry**](a-fromentry.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Tipo di istanza**](a-instancetype.md)                                                        | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-Deleted**](a-isdeleted.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-Member-Of-DL**](a-memberof.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Last-Logon-Timestamp**](a-lastlogontimestamp.md)                                           | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Tempo di blocco**](a-lockouttime.md)                                                          | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Oggetti gestiti**](a-managedobjects.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Mastered-By**](a-masteredby.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Modifica timestamp**](a-modifytimestamp.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-User-Account-Auto-Locked**](a-ms-ds-useraccountautolocked.md)                        | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)            | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Account-Disabled**](a-msds-useraccountdisabled.md)                              | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Dont-Expire-Password**](a-msds-userdontexpirepassword.md)                       | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Encrypted-Text-Password-Allowed**](a-ms-ds-userencryptedtextpasswordallowed.md) | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Password-Expired**](a-msds-userpasswordexpired.md)                              | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**ms-DS-User-Password-Not-Required**](a-ms-ds-userpasswordnotrequired.md)                    | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Nt-Pwd-History**](a-ntpwdhistory.md)                                                       | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                       | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Categoria di oggetti**](a-objectcategory.md)                                                    | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Classe object**](a-objectclass.md)                                                          | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Object-Guid**](a-objectguid.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Object-Sid**](a-objectsid.md)                                                              | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Versione oggetto**](a-objectversion.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Possibili inevasi**](a-possibleinferiors.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Pwd-Last-Set**](a-pwdlastset.md)                                                           | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Rdn**](a-name.md)                                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Reps-From**](a-repsfrom.md)                                                                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Reps-To**](a-repsto.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Revisione**](a-revision.md)                                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Classe structural-object**](a-structuralobjectclass.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Sottori ref**](a-subrefs.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Credenziali supplementari**](a-supplementalcredentials.md)                                  | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Flag di sistema**](a-systemflags.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Gruppi di token**](a-tokengroups.md)                                                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Unicode-Pwd**](a-unicodepwd.md)                                                            | Falso     | **ms-DS-Bindable-Object**                                                                    |
| [**Modifica di USN**](a-usnchanged.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Creato da USN**](a-usncreated.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-Intersite**](a-usnintersite.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-Source**](a-usnsource.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Wbem-Path**](a-wbempath.md)                                                                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Oggetti noti**](a-wellknownobjects.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Quando viene modificato**](a-whenchanged.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Quando creato**](a-whencreated.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Www-Home-Page**](a-wwwhomepage.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WWW-Page-Other**](a-url.md)                                                                | Falso     | [**In alto**](c-top.md)<br/>                                                              |



 

 





