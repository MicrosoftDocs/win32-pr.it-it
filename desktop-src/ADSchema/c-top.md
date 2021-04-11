---
title: Classe Top
description: Classe di primo livello dalla quale vengono derivate tutte le classi.
ms.assetid: 025aff6c-1804-4141-accf-d50cfd50e90e
ms.tgt_platform: multiple
keywords:
- Primo schema di Active Class
- primo schema di Active Class
topic_type:
- apiref
api_name:
- Top
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01cd6a72dfba6a80687081d503864c88fd1c5122
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104121806"
---
# <a name="top-class"></a>Classe Top

Classe di primo livello dalla quale vengono derivate tutte le classi.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Inizio                                  |
| LDAP-Display-Name | top                                  |
| Privilegio aggiornamento  | Amministratore schema                 |
| Frequenza di aggiornamento  | \-                                   |
| Schema-ID-GUID    | bf967ab7-0de6-11d0-a285-00aa003049e2 |



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
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valore predefinito-nascondiglio        | 1                                                                                            |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | **Top**<br/>                                                                           |
| Possibili superiori          | [**Perso e trovato**](c-lostandfound.md)                                                     |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                 |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Attributi del server Windows 2000

Questa classe contiene gli attributi seguenti per Windows 2000 Server:



| Attributo                                                                 | Obbligatorio | Derivato da |
|---------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Descrizione**](a-admindescription.md)                           | Falso     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Falso     | **Top**      |
| [**Attributi consentiti**](a-allowedattributes.md)                         | Falso     | **Top**      |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)      | Falso     | **Top**      |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                    | Falso     | **Top**      |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md) | Falso     | **Top**      |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)             | Falso     | **Top**      |
| [**Nome canonico**](a-canonicalname.md)                                 | Falso     | **Top**      |
| [**Nome comune**](a-cn.md)                                               | Falso     | **Top**      |
| [**Creazione timestamp**](a-createtimestamp.md)                            | Falso     | **Top**      |
| [**Descrizione**](a-description.md)                                      | Falso     | **Top**      |
| [**Nome visualizzato**](a-displayname.md)                                     | Falso     | **Top**      |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                  | Falso     | **Top**      |
| [**DSA-firma**](a-dsasignature.md)                                   | Falso     | **Top**      |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)               | Falso     | **Top**      |
| [**Nome estensione**](a-extensionname.md)                                 | Falso     | **Top**      |
| [**Bandiere**](a-flags.md)                                                  | Falso     | **Top**      |
| [**Da-entry**](a-fromentry.md)                                         | Falso     | **Top**      |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | **Top**      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falso     | **Top**      |
| [**Tipo di istanza**](a-instancetype.md)                                   | Vero      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falso     | **Top**      |
| [**Viene eliminato**](a-isdeleted.md)                                         | Falso     | **Top**      |
| [**Is-member-of-DL**](a-memberof.md)                                     | Falso     | **Top**      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | Falso     | **Top**      |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                            | Falso     | **Top**      |
| [**Oggetti gestiti**](a-managedobjects.md)                               | Falso     | **Top**      |
| [**Mastered-by**](a-masteredby.md)                                       | Falso     | **Top**      |
| [**Modifica-timestamp**](a-modifytimestamp.md)                            | Falso     | **Top**      |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)    | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | **Top**      |
| [**-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | **Top**      |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                   | Falso     | **Top**      |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                  | Vero      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falso     | **Top**      |
| [**Categoria oggetto**](a-objectcategory.md)                               | Vero      | **Top**      |
| [**Classe Object**](a-objectclass.md)                                     | Vero      | **Top**      |
| [**GUID oggetto**](a-objectguid.md)                                       | Falso     | **Top**      |
| [**Versione oggetto**](a-objectversion.md)                                 | Falso     | **Top**      |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)               | Falso     | **Top**      |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md) | Falso     | **Top**      |
| [**Set di attributi parziali**](a-partialattributeset.md)                    | Falso     | **Top**      |
| [**Possibili-inferiori**](a-possibleinferiors.md)                         | Falso     | **Top**      |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                        | Falso     | **Top**      |
| [**Indirizzi proxy**](a-proxyaddresses.md)                               | Falso     | **Top**      |
| [**Query-criteri-BL**](a-querypolicybl.md)                                | Falso     | **Top**      |
| [**RDN**](a-name.md)                                                     | Falso     | **Top**      |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                 | Falso     | **Top**      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                      | Falso     | **Top**      |
| [**Report**](a-directreports.md)                                        | Falso     | **Top**      |
| [**Reps-da**](a-repsfrom.md)                                           | Falso     | **Top**      |
| [**Da Reps a**](a-repsto.md)                                               | Falso     | **Top**      |
| [**Revisione**](a-revision.md)                                            | Falso     | **Top**      |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                        | Falso     | **Top**      |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                        | Falso     | **Top**      |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)            | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | **Top**      |
| [**Riferimenti secondari**](a-subrefs.md)                                             | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | **Top**      |
| [**Flag di sistema**](a-systemflags.md)                                     | Falso     | **Top**      |
| [**USN-modificato**](a-usnchanged.md)                                       | Falso     | **Top**      |
| [**USN creato**](a-usncreated.md)                                       | Falso     | **Top**      |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                | Falso     | **Top**      |
| [**USN-tra siti**](a-usnintersite.md)                                   | Falso     | **Top**      |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                               | Falso     | **Top**      |
| [**USN-origine**](a-usnsource.md)                                         | Falso     | **Top**      |
| [**WBEM-percorso**](a-wbempath.md)                                           | Falso     | **Top**      |
| [**Oggetti noti**](a-wellknownobjects.md)                          | Falso     | **Top**      |
| [**Quando-modificato**](a-whenchanged.md)                                     | Falso     | **Top**      |
| [**Data di creazione**](a-whencreated.md)                                     | Falso     | **Top**      |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                    | Falso     | **Top**      |
| [**WWW-pagina-altro**](a-url.md)                                           | Falso     | **Top**      |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributes (Attributi)](#windows-server-2003-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valore predefinito-nascondiglio        | 1                                                                                            |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | **Top**<br/>                                                                           |
| Possibili superiori          | [**Perso e trovato**](c-lostandfound.md)                                                     |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                 |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Attributi di Windows Server 2003

Questa classe contiene gli attributi seguenti per Windows Server 2003:



| Attributo                                                                   | Obbligatorio | Derivato da |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Descrizione**](a-admindescription.md)                             | Falso     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | **Top**      |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | **Top**      |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)        | Falso     | **Top**      |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | **Top**      |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)   | Falso     | **Top**      |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)               | Falso     | **Top**      |
| [**Nome canonico**](a-canonicalname.md)                                   | Falso     | **Top**      |
| [**Nome comune**](a-cn.md)                                                 | Falso     | **Top**      |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | **Top**      |
| [**Descrizione**](a-description.md)                                        | Falso     | **Top**      |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | **Top**      |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                    | Falso     | **Top**      |
| [**DSA-firma**](a-dsasignature.md)                                     | Falso     | **Top**      |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                 | Falso     | **Top**      |
| [**Nome estensione**](a-extensionname.md)                                   | Falso     | **Top**      |
| [**Bandiere**](a-flags.md)                                                    | Falso     | **Top**      |
| [**Da-entry**](a-fromentry.md)                                           | Falso     | **Top**      |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | **Top**      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | **Top**      |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | **Top**      |
| [**Viene eliminato**](a-isdeleted.md)                                           | Falso     | **Top**      |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | **Top**      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | **Top**      |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | **Top**      |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | **Top**      |
| [**Mastered-by**](a-masteredby.md)                                         | Falso     | **Top**      |
| [**Modifica-timestamp**](a-modifytimestamp.md)                              | Falso     | **Top**      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | **Top**      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | **Top**      |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | **Top**      |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)      | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | **Top**      |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                              | Falso     | **Top**      |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | **Top**      |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                       | Falso     | **Top**      |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | **Top**      |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | **Top**      |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                         | Falso     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | **Top**      |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | **Top**      |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)              | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | **Top**      |
| [**-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | **Top**      |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | **Top**      |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                    | Vero      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | **Top**      |
| [**Categoria oggetto**](a-objectcategory.md)                                 | Vero      | **Top**      |
| [**Classe Object**](a-objectclass.md)                                       | Vero      | **Top**      |
| [**GUID oggetto**](a-objectguid.md)                                         | Falso     | **Top**      |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | **Top**      |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                 | Falso     | **Top**      |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)   | Falso     | **Top**      |
| [**Set di attributi parziali**](a-partialattributeset.md)                      | Falso     | **Top**      |
| [**Possibili-inferiori**](a-possibleinferiors.md)                           | Falso     | **Top**      |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                          | Falso     | **Top**      |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | **Top**      |
| [**Query-criteri-BL**](a-querypolicybl.md)                                  | Falso     | **Top**      |
| [**RDN**](a-name.md)                                                       | Falso     | **Top**      |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                   | Falso     | **Top**      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | **Top**      |
| [**Report**](a-directreports.md)                                          | Falso     | **Top**      |
| [**Reps-da**](a-repsfrom.md)                                             | Falso     | **Top**      |
| [**Da Reps a**](a-repsto.md)                                                 | Falso     | **Top**      |
| [**Revisione**](a-revision.md)                                              | Falso     | **Top**      |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                          | Falso     | **Top**      |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                          | Falso     | **Top**      |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)              | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | **Top**      |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                  | Falso     | **Top**      |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | **Top**      |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | **Top**      |
| [**USN-modificato**](a-usnchanged.md)                                         | Falso     | **Top**      |
| [**USN creato**](a-usncreated.md)                                         | Falso     | **Top**      |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                  | Falso     | **Top**      |
| [**USN-tra siti**](a-usnintersite.md)                                     | Falso     | **Top**      |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | **Top**      |
| [**USN-origine**](a-usnsource.md)                                           | Falso     | **Top**      |
| [**WBEM-percorso**](a-wbempath.md)                                             | Falso     | **Top**      |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | **Top**      |
| [**Quando-modificato**](a-whenchanged.md)                                       | Falso     | **Top**      |
| [**Data di creazione**](a-whencreated.md)                                       | Falso     | **Top**      |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                      | Falso     | **Top**      |
| [**WWW-pagina-altro**](a-url.md)                                             | Falso     | **Top**      |



## <a name="adam"></a>ADAM

-   [Attributes (Attributi)](#adam-attributes)



| Voce | Valore |
|-----------------------------|------------------------------------------|
| System-Only                 | Vero                                     |
| Object-Category             | 2                                        |
| Default-Object-Category     | \-                                       |
| Governs-Id                  | 2.5.6.0                                  |
| Valore predefinito-nascondiglio        | 1                                        |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>   |
| Sottoclasse di                 | **Top**<br/>                       |
| Possibili superiori          | [**Perso e trovato**](c-lostandfound.md) |
| Classi ausiliarie           | \-                                       |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                             |
| Descrittore di sicurezza predefinito | D:S                                     |
| System-Flags                | 0x00000010                               |



## <a name="adam-attributes"></a>Attributi ADAM

Questa classe contiene gli attributi seguenti per ADAM:



| Attributo                                                                   | Obbligatorio | Derivato da |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Descrizione**](a-admindescription.md)                             | Falso     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | **Top**      |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | **Top**      |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)        | Falso     | **Top**      |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | **Top**      |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)   | Falso     | **Top**      |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)               | Falso     | **Top**      |
| [**Nome canonico**](a-canonicalname.md)                                   | Falso     | **Top**      |
| [**Nome comune**](a-cn.md)                                                 | Falso     | **Top**      |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | **Top**      |
| [**Descrizione**](a-description.md)                                        | Falso     | **Top**      |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | **Top**      |
| [**DSA-firma**](a-dsasignature.md)                                     | Falso     | **Top**      |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                 | Falso     | **Top**      |
| [**Da-entry**](a-fromentry.md)                                           | Falso     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | **Top**      |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | **Top**      |
| [**Viene eliminato**](a-isdeleted.md)                                           | Falso     | **Top**      |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | **Top**      |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | **Top**      |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | **Top**      |
| [**Mastered-by**](a-masteredby.md)                                         | Falso     | **Top**      |
| [**Modifica-timestamp**](a-modifytimestamp.md)                              | Falso     | **Top**      |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | **Top**      |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)      | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | **Top**      |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)      | Falso     | **Top**      |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                              | Falso     | **Top**      |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                       | Falso     | **Top**      |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | **Top**      |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | **Top**      |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | **Top**      |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)              | Falso     | **Top**      |
| [**ms-DS-service-account-BL**](a-msds-serviceaccountbl.md)                 | Falso     | **Top**      |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                    | Vero      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | **Top**      |
| [**Categoria oggetto**](a-objectcategory.md)                                 | Vero      | **Top**      |
| [**Classe Object**](a-objectclass.md)                                       | Vero      | **Top**      |
| [**GUID oggetto**](a-objectguid.md)                                         | Falso     | **Top**      |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | **Top**      |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                 | Falso     | **Top**      |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)   | Falso     | **Top**      |
| [**Set di attributi parziali**](a-partialattributeset.md)                      | Falso     | **Top**      |
| [**Possibili-inferiori**](a-possibleinferiors.md)                           | Falso     | **Top**      |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                          | Falso     | **Top**      |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | **Top**      |
| [**Query-criteri-BL**](a-querypolicybl.md)                                  | Falso     | **Top**      |
| [**RDN**](a-name.md)                                                       | Falso     | **Top**      |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                   | Falso     | **Top**      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | **Top**      |
| [**Reps-da**](a-repsfrom.md)                                             | Falso     | **Top**      |
| [**Da Reps a**](a-repsto.md)                                                 | Falso     | **Top**      |
| [**Revisione**](a-revision.md)                                              | Falso     | **Top**      |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                          | Falso     | **Top**      |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                          | Falso     | **Top**      |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)              | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | **Top**      |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                  | Falso     | **Top**      |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | **Top**      |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | **Top**      |
| [**USN-modificato**](a-usnchanged.md)                                         | Falso     | **Top**      |
| [**USN creato**](a-usncreated.md)                                         | Falso     | **Top**      |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                  | Falso     | **Top**      |
| [**USN-tra siti**](a-usnintersite.md)                                     | Falso     | **Top**      |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | **Top**      |
| [**USN-origine**](a-usnsource.md)                                           | Falso     | **Top**      |
| [**WBEM-percorso**](a-wbempath.md)                                             | Falso     | **Top**      |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | **Top**      |
| [**Quando-modificato**](a-whenchanged.md)                                       | Falso     | **Top**      |
| [**Data di creazione**](a-whencreated.md)                                       | Falso     | **Top**      |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                      | Falso     | **Top**      |
| [**WWW-pagina-altro**](a-url.md)                                             | Falso     | **Top**      |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributes (Attributi)](#windows-server-2003-r2-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valore predefinito-nascondiglio        | 1                                                                                            |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | **Top**<br/>                                                                           |
| Possibili superiori          | [**Perso e trovato**](c-lostandfound.md)                                                     |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                 |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Attributi di Windows Server 2003 R2

Questa classe contiene gli attributi seguenti per Windows Server 2003 R2:



| Attributo                                                                   | Obbligatorio | Derivato da |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Descrizione**](a-admindescription.md)                             | Falso     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | **Top**      |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | **Top**      |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)        | Falso     | **Top**      |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | **Top**      |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)   | Falso     | **Top**      |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)               | Falso     | **Top**      |
| [**Nome canonico**](a-canonicalname.md)                                   | Falso     | **Top**      |
| [**Nome comune**](a-cn.md)                                                 | Falso     | **Top**      |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | **Top**      |
| [**Descrizione**](a-description.md)                                        | Falso     | **Top**      |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | **Top**      |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                    | Falso     | **Top**      |
| [**DSA-firma**](a-dsasignature.md)                                     | Falso     | **Top**      |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                 | Falso     | **Top**      |
| [**Nome estensione**](a-extensionname.md)                                   | Falso     | **Top**      |
| [**Bandiere**](a-flags.md)                                                    | Falso     | **Top**      |
| [**Da-entry**](a-fromentry.md)                                           | Falso     | **Top**      |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | **Top**      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | **Top**      |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | **Top**      |
| [**Viene eliminato**](a-isdeleted.md)                                           | Falso     | **Top**      |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | **Top**      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | **Top**      |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | **Top**      |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | **Top**      |
| [**Mastered-by**](a-masteredby.md)                                         | Falso     | **Top**      |
| [**Modifica-timestamp**](a-modifytimestamp.md)                              | Falso     | **Top**      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | **Top**      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | **Top**      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | **Top**      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | **Top**      |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | **Top**      |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)      | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | **Top**      |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                              | Falso     | **Top**      |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | **Top**      |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                       | Falso     | **Top**      |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | **Top**      |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | **Top**      |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                         | Falso     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | **Top**      |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | **Top**      |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)              | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | **Top**      |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                  | Falso     | **Top**      |
| [**-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | **Top**      |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | **Top**      |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                    | Vero      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | **Top**      |
| [**Categoria oggetto**](a-objectcategory.md)                                 | Vero      | **Top**      |
| [**Classe Object**](a-objectclass.md)                                       | Vero      | **Top**      |
| [**GUID oggetto**](a-objectguid.md)                                         | Falso     | **Top**      |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | **Top**      |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                 | Falso     | **Top**      |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)   | Falso     | **Top**      |
| [**Set di attributi parziali**](a-partialattributeset.md)                      | Falso     | **Top**      |
| [**Possibili-inferiori**](a-possibleinferiors.md)                           | Falso     | **Top**      |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                          | Falso     | **Top**      |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | **Top**      |
| [**Query-criteri-BL**](a-querypolicybl.md)                                  | Falso     | **Top**      |
| [**RDN**](a-name.md)                                                       | Falso     | **Top**      |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                   | Falso     | **Top**      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | **Top**      |
| [**Report**](a-directreports.md)                                          | Falso     | **Top**      |
| [**Reps-da**](a-repsfrom.md)                                             | Falso     | **Top**      |
| [**Da Reps a**](a-repsto.md)                                                 | Falso     | **Top**      |
| [**Revisione**](a-revision.md)                                              | Falso     | **Top**      |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                          | Falso     | **Top**      |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                          | Falso     | **Top**      |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)              | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | **Top**      |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                  | Falso     | **Top**      |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | **Top**      |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | **Top**      |
| [**USN-modificato**](a-usnchanged.md)                                         | Falso     | **Top**      |
| [**USN creato**](a-usncreated.md)                                         | Falso     | **Top**      |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                  | Falso     | **Top**      |
| [**USN-tra siti**](a-usnintersite.md)                                     | Falso     | **Top**      |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | **Top**      |
| [**USN-origine**](a-usnsource.md)                                           | Falso     | **Top**      |
| [**WBEM-percorso**](a-wbempath.md)                                             | Falso     | **Top**      |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | **Top**      |
| [**Quando-modificato**](a-whenchanged.md)                                       | Falso     | **Top**      |
| [**Data di creazione**](a-whencreated.md)                                       | Falso     | **Top**      |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                      | Falso     | **Top**      |
| [**WWW-pagina-altro**](a-url.md)                                             | Falso     | **Top**      |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributes (Attributi)](#windows-server-2008-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valore predefinito-nascondiglio        | 1                                                                                            |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | **Top**<br/>                                                                           |
| Possibili superiori          | [**Perso e trovato**](c-lostandfound.md)                                                     |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                 |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Attributi di Windows Server 2008

Questa classe contiene gli attributi seguenti per Windows Server 2008:



| Attributo                                                                      | Obbligatorio | Derivato da |
|--------------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Descrizione**](a-admindescription.md)                                | Falso     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | **Top**      |
| [**Attributi consentiti**](a-allowedattributes.md)                              | Falso     | **Top**      |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)           | Falso     | **Top**      |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                         | Falso     | **Top**      |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)      | Falso     | **Top**      |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | **Top**      |
| [**Nome canonico**](a-canonicalname.md)                                      | Falso     | **Top**      |
| [**Nome comune**](a-cn.md)                                                    | Falso     | **Top**      |
| [**Creazione timestamp**](a-createtimestamp.md)                                 | Falso     | **Top**      |
| [**Descrizione**](a-description.md)                                           | Falso     | **Top**      |
| [**Nome visualizzato**](a-displayname.md)                                          | Falso     | **Top**      |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                       | Falso     | **Top**      |
| [**DSA-firma**](a-dsasignature.md)                                        | Falso     | **Top**      |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                    | Falso     | **Top**      |
| [**Nome estensione**](a-extensionname.md)                                      | Falso     | **Top**      |
| [**Bandiere**](a-flags.md)                                                       | Falso     | **Top**      |
| [**Da-entry**](a-fromentry.md)                                              | Falso     | **Top**      |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | **Top**      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falso     | **Top**      |
| [**Tipo di istanza**](a-instancetype.md)                                        | Vero      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | **Top**      |
| [**Viene eliminato**](a-isdeleted.md)                                              | Falso     | **Top**      |
| [**Is-member-of-DL**](a-memberof.md)                                          | Falso     | **Top**      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | Falso     | **Top**      |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                 | Falso     | **Top**      |
| [**Oggetti gestiti**](a-managedobjects.md)                                    | Falso     | **Top**      |
| [**Mastered-by**](a-masteredby.md)                                            | Falso     | **Top**      |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                 | Falso     | **Top**      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | **Top**      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                    | Falso     | **Top**      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | **Top**      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | **Top**      |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)    | Falso     | **Top**      |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md) | Falso     | **Top**      |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)         | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | **Top**      |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                              | Falso     | **Top**      |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                   | Falso     | **Top**      |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)             | Falso     | **Top**      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | **Top**      |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                 | Falso     | **Top**      |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Falso     | **Top**      |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                          | Falso     | **Top**      |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)       | Falso     | **Top**      |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | **Top**      |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | **Top**      |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falso     | **Top**      |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                            | Falso     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | **Top**      |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                           | Falso     | **Top**      |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                 | Falso     | **Top**      |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)         | Falso     | **Top**      |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                 | Falso     | **Top**      |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                             | Falso     | **Top**      |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                        | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | **Top**      |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                     | Falso     | **Top**      |
| [**-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | **Top**      |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                        | Falso     | **Top**      |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                       | Vero      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falso     | **Top**      |
| [**Categoria oggetto**](a-objectcategory.md)                                    | Vero      | **Top**      |
| [**Classe Object**](a-objectclass.md)                                          | Vero      | **Top**      |
| [**GUID oggetto**](a-objectguid.md)                                            | Falso     | **Top**      |
| [**Versione oggetto**](a-objectversion.md)                                      | Falso     | **Top**      |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                    | Falso     | **Top**      |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)      | Falso     | **Top**      |
| [**Set di attributi parziali**](a-partialattributeset.md)                         | Falso     | **Top**      |
| [**Possibili-inferiori**](a-possibleinferiors.md)                              | Falso     | **Top**      |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                             | Falso     | **Top**      |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                    | Falso     | **Top**      |
| [**Query-criteri-BL**](a-querypolicybl.md)                                     | Falso     | **Top**      |
| [**RDN**](a-name.md)                                                          | Falso     | **Top**      |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                      | Falso     | **Top**      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | **Top**      |
| [**Report**](a-directreports.md)                                             | Falso     | **Top**      |
| [**Reps-da**](a-repsfrom.md)                                                | Falso     | **Top**      |
| [**Da Reps a**](a-repsto.md)                                                    | Falso     | **Top**      |
| [**Revisione**](a-revision.md)                                                 | Falso     | **Top**      |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                             | Falso     | **Top**      |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                             | Falso     | **Top**      |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                 | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | **Top**      |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                     | Falso     | **Top**      |
| [**Riferimenti secondari**](a-subrefs.md)                                                  | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | **Top**      |
| [**Flag di sistema**](a-systemflags.md)                                          | Falso     | **Top**      |
| [**USN-modificato**](a-usnchanged.md)                                            | Falso     | **Top**      |
| [**USN creato**](a-usncreated.md)                                            | Falso     | **Top**      |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                     | Falso     | **Top**      |
| [**USN-tra siti**](a-usnintersite.md)                                        | Falso     | **Top**      |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                    | Falso     | **Top**      |
| [**USN-origine**](a-usnsource.md)                                              | Falso     | **Top**      |
| [**WBEM-percorso**](a-wbempath.md)                                                | Falso     | **Top**      |
| [**Oggetti noti**](a-wellknownobjects.md)                               | Falso     | **Top**      |
| [**Quando-modificato**](a-whenchanged.md)                                          | Falso     | **Top**      |
| [**Data di creazione**](a-whencreated.md)                                          | Falso     | **Top**      |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                         | Falso     | **Top**      |
| [**WWW-pagina-altro**](a-url.md)                                                | Falso     | **Top**      |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributes (Attributi)](#windows-server-2008-r2-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valore predefinito-nascondiglio        | 1                                                                                            |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | **Top**<br/>                                                                           |
| Possibili superiori          | [**Perso e trovato**](c-lostandfound.md)                                                     |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                 |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Attributi di Windows Server 2008 R2

Questa classe contiene gli attributi seguenti per Windows Server 2008 R2:



| Attributo                                                                        | Obbligatorio | Derivato da |
|----------------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Descrizione**](a-admindescription.md)                                  | Falso     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | **Top**      |
| [**Attributi consentiti**](a-allowedattributes.md)                                | Falso     | **Top**      |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)             | Falso     | **Top**      |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                           | Falso     | **Top**      |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)        | Falso     | **Top**      |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | **Top**      |
| [**Nome canonico**](a-canonicalname.md)                                        | Falso     | **Top**      |
| [**Nome comune**](a-cn.md)                                                      | Falso     | **Top**      |
| [**Creazione timestamp**](a-createtimestamp.md)                                   | Falso     | **Top**      |
| [**Descrizione**](a-description.md)                                             | Falso     | **Top**      |
| [**Nome visualizzato**](a-displayname.md)                                            | Falso     | **Top**      |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                         | Falso     | **Top**      |
| [**DSA-firma**](a-dsasignature.md)                                          | Falso     | **Top**      |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                      | Falso     | **Top**      |
| [**Nome estensione**](a-extensionname.md)                                        | Falso     | **Top**      |
| [**Bandiere**](a-flags.md)                                                         | Falso     | **Top**      |
| [**Da-entry**](a-fromentry.md)                                                | Falso     | **Top**      |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | **Top**      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | **Top**      |
| [**Tipo di istanza**](a-instancetype.md)                                          | Vero      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | **Top**      |
| [**Viene eliminato**](a-isdeleted.md)                                                | Falso     | **Top**      |
| [**Is-member-of-DL**](a-memberof.md)                                            | Falso     | **Top**      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | **Top**      |
| [**Riciclato**](a-isrecycled.md)                                              | Falso     | **Top**      |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                   | Falso     | **Top**      |
| [**Oggetti gestiti**](a-managedobjects.md)                                      | Falso     | **Top**      |
| [**Mastered-by**](a-masteredby.md)                                              | Falso     | **Top**      |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                   | Falso     | **Top**      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | **Top**      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | **Top**      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | **Top**      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | **Top**      |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | **Top**      |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md)   | Falso     | **Top**      |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)           | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | **Top**      |
| [**ms-DS-Enabled-feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | **Top**      |
| [**ms-DS-host-Service-account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | **Top**      |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                | Falso     | **Top**      |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | **Top**      |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | **Top**      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | **Top**      |
| [**ms-DS-ultimo-noto-RDN**](a-msds-lastknownrdn.md)                              | Falso     | **Top**      |
| [**ms-DS-locale-effettivo-eliminazione-ora**](a-msds-localeffectivedeletiontime.md) | Falso     | **Top**      |
| [**ms-DS-local-effective-riciclo-tempo**](a-msds-localeffectiverecycletime.md)   | Falso     | **Top**      |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                   | Falso     | **Top**      |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | **Top**      |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                            | Falso     | **Top**      |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | **Top**      |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | **Top**      |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | **Top**      |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | **Top**      |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                              | Falso     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | **Top**      |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | **Top**      |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                             | Falso     | **Top**      |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                   | Falso     | **Top**      |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)           | Falso     | **Top**      |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                   | Falso     | **Top**      |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                               | Falso     | **Top**      |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                          | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | **Top**      |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                       | Falso     | **Top**      |
| [**-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | **Top**      |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | **Top**      |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                         | Vero      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | **Top**      |
| [**Categoria oggetto**](a-objectcategory.md)                                      | Vero      | **Top**      |
| [**Classe Object**](a-objectclass.md)                                            | Vero      | **Top**      |
| [**GUID oggetto**](a-objectguid.md)                                              | Falso     | **Top**      |
| [**Versione oggetto**](a-objectversion.md)                                        | Falso     | **Top**      |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                      | Falso     | **Top**      |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)        | Falso     | **Top**      |
| [**Set di attributi parziali**](a-partialattributeset.md)                           | Falso     | **Top**      |
| [**Possibili-inferiori**](a-possibleinferiors.md)                                | Falso     | **Top**      |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                               | Falso     | **Top**      |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                      | Falso     | **Top**      |
| [**Query-criteri-BL**](a-querypolicybl.md)                                       | Falso     | **Top**      |
| [**RDN**](a-name.md)                                                            | Falso     | **Top**      |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                        | Falso     | **Top**      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | **Top**      |
| [**Report**](a-directreports.md)                                               | Falso     | **Top**      |
| [**Reps-da**](a-repsfrom.md)                                                  | Falso     | **Top**      |
| [**Da Reps a**](a-repsto.md)                                                      | Falso     | **Top**      |
| [**Revisione**](a-revision.md)                                                   | Falso     | **Top**      |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                               | Falso     | **Top**      |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                               | Falso     | **Top**      |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                   | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | **Top**      |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                       | Falso     | **Top**      |
| [**Riferimenti secondari**](a-subrefs.md)                                                    | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | **Top**      |
| [**Flag di sistema**](a-systemflags.md)                                            | Falso     | **Top**      |
| [**USN-modificato**](a-usnchanged.md)                                              | Falso     | **Top**      |
| [**USN creato**](a-usncreated.md)                                              | Falso     | **Top**      |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                       | Falso     | **Top**      |
| [**USN-tra siti**](a-usnintersite.md)                                          | Falso     | **Top**      |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                      | Falso     | **Top**      |
| [**USN-origine**](a-usnsource.md)                                                | Falso     | **Top**      |
| [**WBEM-percorso**](a-wbempath.md)                                                  | Falso     | **Top**      |
| [**Oggetti noti**](a-wellknownobjects.md)                                 | Falso     | **Top**      |
| [**Quando-modificato**](a-whenchanged.md)                                            | Falso     | **Top**      |
| [**Data di creazione**](a-whencreated.md)                                            | Falso     | **Top**      |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                           | Falso     | **Top**      |
| [**WWW-pagina-altro**](a-url.md)                                                  | Falso     | **Top**      |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributes (Attributi)](#windows-server-2012-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valore predefinito-nascondiglio        | 1                                                                                            |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | **Top**<br/>                                                                           |
| Possibili superiori          | [**Perso e trovato**](c-lostandfound.md)                                                     |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                 |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Attributi di Windows Server 2012

Questa classe contiene gli attributi seguenti per Windows Server 2012:



| Attributo                                                                                    | Obbligatorio | Derivato da |
|----------------------------------------------------------------------------------------------|-----------|--------------|
| [**Admin-Descrizione**](a-admindescription.md)                                              | Falso     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | **Top**      |
| [**Attributi consentiti**](a-allowedattributes.md)                                            | Falso     | **Top**      |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)                         | Falso     | **Top**      |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                                       | Falso     | **Top**      |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)                    | Falso     | **Top**      |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | **Top**      |
| [**Nome canonico**](a-canonicalname.md)                                                    | Falso     | **Top**      |
| [**Nome comune**](a-cn.md)                                                                  | Falso     | **Top**      |
| [**Creazione timestamp**](a-createtimestamp.md)                                               | Falso     | **Top**      |
| [**Descrizione**](a-description.md)                                                         | Falso     | **Top**      |
| [**Nome visualizzato**](a-displayname.md)                                                        | Falso     | **Top**      |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                                     | Falso     | **Top**      |
| [**DSA-firma**](a-dsasignature.md)                                                      | Falso     | **Top**      |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                                  | Falso     | **Top**      |
| [**Nome estensione**](a-extensionname.md)                                                    | Falso     | **Top**      |
| [**Bandiere**](a-flags.md)                                                                     | Falso     | **Top**      |
| [**Da-entry**](a-fromentry.md)                                                            | Falso     | **Top**      |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | **Top**      |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | **Top**      |
| [**Tipo di istanza**](a-instancetype.md)                                                      | Vero      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | **Top**      |
| [**Viene eliminato**](a-isdeleted.md)                                                            | Falso     | **Top**      |
| [**Is-member-of-DL**](a-memberof.md)                                                        | Falso     | **Top**      |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falso     | **Top**      |
| [**Riciclato**](a-isrecycled.md)                                                          | Falso     | **Top**      |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                               | Falso     | **Top**      |
| [**Oggetti gestiti**](a-managedobjects.md)                                                  | Falso     | **Top**      |
| [**Mastered-by**](a-masteredby.md)                                                          | Falso     | **Top**      |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                               | Falso     | **Top**      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | **Top**      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | **Top**      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | **Top**      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | **Top**      |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | **Top**      |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md)               | Falso     | **Top**      |
| [**ms-DS-Claim-shares-possible-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | **Top**      |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)                       | Falso     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | **Top**      |
| [**ms-DS-Enabled-feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | **Top**      |
| [**ms-DS-host-Service-account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | **Top**      |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                            | Falso     | **Top**      |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | **Top**      |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                           | Falso     | **Top**      |
| [**ms-DS-is-primary-computer-for**](a-msds-isprimarycomputerfor.md)                         | Falso     | **Top**      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | **Top**      |
| [**ms-DS-ultimo-noto-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | **Top**      |
| [**ms-DS-locale-effettivo-eliminazione-ora**](a-msds-localeffectivedeletiontime.md)             | Falso     | **Top**      |
| [**ms-DS-local-effective-riciclo-tempo**](a-msds-localeffectiverecycletime.md)               | Falso     | **Top**      |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                               | Falso     | **Top**      |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | **Top**      |
| [**ms-DS-members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | **Top**      |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                                        | Falso     | **Top**      |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | **Top**      |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | **Top**      |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | **Top**      |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falso     | **Top**      |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                                          | Falso     | **Top**      |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | **Top**      |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | **Top**      |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                                         | Falso     | **Top**      |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                               | Falso     | **Top**      |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)                       | Falso     | **Top**      |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                               | Falso     | **Top**      |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                                           | Falso     | **Top**      |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                                      | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | **Top**      |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | **Top**      |
| [**ms-DS-TDO-uscita-BL**](a-msds-tdoegressbl.md)                                            | Falso     | **Top**      |
| [**ms-DS-TDO-ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | **Top**      |
| [**ms-DS-valore-tipo-riferimento-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | **Top**      |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | **Top**      |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                                   | Falso     | **Top**      |
| [**-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | **Top**      |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | **Top**      |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                                     | Vero      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | **Top**      |
| [**Categoria oggetto**](a-objectcategory.md)                                                  | Vero      | **Top**      |
| [**Classe Object**](a-objectclass.md)                                                        | Vero      | **Top**      |
| [**GUID oggetto**](a-objectguid.md)                                                          | Falso     | **Top**      |
| [**Versione oggetto**](a-objectversion.md)                                                    | Falso     | **Top**      |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                                  | Falso     | **Top**      |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)                    | Falso     | **Top**      |
| [**Set di attributi parziali**](a-partialattributeset.md)                                       | Falso     | **Top**      |
| [**Possibili-inferiori**](a-possibleinferiors.md)                                            | Falso     | **Top**      |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                                           | Falso     | **Top**      |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                  | Falso     | **Top**      |
| [**Query-criteri-BL**](a-querypolicybl.md)                                                   | Falso     | **Top**      |
| [**RDN**](a-name.md)                                                                        | Falso     | **Top**      |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                                    | Falso     | **Top**      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | **Top**      |
| [**Report**](a-directreports.md)                                                           | Falso     | **Top**      |
| [**Reps-da**](a-repsfrom.md)                                                              | Falso     | **Top**      |
| [**Da Reps a**](a-repsto.md)                                                                  | Falso     | **Top**      |
| [**Revisione**](a-revision.md)                                                               | Falso     | **Top**      |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                                           | Falso     | **Top**      |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                                           | Falso     | **Top**      |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                               | Falso     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | **Top**      |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                                   | Falso     | **Top**      |
| [**Riferimenti secondari**](a-subrefs.md)                                                                | Falso     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | **Top**      |
| [**Flag di sistema**](a-systemflags.md)                                                        | Falso     | **Top**      |
| [**USN-modificato**](a-usnchanged.md)                                                          | Falso     | **Top**      |
| [**USN creato**](a-usncreated.md)                                                          | Falso     | **Top**      |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                                   | Falso     | **Top**      |
| [**USN-tra siti**](a-usnintersite.md)                                                      | Falso     | **Top**      |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                                  | Falso     | **Top**      |
| [**USN-origine**](a-usnsource.md)                                                            | Falso     | **Top**      |
| [**WBEM-percorso**](a-wbempath.md)                                                              | Falso     | **Top**      |
| [**Oggetti noti**](a-wellknownobjects.md)                                             | Falso     | **Top**      |
| [**Quando-modificato**](a-whenchanged.md)                                                        | Falso     | **Top**      |
| [**Data di creazione**](a-whencreated.md)                                                        | Falso     | **Top**      |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                                       | Falso     | **Top**      |
| [**WWW-pagina-altro**](a-url.md)                                                              | Falso     | **Top**      |



 

 





