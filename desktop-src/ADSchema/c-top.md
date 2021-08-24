---
title: Classe principale
description: Classe di primo livello da cui vengono derivate tutte le classi.
ms.assetid: 025aff6c-1804-4141-accf-d50cfd50e90e
ms.tgt_platform: multiple
keywords:
- Schema ad Active Directory di livello superiore
- Schema ad Active Directory di livello superiore
topic_type:
- apiref
api_name:
- Top
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248726d9fac9c0d39fae5759df08d4ea10f4f012ba1a1ce0cc2f4dbe55d76a6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580591"
---
# <a name="top-class"></a>Classe principale

Classe di primo livello da cui vengono derivate tutte le classi.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Inizio                                  |
| Ldap-Display-Name | top                                  |
| Privilegio di aggiornamento  | Amministratore dello schema                 |
| Frequenza di aggiornamento  | \-                                   |
| Schema-Id-Guid    | bf967ab7-0de6-11d0-a285-00aa003049e2 |



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
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | **Top**<br/>                                                                           |
| Possibili superiori          | [**Persi e trovati**](c-lostandfound.md)                                                     |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;; Au) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows 2000 Server Attributes

Questa classe contiene gli attributi seguenti per Windows 2000 Server:



| Attributo                                                                 | Obbligatorio | Derivato da |
|---------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Description**](a-admindescription.md)                           | Falso     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Falso     | **Top**      |
| [**Attributi consentiti**](a-allowedattributes.md)                         | Falso     | **Top**      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | Falso     | **Top**      |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                    | Falso     | **Top**      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | Falso     | **Top**      |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falso     | **Top**      |
| [**Canonical-Name**](a-canonicalname.md)                                 | Falso     | **Top**      |
| [**Nome comune**](a-cn.md)                                               | Falso     | **Top**      |
| [**Create-Time-Stamp**](a-createtimestamp.md)                            | Falso     | **Top**      |
| [**Descrizione**](a-description.md)                                      | Falso     | **Top**      |
| [**Nome visualizzato**](a-displayname.md)                                     | Falso     | **Top**      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                  | Falso     | **Top**      |
| [**Firma DSA**](a-dsasignature.md)                                   | Falso     | **Top**      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)               | Falso     | **Top**      |
| [**Extension-Name**](a-extensionname.md)                                 | Falso     | **Top**      |
| [**Bandiere**](a-flags.md)                                                  | Falso     | **Top**      |
| [**From-Entry**](a-fromentry.md)                                         | Falso     | **Top**      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falso     | **Top**      |
| [**Tipo di istanza**](a-instancetype.md)                                   | Vero      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falso     | **Top**      |
| [**Is-Deleted**](a-isdeleted.md)                                         | Falso     | **Top**      |
| [**Membro di DL**](a-memberof.md)                                     | Falso     | **Top**      |
| [**Titolare del privilegio**](a-isprivilegeholder.md)                        | Falso     | **Top**      |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                            | Falso     | **Top**      |
| [**Oggetti gestiti**](a-managedobjects.md)                               | Falso     | **Top**      |
| [**Mastered-By**](a-masteredby.md)                                       | Falso     | **Top**      |
| [**Modifica timestamp**](a-modifytimestamp.md)                            | Falso     | **Top**      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | **Top**      |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Falso     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Vero      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falso     | **Top**      |
| [**Categoria di oggetti**](a-objectcategory.md)                               | Vero      | **Top**      |
| [**Classe object**](a-objectclass.md)                                     | Vero      | **Top**      |
| [**Guid oggetto**](a-objectguid.md)                                       | Falso     | **Top**      |
| [**Versione oggetto**](a-objectversion.md)                                 | Falso     | **Top**      |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)               | Falso     | **Top**      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md) | Falso     | **Top**      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                    | Falso     | **Top**      |
| [**Possibili eserezioni**](a-possibleinferiors.md)                         | Falso     | **Top**      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | Falso     | **Top**      |
| [**Indirizzi proxy**](a-proxyaddresses.md)                               | Falso     | **Top**      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | Falso     | **Top**      |
| [**Rdn**](a-name.md)                                                     | Falso     | **Top**      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | Falso     | **Top**      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | Falso     | **Top**      |
| [**Report**](a-directreports.md)                                        | Falso     | **Top**      |
| [**Reps-From**](a-repsfrom.md)                                           | Falso     | **Top**      |
| [**Reps-To**](a-repsto.md)                                               | Falso     | **Top**      |
| [**Revisione**](a-revision.md)                                            | Falso     | **Top**      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | Falso     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Falso     | **Top**      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)            | Falso     | **Top**      |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                  | Falso     | **Top**      |
| [**Riferimenti secondari**](a-subrefs.md)                                             | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | **Top**      |
| [**Flag di sistema**](a-systemflags.md)                                     | Falso     | **Top**      |
| [**USN modificato**](a-usnchanged.md)                                       | Falso     | **Top**      |
| [**Creato da USN**](a-usncreated.md)                                       | Falso     | **Top**      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                | Falso     | **Top**      |
| [**USN intersito**](a-usnintersite.md)                                   | Falso     | **Top**      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | Falso     | **Top**      |
| [**USN-Source**](a-usnsource.md)                                         | Falso     | **Top**      |
| [**Wbem-Path**](a-wbempath.md)                                           | Falso     | **Top**      |
| [**Oggetti noti**](a-wellknownobjects.md)                          | Falso     | **Top**      |
| [**Quando viene modificato**](a-whenchanged.md)                                     | Falso     | **Top**      |
| [**Quando creato**](a-whencreated.md)                                     | Falso     | **Top**      |
| [**Www-Home-Page**](a-wwwhomepage.md)                                    | Falso     | **Top**      |
| [**WWW-Page-Other**](a-url.md)                                           | Falso     | **Top**      |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributes (Attributi)](#windows-server-2003-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | **Top**<br/>                                                                           |
| Possibili superiori          | [**Oggetti persi e trovati**](c-lostandfound.md)                                                     |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; Au) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Attributi di Server 2003

Questa classe contiene gli attributi seguenti per Windows Server 2003:



| Attributo                                                                   | Obbligatorio | Derivato da |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Description**](a-admindescription.md)                             | Falso     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | **Top**      |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | **Top**      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | **Top**      |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | **Top**      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | **Top**      |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | **Top**      |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | **Top**      |
| [**Nome comune**](a-cn.md)                                                 | Falso     | **Top**      |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | Falso     | **Top**      |
| [**Descrizione**](a-description.md)                                        | Falso     | **Top**      |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | **Top**      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falso     | **Top**      |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | **Top**      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | **Top**      |
| [**Extension-Name**](a-extensionname.md)                                   | Falso     | **Top**      |
| [**Bandiere**](a-flags.md)                                                    | Falso     | **Top**      |
| [**From-Entry**](a-fromentry.md)                                           | Falso     | **Top**      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | **Top**      |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | **Top**      |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falso     | **Top**      |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | **Top**      |
| [**Titolare del privilegio Is**](a-isprivilegeholder.md)                          | Falso     | **Top**      |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | **Top**      |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | **Top**      |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | **Top**      |
| [**Modifica timestamp**](a-modifytimestamp.md)                              | Falso     | **Top**      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | **Top**      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | **Top**      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | **Top**      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | **Top**      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | **Top**      |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | **Top**      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | **Top**      |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | **Top**      |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | **Top**      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | **Top**      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | **Top**      |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | **Top**      |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | **Top**      |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Vero      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | **Top**      |
| [**Categoria di oggetti**](a-objectcategory.md)                                 | Vero      | **Top**      |
| [**Classe object**](a-objectclass.md)                                       | Vero      | **Top**      |
| [**Guid oggetto**](a-objectguid.md)                                         | Falso     | **Top**      |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | **Top**      |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                 | Falso     | **Top**      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | **Top**      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | **Top**      |
| [**Possibili eserezioni**](a-possibleinferiors.md)                           | Falso     | **Top**      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | **Top**      |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | **Top**      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | **Top**      |
| [**Rdn**](a-name.md)                                                       | Falso     | **Top**      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | **Top**      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | **Top**      |
| [**Report**](a-directreports.md)                                          | Falso     | **Top**      |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | **Top**      |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | **Top**      |
| [**Revisione**](a-revision.md)                                              | Falso     | **Top**      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | **Top**      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | **Top**      |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                    | Falso     | **Top**      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | **Top**      |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | **Top**      |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | **Top**      |
| [**USN modificato**](a-usnchanged.md)                                         | Falso     | **Top**      |
| [**Creato da USN**](a-usncreated.md)                                         | Falso     | **Top**      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | **Top**      |
| [**USN -Intersite**](a-usnintersite.md)                                     | Falso     | **Top**      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | **Top**      |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | **Top**      |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | **Top**      |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | **Top**      |
| [**Quando viene modificato**](a-whenchanged.md)                                       | Falso     | **Top**      |
| [**Creazione in data e ora**](a-whencreated.md)                                       | Falso     | **Top**      |
| [**Www-Home-Page**](a-wwwhomepage.md)                                      | Falso     | **Top**      |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | **Top**      |



## <a name="adam"></a>Adam

-   [Attributes (Attributi)](#adam-attributes)



| Voce | Valore |
|-----------------------------|------------------------------------------|
| System-Only                 | Vero                                     |
| Object-Category             | 2                                        |
| Default-Object-Category     | \-                                       |
| Governs-Id                  | 2.5.6.0                                  |
| Default-Hiding-Value        | 1                                        |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>   |
| Sottoclasse di                 | **Top**<br/>                       |
| Possibili superiori          | [**Oggetti persi e trovati**](c-lostandfound.md) |
| Classi ausiliarie           | \-                                       |
| NT-Security-Descriptor      | O:BAG:BAD:S:                             |
| Descrittore di sicurezza predefinito | D:S:                                     |
| System-Flags                | 0x00000010                               |



## <a name="adam-attributes"></a>Attributi ADAM

Questa classe contiene gli attributi seguenti per ADAM:



| Attributo                                                                   | Obbligatorio | Derivato da |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Description**](a-admindescription.md)                             | Falso     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | **Top**      |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | **Top**      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | **Top**      |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | **Top**      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | **Top**      |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | **Top**      |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | **Top**      |
| [**Nome comune**](a-cn.md)                                                 | Falso     | **Top**      |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | Falso     | **Top**      |
| [**Descrizione**](a-description.md)                                        | Falso     | **Top**      |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | **Top**      |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | **Top**      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | **Top**      |
| [**From-Entry**](a-fromentry.md)                                           | Falso     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | **Top**      |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | **Top**      |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falso     | **Top**      |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | **Top**      |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | **Top**      |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | **Top**      |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | **Top**      |
| [**Modifica timestamp**](a-modifytimestamp.md)                              | Falso     | **Top**      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | **Top**      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | **Top**      |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)      | Falso     | **Top**      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | **Top**      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | **Top**      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | **Top**      |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Falso     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Vero      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | **Top**      |
| [**Categoria di oggetti**](a-objectcategory.md)                                 | Vero      | **Top**      |
| [**Classe object**](a-objectclass.md)                                       | Vero      | **Top**      |
| [**Object-Guid**](a-objectguid.md)                                         | Falso     | **Top**      |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | **Top**      |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                 | Falso     | **Top**      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | **Top**      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | **Top**      |
| [**Possibili inevasi**](a-possibleinferiors.md)                           | Falso     | **Top**      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | **Top**      |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | **Top**      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | **Top**      |
| [**Rdn**](a-name.md)                                                       | Falso     | **Top**      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | **Top**      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | **Top**      |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | **Top**      |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | **Top**      |
| [**Revisione**](a-revision.md)                                              | Falso     | **Top**      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | **Top**      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | **Top**      |
| [**Classe structural-object**](a-structuralobjectclass.md)                  | Falso     | **Top**      |
| [**Sottori ref**](a-subrefs.md)                                               | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | **Top**      |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | **Top**      |
| [**Modifica di USN**](a-usnchanged.md)                                         | Falso     | **Top**      |
| [**Creato da USN**](a-usncreated.md)                                         | Falso     | **Top**      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | **Top**      |
| [**USN -Intersite**](a-usnintersite.md)                                     | Falso     | **Top**      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | **Top**      |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | **Top**      |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | **Top**      |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | **Top**      |
| [**Quando viene modificato**](a-whenchanged.md)                                       | Falso     | **Top**      |
| [**Creazione in data e ora**](a-whencreated.md)                                       | Falso     | **Top**      |
| [**Www-Home-Page**](a-wwwhomepage.md)                                      | Falso     | **Top**      |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | **Top**      |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributes (Attributi)](#windows-server-2003-r2-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | **Top**<br/>                                                                           |
| Possibili superiori          | [**Oggetti persi e trovati**](c-lostandfound.md)                                                     |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; Au) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Attributi di Server 2003 R2

Questa classe contiene gli attributi seguenti per Windows Server 2003 R2:



| Attributo                                                                   | Obbligatorio | Derivato da |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Descrizione dell'amministratore**](a-admindescription.md)                             | Falso     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | **Top**      |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | **Top**      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | **Top**      |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                      | Falso     | **Top**      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | **Top**      |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | **Top**      |
| [**Nome comune**](a-cn.md)                                                 | Falso     | **Top**      |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | **Top**      |
| [**Descrizione**](a-description.md)                                        | Falso     | **Top**      |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | **Top**      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falso     | **Top**      |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | **Top**      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | **Top**      |
| [**Extension-Name**](a-extensionname.md)                                   | Falso     | **Top**      |
| [**Bandiere**](a-flags.md)                                                    | Falso     | **Top**      |
| [**From-Entry**](a-fromentry.md)                                           | Falso     | **Top**      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | **Top**      |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | **Top**      |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falso     | **Top**      |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | **Top**      |
| [**Titolare del privilegio Is**](a-isprivilegeholder.md)                          | Falso     | **Top**      |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | **Top**      |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | **Top**      |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | **Top**      |
| [**Modifica timestamp**](a-modifytimestamp.md)                              | Falso     | **Top**      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | **Top**      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | **Top**      |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | **Top**      |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | **Top**      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | **Top**      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | **Top**      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | **Top**      |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | **Top**      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | **Top**      |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | **Top**      |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | **Top**      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | **Top**      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | **Top**      |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | **Top**      |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | **Top**      |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | Falso     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | **Top**      |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Vero      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | **Top**      |
| [**Categoria di oggetti**](a-objectcategory.md)                                 | Vero      | **Top**      |
| [**Classe object**](a-objectclass.md)                                       | Vero      | **Top**      |
| [**Object-Guid**](a-objectguid.md)                                         | Falso     | **Top**      |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | **Top**      |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                 | Falso     | **Top**      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | **Top**      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | **Top**      |
| [**Possibili inevasi**](a-possibleinferiors.md)                           | Falso     | **Top**      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | **Top**      |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | **Top**      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | **Top**      |
| [**Rdn**](a-name.md)                                                       | Falso     | **Top**      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | **Top**      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | **Top**      |
| [**Report**](a-directreports.md)                                          | Falso     | **Top**      |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | **Top**      |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | **Top**      |
| [**Revisione**](a-revision.md)                                              | Falso     | **Top**      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | **Top**      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | **Top**      |
| [**Classe structural-object**](a-structuralobjectclass.md)                  | Falso     | **Top**      |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | **Top**      |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | **Top**      |
| [**USN modificato**](a-usnchanged.md)                                         | Falso     | **Top**      |
| [**Creato da USN**](a-usncreated.md)                                         | Falso     | **Top**      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | **Top**      |
| [**USN -Intersite**](a-usnintersite.md)                                     | Falso     | **Top**      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | **Top**      |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | **Top**      |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | **Top**      |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | **Top**      |
| [**Quando viene modificato**](a-whenchanged.md)                                       | Falso     | **Top**      |
| [**Creazione in data e ora**](a-whencreated.md)                                       | Falso     | **Top**      |
| [**Www-Home-Page**](a-wwwhomepage.md)                                      | Falso     | **Top**      |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | **Top**      |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributes (Attributi)](#windows-server-2008-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | **Top**<br/>                                                                           |
| Possibili superiori          | [**Oggetti persi e trovati**](c-lostandfound.md)                                                     |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; Au) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Attributi di Server 2008

Questa classe contiene gli attributi seguenti per Windows Server 2008:



| Attributo                                                                      | Obbligatorio | Derivato da |
|--------------------------------------------------------------------------------|-----------|--------------|
| [**Descrizione dell'amministratore**](a-admindescription.md)                                | Falso     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | **Top**      |
| [**Attributi consentiti**](a-allowedattributes.md)                              | Falso     | **Top**      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falso     | **Top**      |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                         | Falso     | **Top**      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falso     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | **Top**      |
| [**Canonical-Name**](a-canonicalname.md)                                      | Falso     | **Top**      |
| [**Nome comune**](a-cn.md)                                                    | Falso     | **Top**      |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                 | Falso     | **Top**      |
| [**Descrizione**](a-description.md)                                           | Falso     | **Top**      |
| [**Nome visualizzato**](a-displayname.md)                                          | Falso     | **Top**      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                       | Falso     | **Top**      |
| [**Firma DSA**](a-dsasignature.md)                                        | Falso     | **Top**      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                    | Falso     | **Top**      |
| [**Extension-Name**](a-extensionname.md)                                      | Falso     | **Top**      |
| [**Bandiere**](a-flags.md)                                                       | Falso     | **Top**      |
| [**From-Entry**](a-fromentry.md)                                              | Falso     | **Top**      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falso     | **Top**      |
| [**Tipo di istanza**](a-instancetype.md)                                        | Vero      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | **Top**      |
| [**Is-Deleted**](a-isdeleted.md)                                              | Falso     | **Top**      |
| [**Is-Member-Of-DL**](a-memberof.md)                                          | Falso     | **Top**      |
| [**Titolare di privilegi is**](a-isprivilegeholder.md)                             | Falso     | **Top**      |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                 | Falso     | **Top**      |
| [**Oggetti gestiti**](a-managedobjects.md)                                    | Falso     | **Top**      |
| [**Mastered-By**](a-masteredby.md)                                            | Falso     | **Top**      |
| [**Modifica timestamp**](a-modifytimestamp.md)                                 | Falso     | **Top**      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | **Top**      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | Falso     | **Top**      |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | **Top**      |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | **Top**      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | Falso     | **Top**      |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | **Top**      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | **Top**      |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                              | Falso     | **Top**      |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                   | Falso     | **Top**      |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)             | Falso     | **Top**      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | **Top**      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | Falso     | **Top**      |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)              | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | **Top**      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | **Top**      |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falso     | **Top**      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | Falso     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | **Top**      |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | **Top**      |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | **Top**      |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | Falso     | **Top**      |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | Falso     | **Top**      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Falso     | **Top**      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Falso     | **Top**      |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                             | Falso     | **Top**      |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | **Top**      |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | **Top**      |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | **Top**      |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | Falso     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | **Top**      |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                        | Falso     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Vero      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falso     | **Top**      |
| [**Categoria di oggetti**](a-objectcategory.md)                                    | Vero      | **Top**      |
| [**Classe object**](a-objectclass.md)                                          | Vero      | **Top**      |
| [**Object-Guid**](a-objectguid.md)                                            | Falso     | **Top**      |
| [**Versione oggetto**](a-objectversion.md)                                      | Falso     | **Top**      |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                    | Falso     | **Top**      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | Falso     | **Top**      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | Falso     | **Top**      |
| [**Possibili inevasi**](a-possibleinferiors.md)                              | Falso     | **Top**      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falso     | **Top**      |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                    | Falso     | **Top**      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falso     | **Top**      |
| [**Rdn**](a-name.md)                                                          | Falso     | **Top**      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falso     | **Top**      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | **Top**      |
| [**Report**](a-directreports.md)                                             | Falso     | **Top**      |
| [**Reps-From**](a-repsfrom.md)                                                | Falso     | **Top**      |
| [**Reps-To**](a-repsto.md)                                                    | Falso     | **Top**      |
| [**Revisione**](a-revision.md)                                                 | Falso     | **Top**      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | Falso     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Falso     | **Top**      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                 | Falso     | **Top**      |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                       | Falso     | **Top**      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Falso     | **Top**      |
| [**Riferimenti secondari**](a-subrefs.md)                                                  | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | **Top**      |
| [**Flag di sistema**](a-systemflags.md)                                          | Falso     | **Top**      |
| [**USN modificato**](a-usnchanged.md)                                            | Falso     | **Top**      |
| [**Creato da USN**](a-usncreated.md)                                            | Falso     | **Top**      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                     | Falso     | **Top**      |
| [**USN -Intersite**](a-usnintersite.md)                                        | Falso     | **Top**      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | Falso     | **Top**      |
| [**USN-Source**](a-usnsource.md)                                              | Falso     | **Top**      |
| [**Wbem-Path**](a-wbempath.md)                                                | Falso     | **Top**      |
| [**Oggetti noti**](a-wellknownobjects.md)                               | Falso     | **Top**      |
| [**Quando viene modificato**](a-whenchanged.md)                                          | Falso     | **Top**      |
| [**Creazione in data e ora**](a-whencreated.md)                                          | Falso     | **Top**      |
| [**Www-Home-Page**](a-wwwhomepage.md)                                         | Falso     | **Top**      |
| [**WWW-Page-Other**](a-url.md)                                                | Falso     | **Top**      |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributes (Attributi)](#windows-server-2008-r2-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | **Top**<br/>                                                                           |
| Possibili superiori          | [**Persi e trovati**](c-lostandfound.md)                                                     |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;; Au) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Attributi di Server 2008 R2

Questa classe contiene gli attributi seguenti per Windows Server 2008 R2:



| Attributo                                                                        | Obbligatorio | Derivato da |
|----------------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Description**](a-admindescription.md)                                  | Falso     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | **Top**      |
| [**Attributi consentiti**](a-allowedattributes.md)                                | Falso     | **Top**      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | **Top**      |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                           | Falso     | **Top**      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | **Top**      |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | **Top**      |
| [**Canonical-Name**](a-canonicalname.md)                                        | Falso     | **Top**      |
| [**Nome comune**](a-cn.md)                                                      | Falso     | **Top**      |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                   | Falso     | **Top**      |
| [**Descrizione**](a-description.md)                                             | Falso     | **Top**      |
| [**Nome visualizzato**](a-displayname.md)                                            | Falso     | **Top**      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falso     | **Top**      |
| [**Firma DSA**](a-dsasignature.md)                                          | Falso     | **Top**      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | **Top**      |
| [**Extension-Name**](a-extensionname.md)                                        | Falso     | **Top**      |
| [**Bandiere**](a-flags.md)                                                         | Falso     | **Top**      |
| [**From-Entry**](a-fromentry.md)                                                | Falso     | **Top**      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | **Top**      |
| [**Tipo di istanza**](a-instancetype.md)                                          | Vero      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | **Top**      |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falso     | **Top**      |
| [**Is-Member-Of-DL**](a-memberof.md)                                            | Falso     | **Top**      |
| [**Titolare di privilegi is**](a-isprivilegeholder.md)                               | Falso     | **Top**      |
| [**Viene riciclato**](a-isrecycled.md)                                              | Falso     | **Top**      |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                   | Falso     | **Top**      |
| [**Oggetti gestiti**](a-managedobjects.md)                                      | Falso     | **Top**      |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | **Top**      |
| [**Modifica timestamp**](a-modifytimestamp.md)                                   | Falso     | **Top**      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | **Top**      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | **Top**      |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | **Top**      |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | **Top**      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | **Top**      |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | **Top**      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | **Top**      |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | **Top**      |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | **Top**      |
| [**ms-DS-is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | **Top**      |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | **Top**      |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)               | Falso     | **Top**      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | **Top**      |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | **Top**      |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falso     | **Top**      |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falso     | **Top**      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | **Top**      |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | **Top**      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | **Top**      |
| [**Ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | **Top**      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | **Top**      |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | **Top**      |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | **Top**      |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | **Top**      |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | **Top**      |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | **Top**      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | **Top**      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | **Top**      |
| [**Ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falso     | **Top**      |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | **Top**      |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | **Top**      |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | **Top**      |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | **Top**      |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Vero      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | **Top**      |
| [**Categoria di oggetti**](a-objectcategory.md)                                      | Vero      | **Top**      |
| [**Classe object**](a-objectclass.md)                                            | Vero      | **Top**      |
| [**Guid oggetto**](a-objectguid.md)                                              | Falso     | **Top**      |
| [**Versione oggetto**](a-objectversion.md)                                        | Falso     | **Top**      |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                      | Falso     | **Top**      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | **Top**      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falso     | **Top**      |
| [**Possibili eserezioni**](a-possibleinferiors.md)                                | Falso     | **Top**      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falso     | **Top**      |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                      | Falso     | **Top**      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falso     | **Top**      |
| [**Rdn**](a-name.md)                                                            | Falso     | **Top**      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falso     | **Top**      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | **Top**      |
| [**Report**](a-directreports.md)                                               | Falso     | **Top**      |
| [**Reps-From**](a-repsfrom.md)                                                  | Falso     | **Top**      |
| [**Reps-To**](a-repsto.md)                                                      | Falso     | **Top**      |
| [**Revisione**](a-revision.md)                                                   | Falso     | **Top**      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falso     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falso     | **Top**      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                   | Falso     | **Top**      |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                         | Falso     | **Top**      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falso     | **Top**      |
| [**Riferimenti secondari**](a-subrefs.md)                                                    | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | **Top**      |
| [**Flag di sistema**](a-systemflags.md)                                            | Falso     | **Top**      |
| [**USN modificato**](a-usnchanged.md)                                              | Falso     | **Top**      |
| [**Creato da USN**](a-usncreated.md)                                              | Falso     | **Top**      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | **Top**      |
| [**USN intersito**](a-usnintersite.md)                                          | Falso     | **Top**      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | **Top**      |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | **Top**      |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | **Top**      |
| [**Oggetti noti**](a-wellknownobjects.md)                                 | Falso     | **Top**      |
| [**Quando viene modificato**](a-whenchanged.md)                                            | Falso     | **Top**      |
| [**Quando creato**](a-whencreated.md)                                            | Falso     | **Top**      |
| [**Www-Home-Page**](a-wwwhomepage.md)                                           | Falso     | **Top**      |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | **Top**      |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributes (Attributi)](#windows-server-2012-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Default-Hiding-Value        | 1                                                                                            |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | **Top**<br/>                                                                           |
| Possibili superiori          | [**Oggetti persi e trovati**](c-lostandfound.md)                                                     |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; Au) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attributi

Questa classe contiene gli attributi seguenti per Windows Server 2012:



| Attributo                                                                                    | Obbligatorio | Derivato da |
|----------------------------------------------------------------------------------------------|-----------|--------------|
| [**Descrizione dell'amministratore**](a-admindescription.md)                                              | Falso     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | **Top**      |
| [**Attributi consentiti**](a-allowedattributes.md)                                            | Falso     | **Top**      |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falso     | **Top**      |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                                       | Falso     | **Top**      |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falso     | **Top**      |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | **Top**      |
| [**Canonical-Name**](a-canonicalname.md)                                                    | Falso     | **Top**      |
| [**Nome comune**](a-cn.md)                                                                  | Falso     | **Top**      |
| [**Creazione timestamp**](a-createtimestamp.md)                                               | Falso     | **Top**      |
| [**Descrizione**](a-description.md)                                                         | Falso     | **Top**      |
| [**Nome visualizzato**](a-displayname.md)                                                        | Falso     | **Top**      |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                     | Falso     | **Top**      |
| [**Firma DSA**](a-dsasignature.md)                                                      | Falso     | **Top**      |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                  | Falso     | **Top**      |
| [**Extension-Name**](a-extensionname.md)                                                    | Falso     | **Top**      |
| [**Bandiere**](a-flags.md)                                                                     | Falso     | **Top**      |
| [**From-Entry**](a-fromentry.md)                                                            | Falso     | **Top**      |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | **Top**      |
| [**Tipo di istanza**](a-instancetype.md)                                                      | Vero      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | **Top**      |
| [**Is-Deleted**](a-isdeleted.md)                                                            | Falso     | **Top**      |
| [**Membro di DL**](a-memberof.md)                                                        | Falso     | **Top**      |
| [**Titolare dei privilegi**](a-isprivilegeholder.md)                                           | Falso     | **Top**      |
| [**Viene riciclato**](a-isrecycled.md)                                                          | Falso     | **Top**      |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                               | Falso     | **Top**      |
| [**Oggetti gestiti**](a-managedobjects.md)                                                  | Falso     | **Top**      |
| [**Mastered-By**](a-masteredby.md)                                                          | Falso     | **Top**      |
| [**Modifica timestamp**](a-modifytimestamp.md)                                               | Falso     | **Top**      |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | **Top**      |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | **Top**      |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | **Top**      |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | **Top**      |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | **Top**      |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | **Top**      |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | **Top**      |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | **Top**      |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | **Top**      |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | **Top**      |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | Falso     | **Top**      |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | **Top**      |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                           | Falso     | **Top**      |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falso     | **Top**      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | **Top**      |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | **Top**      |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falso     | **Top**      |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falso     | **Top**      |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falso     | **Top**      |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | **Top**      |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | **Top**      |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | **Top**      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | **Top**      |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falso     | **Top**      |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | **Top**      |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | **Top**      |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | **Top**      |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | **Top**      |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falso     | **Top**      |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falso     | **Top**      |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falso     | **Top**      |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falso     | **Top**      |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | Falso     | **Top**      |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | **Top**      |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | **Top**      |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | **Top**      |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | **Top**      |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | **Top**      |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | **Top**      |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falso     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | **Top**      |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | **Top**      |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Vero      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | **Top**      |
| [**Categoria di oggetti**](a-objectcategory.md)                                                  | Vero      | **Top**      |
| [**Classe object**](a-objectclass.md)                                                        | Vero      | **Top**      |
| [**Object-Guid**](a-objectguid.md)                                                          | Falso     | **Top**      |
| [**Versione oggetto**](a-objectversion.md)                                                    | Falso     | **Top**      |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                                  | Falso     | **Top**      |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falso     | **Top**      |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | Falso     | **Top**      |
| [**Possibili inevasi**](a-possibleinferiors.md)                                            | Falso     | **Top**      |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falso     | **Top**      |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                  | Falso     | **Top**      |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falso     | **Top**      |
| [**Rdn**](a-name.md)                                                                        | Falso     | **Top**      |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falso     | **Top**      |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | **Top**      |
| [**Report**](a-directreports.md)                                                           | Falso     | **Top**      |
| [**Reps-From**](a-repsfrom.md)                                                              | Falso     | **Top**      |
| [**Reps-To**](a-repsto.md)                                                                  | Falso     | **Top**      |
| [**Revisione**](a-revision.md)                                                               | Falso     | **Top**      |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falso     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falso     | **Top**      |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                               | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | **Top**      |
| [**Classe structural-object**](a-structuralobjectclass.md)                                   | Falso     | **Top**      |
| [**Sottori ref**](a-subrefs.md)                                                                | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | **Top**      |
| [**Flag di sistema**](a-systemflags.md)                                                        | Falso     | **Top**      |
| [**Modifica di USN**](a-usnchanged.md)                                                          | Falso     | **Top**      |
| [**Creato da USN**](a-usncreated.md)                                                          | Falso     | **Top**      |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | Falso     | **Top**      |
| [**USN-Intersite**](a-usnintersite.md)                                                      | Falso     | **Top**      |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falso     | **Top**      |
| [**USN-Source**](a-usnsource.md)                                                            | Falso     | **Top**      |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falso     | **Top**      |
| [**Oggetti noti**](a-wellknownobjects.md)                                             | Falso     | **Top**      |
| [**Quando viene modificato**](a-whenchanged.md)                                                        | Falso     | **Top**      |
| [**Quando viene creato**](a-whencreated.md)                                                        | Falso     | **Top**      |
| [**Www-Home-Page**](a-wwwhomepage.md)                                                       | Falso     | **Top**      |
| [**WWW-Page-Other**](a-url.md)                                                              | Falso     | **Top**      |



 

 





