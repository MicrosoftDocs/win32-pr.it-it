---
title: Classe ms-DS-Service-Connection-Point-Publication-Service
description: Archivia le opzioni di configurazione per il servizio di pubblicazione del punto di connessione del servizio in ADAM.
ms.assetid: 30b4df70-a03b-4d42-b200-75bfa6cf8273
ms.tgt_platform: multiple
keywords:
- Schema AD della classe ms-DS-Service-Connection-Point-Publication-Service
- Schema AD della classe msDS-ServiceConnectionPointPublicationService
topic_type:
- apiref
api_name:
- ms-DS-Service-Connection-Point-Publication-Service
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b458a5d66d8d6fd90a58519ce57de03f625087be4123f2e51ca8c09534ed96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879841"
---
# <a name="ms-ds-service-connection-point-publication-service-class"></a>Classe ms-DS-Service-Connection-Point-Publication-Service

Archivia le opzioni di configurazione per il servizio di pubblicazione del punto di connessione del servizio in ADAM.



| Voce | Valore |
|-------------------|----------------------------------------------------|
| CN                | ms-DS-Service-Connection-Point-Publication-Service |
| Ldap-Display-Name | msDS-ServiceConnectionPointPublicationService      |
| Aggiorna privilegio  | \-                                                 |
| Frequenza di aggiornamento  | \-                                                 |
| Schema-Id-Guid    | d33f5da6-b009-7e48-8268-b2305529e933               |



## <a name="implementations"></a>Implementazioni

-   [**Adam**](#adam-attributes)

## <a name="adam"></a>Adam

-   [Attributes (Attributi)](#adam-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------|
| System-Only                 | Vero                                   |
| Object-Category             | 1                                      |
| Default-Object-Category     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.5.247                 |
| Default-Hiding-Value        | 1                                      |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/> |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>        |
| Possibili superiori          | [**NTDS-Service**](c-ntdsservice.md)  |
| Classi ausiliarie           | \-                                     |
| NT-Security-Descriptor      | O:BAG:BAD:S:                           |
| Descrittore di sicurezza predefinito | D:S:                                   |
| System-Flags                | 0x00000000                             |



## <a name="adam-attributes"></a>Attributi ADAM

Questa classe contiene gli attributi seguenti per ADAM:



| Attributo                                                                   | Obbligatorio | Derivato da                                           |
|-----------------------------------------------------------------------------|-----------|--------------------------------------------------------|
| [**Descrizione dell'amministratore**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Nome comune**](a-cn.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Abilitato**](a-enabled.md)                                                | Falso     | **ms-DS-Service-Connection-Point-Publication-Service** |
| [**From-Entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                        |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Membro di DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Parole chiavi**](a-keywords.md)                                              | Falso     | **ms-DS-Service-Connection-Point-Publication-Service** |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Modifica timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**ms-DS-Disable-For-Instances**](a-msds-disableforinstances.md)           | Falso     | **ms-DS-Service-Connection-Point-Publication-Service** |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)      | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**ms-DS-SCP-Container**](a-msds-scpcontainer.md)                          | Falso     | **ms-DS-Service-Connection-Point-Publication-Service** |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/>                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Categoria di oggetti**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/>                        |
| [**Classe object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/>                        |
| [**Guid oggetto**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Possibili eserezioni**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Rdn**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**USN modificato**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Creato da USN**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**USN intersito**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Quando viene modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Quando creato**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**Www-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                        |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                        |



 

 





