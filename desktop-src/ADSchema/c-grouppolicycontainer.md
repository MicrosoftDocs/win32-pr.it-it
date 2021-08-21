---
title: Classe Group-Policy-Container
description: Rappresenta l'Criteri di gruppo corrente. Viene usato per definire i criteri di gruppo.
ms.assetid: f57aa609-b1bf-4423-a533-37e5ff768ab5
ms.tgt_platform: multiple
keywords:
- Schema AD della classe Group-Policy-Container
- Schema AD della classe groupPolicyContainer
topic_type:
- apiref
api_name:
- Group-Policy-Container
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c398afc8aca649c0bc5c7a24b31e0e6753b74c40b1cdefbb352e15849ca6633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118011220"
---
# <a name="group-policy-container-class"></a>Classe Group-Policy-Container

Rappresenta l'Criteri di gruppo corrente. Viene usato per definire i criteri di gruppo.



| Voce | Valore |
|-------------------|----------------------------------------------------------|
| CN                | Contenitore criteri di gruppo                                   |
| Ldap-Display-Name | groupPolicyContainer                                     |
| Aggiorna privilegio  | Questo valore viene impostato dall'amministratore del dominio o dei criteri. |
| Frequenza di aggiornamento  | Ogni volta che un oggetto Criteri di gruppo viene aggiornato tramite l'oggetto Criteri di gruppo.               |
| Schema-Id-Guid    | f30e3bc2-9ff0-11d1-b603-0000f80367c1                     |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attributes (Attributi)](#windows-2000-server-attributes)
-   [Diritti estesi](#windows-2000-server-extended-rights)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.157                                                                                                                                                                                                           |
| Default-Hiding-Value        | 1                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                           |
| Sottoclasse di                 | [**Contenitore**](c-container.md)<br/>                                                                                                                                                                                      |
| Possibili superiori          | \-                                                                                                                                                                                                                               |
| Classi ausiliarie           | \-                                                                                                                                                                                                                               |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                     |
| Descrittore di sicurezza predefinito | D:P(A; CI;RPWPCCDCLOLORCWOWDSDDTSW;;;D A)(A; CI;RPWPCCDCLOLORCWOWDSDDTSW;;; EA)(A; CI;RPWPCCDCLOLORCWOWDSDDTSW;;; CO)(A; CI;RPWPCCDCLCLORCWOWDSDDTSW;;; SY)(A; CI;RPLCLORC;;; AU)(OA; CI;CR;edacfd8f-ffb3-11d1-b41d-00a0c968f939;; Au) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                       |



## <a name="windows-2000-server-attributes"></a>attributi del server Windows 2000

Questa classe contiene gli attributi seguenti per Windows 2000 Server:



| Attributo                                                                 | Obbligatorio | Derivato da                                                                |
|---------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------------|
| [**Descrizione dell'amministratore**](a-admindescription.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Attributi consentiti**](a-allowedattributes.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Canonical-Name**](a-canonicalname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Nome comune**](a-cn.md)                                               | Vero      | [**Contenitore**](c-container.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Creazione timestamp**](a-createtimestamp.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Default-Class-Store**](a-defaultclassstore.md)                        | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**Descrizione**](a-description.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Nome visualizzato**](a-displayname.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Display-Name-Printable**](a-displaynameprintable.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Firma DSA**](a-dsasignature.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Extension-Name**](a-extensionname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Bandiere**](a-flags.md)                                                  | Falso     | **Gruppo-Criteri-Contenitore** [ **in alto**](c-top.md)<br/>                  |
| [**From-Entry**](a-fromentry.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**GPC-File-Sys-Path**](a-gpcfilesyspath.md)                             | Falso     | **Group-Policy-Container**                                                  |
| [**GPC-Functionality-Version**](a-gpcfunctionalityversion.md)            | Falso     | **Group-Policy-Container**                                                  |
| [**GPC-Machine-Extension-Names**](a-gpcmachineextensionnames.md)         | Falso     | **Group-Policy-Container**                                                  |
| [**GPC-User-Extension-Names**](a-gpcuserextensionnames.md)               | Falso     | **Group-Policy-Container**                                                  |
| [**Tipo di istanza**](a-instancetype.md)                                   | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Deleted**](a-isdeleted.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Member-Of-DL**](a-memberof.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Titolare del privilegio Is**](a-isprivilegeholder.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetti gestiti**](a-managedobjects.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Mastered-By**](a-masteredby.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Modifica timestamp**](a-modifytimestamp.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Categoria di oggetti**](a-objectcategory.md)                               | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Classe object**](a-objectclass.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Object-Guid**](a-objectguid.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Versione oggetto**](a-objectversion.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md) | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Possibili inevasi**](a-possibleinferiors.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Indirizzi proxy**](a-proxyaddresses.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Rdn**](a-name.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Report**](a-directreports.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Reps-From**](a-repsfrom.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Reps-To**](a-repsto.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Revisione**](a-revision.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Versione dello schema**](a-schemaversion.md)                                 | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Sottori ref**](a-subrefs.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Flag di sistema**](a-systemflags.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Modifica di USN**](a-usnchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Creato da USN**](a-usncreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-Intersite**](a-usnintersite.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-Source**](a-usnsource.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Numero di versione**](a-versionnumber.md)                                 | Falso     | **Group-Policy-Container**                                                  |
| [**Wbem-Path**](a-wbempath.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetti noti**](a-wellknownobjects.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Quando viene modificato**](a-whenchanged.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Quando viene creato**](a-whencreated.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Www-Home-Page**](a-wwwhomepage.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**WWW-Page-Other**](a-url.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |



## <a name="windows-2000-server-extended-rights"></a>Windows 2000 Server Extended Rights

Questa classe contiene i diritti estesi seguenti per Windows 2000 Server:



| Nome comune                                        |
|----------------------------------------------------|
| [**Applica-Criteri di gruppo**](r-apply-group-policy.md) |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributes (Attributi)](#windows-server-2003-attributes)
-   [Diritti estesi](#windows-server-2003-extended-rights)



| Voce | Valore |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.157                                                                                                                                                                                                                               |
| Default-Hiding-Value        | 1                                                                                                                                                                                                                                                    |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                                               |
| Sottoclasse di                 | [**Contenitore**](c-container.md)<br/>                                                                                                                                                                                                          |
| Possibili superiori          | \-                                                                                                                                                                                                                                                   |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                         |
| Descrittore di sicurezza predefinito | D:P(A; CI;RPWPCCDCLCLOLORCWOWDSDDTSW;;;D A)(A; CI;RPWPCCDCLCLOLORCWOWDSDDTSW;; EA)(A; CI;RPWPCCDCLCLOLORCWOWDSDDTSW;; CO)(A; CI;RPWPCCDCLCLORCWOWDSDDTSW;; SY)(A; CI;RPLCLORC;; AU)(OA; CI;CR;edacfd8f-ffb3-11d1-b41d-00a0c968f939;; AU)(A; CI;LCRPLORC;;; ED) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                           |



## <a name="windows-server-2003-attributes"></a>Windows Attributi di Server 2003

Questa classe contiene gli attributi seguenti per Windows Server 2003:



| Attributo                                                                   | Obbligatorio | Derivato da                                                                |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Nome comune**](a-cn.md)                                                 | Vero      | [**Contenitore**](c-container.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Default-Class-Store**](a-defaultclassstore.md)                          | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Extension-Name**](a-extensionname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Bandiere**](a-flags.md)                                                    | Falso     | **Gruppo-Criteri-Contenitore** [ **in alto**](c-top.md)<br/>                  |
| [**From-Entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**GPC-File-Sys-Path**](a-gpcfilesyspath.md)                               | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**GpC-Functionality-Version**](a-gpcfunctionalityversion.md)              | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**GpC-Machine-Extension-Names**](a-gpcmachineextensionnames.md)           | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**GPC-User-Extension-Names**](a-gpcuserextensionnames.md)                 | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**GpC-WQL-Filter**](a-gpcwqlfilter.md)                                    | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Membro di DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Titolare dei privilegi**](a-isprivilegeholder.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Modifica timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ms-DS-Object-Reference**](a-msds-objectreference.md)                    | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Categoria di oggetti**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Classe object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Guid oggetto**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Possibili eserezioni**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Rdn**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Report**](a-directreports.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Versione schema**](a-schemaversion.md)                                   | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN modificato**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Creato da USN**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN -Intersite**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Numero di versione**](a-versionnumber.md)                                   | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Quando viene modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Creazione in data e ora**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Www-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                             |



## <a name="windows-server-2003-extended-rights"></a>Windows Diritti estesi di Server 2003

Questa classe contiene i seguenti diritti estesi per Windows Server 2003:



| Nome comune                                        |
|----------------------------------------------------|
| [**Applica criteri di gruppo**](r-apply-group-policy.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributes (Attributi)](#windows-server-2003-r2-attributes)
-   [Diritti estesi](#windows-server-2003-r2-extended-rights)



| Voce | Valore |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.157                                                                                                                                                                                                                               |
| Default-Hiding-Value        | 1                                                                                                                                                                                                                                                    |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                                               |
| Sottoclasse di                 | [**Contenitore**](c-container.md)<br/>                                                                                                                                                                                                          |
| Possibili superiori          | \-                                                                                                                                                                                                                                                   |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                         |
| Descrittore di sicurezza predefinito | D:P(A; CI;RPWPCCDCLOLORCWOWDSDDTSW;;;D A)(A; CI;RPWPCCDCLOLORCWOWDSDDTSW;;; EA)(A; CI;RPWPCCDCLOLORCWOWDSDDTSW;;; CO)(A; CI;RPWPCCDCLCLORCWOWDSDDTSW;;; SY)(A; CI;RPLCLORC;;; AU)(OA; CI;CR;edacfd8f-ffb3-11d1-b41d-00a0c968f939;; AU)(A; CI;LCRPLORC;;; ED) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                           |



## <a name="windows-server-2003-r2-attributes"></a>Windows Attributi di Server 2003 R2

Questa classe contiene gli attributi seguenti per Windows Server 2003 R2:



| Attributo                                                                   | Obbligatorio | Derivato da                                                                |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------------|
| [**Descrizione dell'amministratore**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Nome comune**](a-cn.md)                                                 | Vero      | [**Contenitore**](c-container.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Default-Class-Store**](a-defaultclassstore.md)                          | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Extension-Name**](a-extensionname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Bandiere**](a-flags.md)                                                    | Falso     | **Gruppo-Criteri-Contenitore** [ **in alto**](c-top.md)<br/>                  |
| [**From-Entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**GPC-File-Sys-Path**](a-gpcfilesyspath.md)                               | Falso     | **Group-Policy-Container**                                                  |
| [**GPC-Functionality-Version**](a-gpcfunctionalityversion.md)              | Falso     | **Group-Policy-Container**                                                  |
| [**GPC-Machine-Extension-Names**](a-gpcmachineextensionnames.md)           | Falso     | **Group-Policy-Container**                                                  |
| [**GPC-User-Extension-Names**](a-gpcuserextensionnames.md)                 | Falso     | **Group-Policy-Container**                                                  |
| [**GPC-WQL-Filter**](a-gpcwqlfilter.md)                                    | Falso     | **Group-Policy-Container**                                                  |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Titolare del privilegio Is**](a-isprivilegeholder.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Modifica timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ms-DS-Object-Reference**](a-msds-objectreference.md)                    | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Categoria di oggetti**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Classe object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Object-Guid**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Possibili inevasi**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Rdn**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Report**](a-directreports.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Versione dello schema**](a-schemaversion.md)                                   | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Classe structural-object**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Sottori ref**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Modifica di USN**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Creato da USN**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Numero di versione**](a-versionnumber.md)                                   | Falso     | **Group-Policy-Container**                                                  |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Quando viene modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Quando viene creato**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Www-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                             |



## <a name="windows-server-2003-r2-extended-rights"></a>Windows Diritti estesi di Server 2003 R2

Questa classe contiene i diritti estesi seguenti per Windows Server 2003 R2:



| Nome comune                                        |
|----------------------------------------------------|
| [**Applica-Criteri di gruppo**](r-apply-group-policy.md) |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributes (Attributi)](#windows-server-2008-attributes)
-   [Diritti estesi](#windows-server-2008-extended-rights)



| Voce | Valore |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.157                                                                                                                                                                                                                               |
| Default-Hiding-Value        | 1                                                                                                                                                                                                                                                    |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                                               |
| Sottoclasse di                 | [**Contenitore**](c-container.md)<br/>                                                                                                                                                                                                          |
| Possibili superiori          | \-                                                                                                                                                                                                                                                   |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                         |
| Descrittore di sicurezza predefinito | D:P(A; CI;RPWPCCDCLOLORCWOWDSDDTSW;;;D A)(A; CI;RPWPCCDCLOLORCWOWDSDDTSW;;; EA)(A; CI;RPWPCCDCLOLORCWOWDSDDTSW;;; CO)(A; CI;RPWPCCDCLCLORCWOWDSDDTSW;;; SY)(A; CI;RPLCLORC;;; AU)(OA; CI;CR;edacfd8f-ffb3-11d1-b41d-00a0c968f939;; AU)(A; CI;LCRPLORC;;; ED) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                           |



## <a name="windows-server-2008-attributes"></a>Windows Attributi di Server 2008

Questa classe contiene gli attributi seguenti per Windows Server 2008:



| Attributo                                                                      | Obbligatorio | Derivato da                                                                |
|--------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------------|
| [**Descrizione dell'amministratore**](a-admindescription.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Attributi consentiti**](a-allowedattributes.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Canonical-Name**](a-canonicalname.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Nome comune**](a-cn.md)                                                    | Vero      | [**Contenitore**](c-container.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Creazione timestamp**](a-createtimestamp.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Default-Class-Store**](a-defaultclassstore.md)                             | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**Descrizione**](a-description.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Nome visualizzato**](a-displayname.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Display-Name-Printable**](a-displaynameprintable.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Firma DSA**](a-dsasignature.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Extension-Name**](a-extensionname.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Bandiere**](a-flags.md)                                                       | Falso     | **Group-Policy-Container** [ **Top**](c-top.md)<br/>                  |
| [**From-Entry**](a-fromentry.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**GPC-File-Sys-Path**](a-gpcfilesyspath.md)                                  | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**GpC-Functionality-Version**](a-gpcfunctionalityversion.md)                 | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**GpC-Machine-Extension-Names**](a-gpcmachineextensionnames.md)              | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**GPC-User-Extension-Names**](a-gpcuserextensionnames.md)                    | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**GpC-WQL-Filter**](a-gpcwqlfilter.md)                                       | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**Tipo di istanza**](a-instancetype.md)                                        | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Deleted**](a-isdeleted.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Member-Of-DL**](a-memberof.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Titolare di privilegi is**](a-isprivilegeholder.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetti gestiti**](a-managedobjects.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Mastered-By**](a-masteredby.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Modifica timestamp**](a-modifytimestamp.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ms-DS-Object-Reference**](a-msds-objectreference.md)                       | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Categoria di oggetti**](a-objectcategory.md)                                    | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Classe object**](a-objectclass.md)                                          | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Object-Guid**](a-objectguid.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Versione oggetto**](a-objectversion.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Possibili inevasi**](a-possibleinferiors.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Rdn**](a-name.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Report**](a-directreports.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Reps-From**](a-repsfrom.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Reps-To**](a-repsto.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Revisione**](a-revision.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Versione dello schema**](a-schemaversion.md)                                      | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Riferimenti secondari**](a-subrefs.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Flag di sistema**](a-systemflags.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN modificato**](a-usnchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Creato da USN**](a-usncreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN intersito**](a-usnintersite.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-Source**](a-usnsource.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Numero di versione**](a-versionnumber.md)                                      | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**Wbem-Path**](a-wbempath.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetti noti**](a-wellknownobjects.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Quando viene modificato**](a-whenchanged.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Quando creato**](a-whencreated.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Www-Home-Page**](a-wwwhomepage.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**WWW-Page-Other**](a-url.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                             |



## <a name="windows-server-2008-extended-rights"></a>Windows Diritti estesi di Server 2008

Questa classe contiene i seguenti diritti estesi per Windows Server 2008:



| Nome comune                                        |
|----------------------------------------------------|
| [**Applica criteri di gruppo**](r-apply-group-policy.md) |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributes (Attributi)](#windows-server-2008-r2-attributes)
-   [Diritti estesi](#windows-server-2008-r2-extended-rights)



| Voce | Valore |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.157                                                                                                                                                                                                                               |
| Default-Hiding-Value        | 1                                                                                                                                                                                                                                                    |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                                               |
| Sottoclasse di                 | [**Contenitore**](c-container.md)<br/>                                                                                                                                                                                                          |
| Possibili superiori          | \-                                                                                                                                                                                                                                                   |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                         |
| Descrittore di sicurezza predefinito | D:P(A; CI;RPWPCCDCLOLORCWOWDSDDTSW;;;D A)(A; CI;RPWPCCDCLOLORCWOWDSDDTSW;;; EA)(A; CI;RPWPCCDCLOLORCWOWDSDDTSW;;; CO)(A; CI;RPWPCCDCLCLORCWOWDSDDTSW;;; SY)(A; CI;RPLCLORC;;; AU)(OA; CI;CR;edacfd8f-ffb3-11d1-b41d-00a0c968f939;; AU)(A; CI;LCRPLORC;;; ED) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                           |



## <a name="windows-server-2008-r2-attributes"></a>Windows Attributi di Server 2008 R2

Questa classe contiene gli attributi seguenti per Windows Server 2008 R2:



| Attributo                                                                        | Obbligatorio | Derivato da                                                                |
|----------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------------|
| [**Descrizione dell'amministratore**](a-admindescription.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Attributi consentiti**](a-allowedattributes.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Canonical-Name**](a-canonicalname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Nome comune**](a-cn.md)                                                      | Vero      | [**Contenitore**](c-container.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Default-Class-Store**](a-defaultclassstore.md)                               | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**Descrizione**](a-description.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Nome visualizzato**](a-displayname.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Firma DSA**](a-dsasignature.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Extension-Name**](a-extensionname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Bandiere**](a-flags.md)                                                         | Falso     | **Gruppo-Criteri-Contenitore** [ **in alto**](c-top.md)<br/>                  |
| [**From-Entry**](a-fromentry.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**GPC-File-Sys-Path**](a-gpcfilesyspath.md)                                    | Falso     | **Group-Policy-Container**                                                  |
| [**GPC-Functionality-Version**](a-gpcfunctionalityversion.md)                   | Falso     | **Group-Policy-Container**                                                  |
| [**GPC-Machine-Extension-Names**](a-gpcmachineextensionnames.md)                | Falso     | **Group-Policy-Container**                                                  |
| [**GPC-User-Extension-Names**](a-gpcuserextensionnames.md)                      | Falso     | **Group-Policy-Container**                                                  |
| [**GPC-WQL-Filter**](a-gpcwqlfilter.md)                                         | Falso     | **Group-Policy-Container**                                                  |
| [**Tipo di istanza**](a-instancetype.md)                                          | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Member-Of-DL**](a-memberof.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Titolare del privilegio Is**](a-isprivilegeholder.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Recycled**](a-isrecycled.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetti gestiti**](a-managedobjects.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Modifica timestamp**](a-modifytimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ms-DS-Object-Reference**](a-msds-objectreference.md)                         | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Categoria di oggetti**](a-objectcategory.md)                                      | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Classe object**](a-objectclass.md)                                            | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Guid oggetto**](a-objectguid.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Versione oggetto**](a-objectversion.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Possibili eserezioni**](a-possibleinferiors.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Rdn**](a-name.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Report**](a-directreports.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Reps-From**](a-repsfrom.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Reps-To**](a-repsto.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Revisione**](a-revision.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Versione schema**](a-schemaversion.md)                                        | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Riferimenti secondari**](a-subrefs.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Flag di sistema**](a-systemflags.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN modificato**](a-usnchanged.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Creato da USN**](a-usncreated.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN intersito**](a-usnintersite.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Numero di versione**](a-versionnumber.md)                                        | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetti noti**](a-wellknownobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Quando viene modificato**](a-whenchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Quando creato**](a-whencreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Www-Home-Page**](a-wwwhomepage.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |



## <a name="windows-server-2008-r2-extended-rights"></a>Windows Diritti estesi di Server 2008 R2

Questa classe contiene i seguenti diritti estesi per Windows Server 2008 R2:



| Nome comune                                        |
|----------------------------------------------------|
| [**Applica criteri di gruppo**](r-apply-group-policy.md) |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributes (Attributi)](#windows-server-2012-attributes)
-   [Diritti estesi](#windows-server-2012-extended-rights)



| Voce | Valore |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.157                                                                                                                                                                                                                               |
| Default-Hiding-Value        | 1                                                                                                                                                                                                                                                    |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                                               |
| Sottoclasse di                 | [**Contenitore**](c-container.md)<br/>                                                                                                                                                                                                          |
| Possibili superiori          | \-                                                                                                                                                                                                                                                   |
| Classi ausiliarie           | \-                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                         |
| Descrittore di sicurezza predefinito | D:P(A; CI;RPWPCCDCLOLORCWOWDSDDTSW;;;D A)(A; CI;RPWPCCDCLOLORCWOWDSDDTSW;;; EA)(A; CI;RPWPCCDCLOLORCWOWDSDDTSW;;; CO)(A; CI;RPWPCCDCLCLORCWOWDSDDTSW;;; SY)(A; CI;RPLCLORC;;; AU)(OA; CI;CR;edacfd8f-ffb3-11d1-b41d-00a0c968f939;; AU)(A; CI;LCRPLORC;;; ED) |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                           |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attributi

Questa classe contiene gli attributi seguenti per Windows Server 2012:



| Attributo                                                                                    | Obbligatorio | Derivato da                                                                |
|----------------------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------------|
| [**Descrizione dell'amministratore**](a-admindescription.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Attributi consentiti**](a-allowedattributes.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Canonical-Name**](a-canonicalname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Nome comune**](a-cn.md)                                                                  | Vero      | [**Contenitore**](c-container.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Creazione timestamp**](a-createtimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Default-Class-Store**](a-defaultclassstore.md)                                           | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**Descrizione**](a-description.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Nome visualizzato**](a-displayname.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Firma DSA**](a-dsasignature.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Extension-Name**](a-extensionname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Bandiere**](a-flags.md)                                                                     | Falso     | **Group-Policy-Container** [ **Top**](c-top.md)<br/>                  |
| [**From-Entry**](a-fromentry.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**GPC-File-Sys-Path**](a-gpcfilesyspath.md)                                                | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**GpC-Functionality-Version**](a-gpcfunctionalityversion.md)                               | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**GpC-Machine-Extension-Names**](a-gpcmachineextensionnames.md)                            | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**GPC-User-Extension-Names**](a-gpcuserextensionnames.md)                                  | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**GpC-WQL-Filter**](a-gpcwqlfilter.md)                                                     | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**Tipo di istanza**](a-instancetype.md)                                                      | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Is-Deleted**](a-isdeleted.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Membro di DL**](a-memberof.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Titolare dei privilegi**](a-isprivilegeholder.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Viene riciclato**](a-isrecycled.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetti gestiti**](a-managedobjects.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Mastered-By**](a-masteredby.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Modifica timestamp**](a-modifytimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-is-Domain-For**](a-msds-isdomainfor.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ms-DS-Object-Reference**](a-msds-objectreference.md)                                     | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Categoria di oggetti**](a-objectcategory.md)                                                  | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Classe object**](a-objectclass.md)                                                        | Vero      | [**In alto**](c-top.md)<br/>                                             |
| [**Object-Guid**](a-objectguid.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Versione oggetto**](a-objectversion.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Possibili inevasi**](a-possibleinferiors.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Rdn**](a-name.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Report**](a-directreports.md)                                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Reps-From**](a-repsfrom.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Reps-To**](a-repsto.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Revisione**](a-revision.md)                                                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Versione schema**](a-schemaversion.md)                                                    | Falso     | [**Contenitore**](c-container.md)<br/>                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Riferimenti secondari**](a-subrefs.md)                                                                | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Flag di sistema**](a-systemflags.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN modificato**](a-usnchanged.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Creato da USN**](a-usncreated.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN -Intersite**](a-usnintersite.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**USN-Source**](a-usnsource.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Numero di versione**](a-versionnumber.md)                                                    | Falso     | **Contenitore criteri di gruppo**                                                  |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Oggetti noti**](a-wellknownobjects.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Quando viene modificato**](a-whenchanged.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Creazione in data e ora**](a-whencreated.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**Www-Home-Page**](a-wwwhomepage.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                             |
| [**WWW-Page-Other**](a-url.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                             |



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012 Diritti estesi

Questa classe contiene i seguenti diritti estesi per Windows Server 2012:



| Nome comune                                        |
|----------------------------------------------------|
| [**Applica criteri di gruppo**](r-apply-group-policy.md) |



 

 





