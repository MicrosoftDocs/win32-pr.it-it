---
title: Classe MS-DFSR-LocalSettings
description: Contiene le impostazioni del servizio di replica file system distribuito (DFS) applicabili al computer locale.
ms.assetid: a7e57bd9-2b02-4d3c-bc05-f4d53e92567d
ms.tgt_platform: multiple
keywords:
- Schema di Active Directory della classe MS-DFSR-LocalSettings
- msDFSR-schema di Active Directory della classe LocalSettings
topic_type:
- apiref
api_name:
- ms-DFSR-LocalSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bc9cf3d7d4858aae2062ee937b523d2704a8f99
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744050"
---
# <a name="ms-dfsr-localsettings-class"></a>Classe MS-DFSR-LocalSettings

Contiene le impostazioni del servizio di replica file system distribuito (DFS) applicabili al computer locale.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | MS-DFSR-LocalSettings                |
| LDAP-Display-Name | msDFSR-LocalSettings                 |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Schema-ID-GUID    | fa85c591-197f-477e-83bd-ea5a43df2239 |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributes (Attributi)](#windows-server-2003-r2-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                            |
| Object-Category             | 1                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.6.13.4.1                                                                                                        |
| Valore predefinito-nascondiglio        | 1                                                                                                                                |
| RDN-att-ID                  | \-                                                                                                                               |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                  |
| Possibili superiori          | [**Computer**](c-computer.md)                                                                                                   |
| Classi ausiliarie           | \-                                                                                                                               |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                     |
| Descrittore di sicurezza predefinito | D: (A;; RPLCLORC;;; AU) (A;; RPWPCRLCLOCCDCRCWDWOSDDTSW;;;D A) (A;; RPWPCRLCLOCCDCRCWDWOSDDTSW;;; CO) (A;; RPWPCRLCLOCCDCRCWDWOSDDTSW;;; SY |
| System-Flags                | 0x00000000                                                                                                                       |



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
| [**Nome canonico**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**DSA-firma**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome estensione**](a-extensionname.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Bandiere**](a-flags.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da-entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Viene eliminato**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-by**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica-timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-Extension**](a-msdfsr-extension.md)                             | Falso     | **MS-DFSR-LocalSettings**       |
| [**Flag MS-DFSR**](a-msdfsr-flags.md)                                     | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-Options**](a-msdfsr-options.md)                                 | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-Version**](a-msdfsr-version.md)                                 | Falso     | **MS-DFSR-LocalSettings**       |
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
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Set di attributi parziali**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Possibili-inferiori**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-criteri-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-da**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da Reps a**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
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



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributes (Attributi)](#windows-server-2008-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                            |
| Object-Category             | 1                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.6.13.4.1                                                                                                        |
| Valore predefinito-nascondiglio        | 1                                                                                                                                |
| RDN-att-ID                  | \-                                                                                                                               |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                  |
| Possibili superiori          | [**Computer**](c-computer.md)                                                                                                   |
| Classi ausiliarie           | \-                                                                                                                               |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                     |
| Descrittore di sicurezza predefinito | D: (A;; RPLCLORC;;; AU) (A;; RPWPCRLCLOCCDCRCWDWOSDDTSW;;;D A) (A;; RPWPCRLCLOCCDCRCWDWOSDDTSW;;; CO) (A;; RPWPCRLCLOCCDCRCWDWOSDDTSW;;; SY |
| System-Flags                | 0x00000000                                                                                                                       |



## <a name="windows-server-2008-attributes"></a>Attributi di Windows Server 2008

Questa classe contiene gli attributi seguenti per Windows Server 2008:



| Attributo                                                                                 | Obbligatorio | Derivato da                    |
|-------------------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome canonico**](a-canonicalname.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creazione timestamp**](a-createtimestamp.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Descrizione**](a-description.md)                                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome visualizzato**](a-displayname.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**DSA-firma**](a-dsasignature.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome estensione**](a-extensionname.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Bandiere**](a-flags.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da-entry**](a-fromentry.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Tipo di istanza**](a-instancetype.md)                                                   | Vero      | [**In alto**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Viene eliminato**](a-isdeleted.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-member-of-DL**](a-memberof.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti gestiti**](a-managedobjects.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-by**](a-masteredby.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-CommonStagingPath**](a-msdfsr-commonstagingpath.md)                           | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-CommonStagingSizeInMb**](a-msdfsr-commonstagingsizeinmb.md)                   | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-Extension**](a-msdfsr-extension.md)                                           | Falso     | **MS-DFSR-LocalSettings**       |
| [**Flag MS-DFSR**](a-msdfsr-flags.md)                                                   | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-Options**](a-msdfsr-options.md)                                               | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-Options2**](a-msdfsr-options2.md)                                             | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-StagingCleanupTriggerInPercent**](a-msdfsr-stagingcleanuptriggerinpercent.md) | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-Version**](a-msdfsr-version.md)                                               | Falso     | **MS-DFSR-LocalSettings**       |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md)            | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**-SCP-BL**](a-netbootscpbl.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                                  | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria oggetto**](a-objectcategory.md)                                               | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe Object**](a-objectclass.md)                                                     | Vero      | [**In alto**](c-top.md)<br/> |
| [**GUID oggetto**](a-objectguid.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Set di attributi parziali**](a-partialattributeset.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Possibili-inferiori**](a-possibleinferiors.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-criteri-BL**](a-querypolicybl.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-da**](a-repsfrom.md)                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da Reps a**](a-repsto.md)                                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riferimenti secondari**](a-subrefs.md)                                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-modificato**](a-usnchanged.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN creato**](a-usncreated.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-tra siti**](a-usnintersite.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-origine**](a-usnsource.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**WBEM-percorso**](a-wbempath.md)                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando-modificato**](a-whenchanged.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Data di creazione**](a-whencreated.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-pagina-altro**](a-url.md)                                                           | Falso     | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributes (Attributi)](#windows-server-2008-r2-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                            |
| Object-Category             | 1                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.6.13.4.1                                                                                                        |
| Valore predefinito-nascondiglio        | 1                                                                                                                                |
| RDN-att-ID                  | \-                                                                                                                               |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                  |
| Possibili superiori          | [**Computer**](c-computer.md)                                                                                                   |
| Classi ausiliarie           | \-                                                                                                                               |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                     |
| Descrittore di sicurezza predefinito | D: (A;; RPLCLORC;;; AU) (A;; RPWPCRLCLOCCDCRCWDWOSDDTSW;;;D A) (A;; RPWPCRLCLOCCDCRCWDWOSDDTSW;;; CO) (A;; RPWPCRLCLOCCDCRCWDWOSDDTSW;;; SY |
| System-Flags                | 0x00000000                                                                                                                       |



## <a name="windows-server-2008-r2-attributes"></a>Attributi di Windows Server 2008 R2

Questa classe contiene gli attributi seguenti per Windows Server 2008 R2:



| Attributo                                                                                 | Obbligatorio | Derivato da                    |
|-------------------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome canonico**](a-canonicalname.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creazione timestamp**](a-createtimestamp.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Descrizione**](a-description.md)                                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome visualizzato**](a-displayname.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**DSA-firma**](a-dsasignature.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome estensione**](a-extensionname.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Bandiere**](a-flags.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da-entry**](a-fromentry.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Tipo di istanza**](a-instancetype.md)                                                   | Vero      | [**In alto**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Viene eliminato**](a-isdeleted.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-member-of-DL**](a-memberof.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riciclato**](a-isrecycled.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti gestiti**](a-managedobjects.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-by**](a-masteredby.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-CommonStagingPath**](a-msdfsr-commonstagingpath.md)                           | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-CommonStagingSizeInMb**](a-msdfsr-commonstagingsizeinmb.md)                   | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-Extension**](a-msdfsr-extension.md)                                           | Falso     | **MS-DFSR-LocalSettings**       |
| [**Flag MS-DFSR**](a-msdfsr-flags.md)                                                   | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-Options**](a-msdfsr-options.md)                                               | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-Options2**](a-msdfsr-options2.md)                                             | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-StagingCleanupTriggerInPercent**](a-msdfsr-stagingcleanuptriggerinpercent.md) | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-Version**](a-msdfsr-version.md)                                               | Falso     | **MS-DFSR-LocalSettings**       |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md)            | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Enabled-feature-BL**](a-msds-enabledfeaturebl.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-host-Service-account-BL**](a-msds-hostserviceaccountbl.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-ultimo-noto-RDN**](a-msds-lastknownrdn.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-locale-effettivo-eliminazione-ora**](a-msds-localeffectivedeletiontime.md)          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-local-effective-riciclo-tempo**](a-msds-localeffectiverecycletime.md)            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**-SCP-BL**](a-netbootscpbl.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                                  | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria oggetto**](a-objectcategory.md)                                               | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe Object**](a-objectclass.md)                                                     | Vero      | [**In alto**](c-top.md)<br/> |
| [**GUID oggetto**](a-objectguid.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Set di attributi parziali**](a-partialattributeset.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Possibili-inferiori**](a-possibleinferiors.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-criteri-BL**](a-querypolicybl.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-da**](a-repsfrom.md)                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da Reps a**](a-repsto.md)                                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riferimenti secondari**](a-subrefs.md)                                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-modificato**](a-usnchanged.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN creato**](a-usncreated.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-tra siti**](a-usnintersite.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-origine**](a-usnsource.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**WBEM-percorso**](a-wbempath.md)                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando-modificato**](a-whenchanged.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Data di creazione**](a-whencreated.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-pagina-altro**](a-url.md)                                                           | Falso     | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributes (Attributi)](#windows-server-2012-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                            |
| Object-Category             | 1                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.6.13.4.1                                                                                                        |
| Valore predefinito-nascondiglio        | 1                                                                                                                                |
| RDN-att-ID                  | \-                                                                                                                               |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                  |
| Possibili superiori          | [**Computer**](c-computer.md)                                                                                                   |
| Classi ausiliarie           | \-                                                                                                                               |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                     |
| Descrittore di sicurezza predefinito | D: (A;; RPLCLORC;;; AU) (A;; RPWPCRLCLOCCDCRCWDWOSDDTSW;;;D A) (A;; RPWPCRLCLOCCDCRCWDWOSDDTSW;;; CO) (A;; RPWPCRLCLOCCDCRCWDWOSDDTSW;;; SY |
| System-Flags                | 0x00000000                                                                                                                       |



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
| [**Nome canonico**](a-canonicalname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creazione timestamp**](a-createtimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Descrizione**](a-description.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome visualizzato**](a-displayname.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**DSA-firma**](a-dsasignature.md)                                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome estensione**](a-extensionname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Bandiere**](a-flags.md)                                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da-entry**](a-fromentry.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Tipo di istanza**](a-instancetype.md)                                                      | Vero      | [**In alto**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Viene eliminato**](a-isdeleted.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-member-of-DL**](a-memberof.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riciclato**](a-isrecycled.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti gestiti**](a-managedobjects.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-by**](a-masteredby.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-CommonStagingPath**](a-msdfsr-commonstagingpath.md)                              | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-CommonStagingSizeInMb**](a-msdfsr-commonstagingsizeinmb.md)                      | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-Extension**](a-msdfsr-extension.md)                                              | Falso     | **MS-DFSR-LocalSettings**       |
| [**Flag MS-DFSR**](a-msdfsr-flags.md)                                                      | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DFSR-Options**](a-msdfsr-options.md)                                                  | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-Options2**](a-msdfsr-options2.md)                                                | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-StagingCleanupTriggerInPercent**](a-msdfsr-stagingcleanuptriggerinpercent.md)    | Falso     | **MS-DFSR-LocalSettings**       |
| [**MS-DFSR-Version**](a-msdfsr-version.md)                                                  | Falso     | **MS-DFSR-LocalSettings**       |
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
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Set di attributi parziali**](a-partialattributeset.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Possibili-inferiori**](a-possibleinferiors.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-criteri-BL**](a-querypolicybl.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-da**](a-repsfrom.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Da Reps a**](a-repsto.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riferimenti secondari**](a-subrefs.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
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



## <a name="remarks"></a>Commenti

La classe **MS-DFSR-LocalSettings** fa parte del supporto del servizio Replica DFS.

 

 





