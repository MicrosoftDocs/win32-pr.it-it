---
title: Classe NTDS-DSA
description: Rappresenta il processo Active Directory DSA sul server.
ms.assetid: f4369122-d74a-45d2-9dc0-46894a9f99cc
ms.tgt_platform: multiple
keywords:
- Schema AD della classe NTDS-DSA
- Schema di Active Directory della classe nTDSDSA
topic_type:
- apiref
api_name:
- NTDS-DSA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f64606c07aa15aaf7d75e7bbcdb1caf06ed84ac
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744463"
---
# <a name="ntds-dsa-class"></a>Classe NTDS-DSA

Rappresenta il processo Active Directory DSA sul server.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | NTDS-DSA                             |
| LDAP-Display-Name | nTDSDSA                              |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Schema-ID-GUID    | f0f8ffab-1191-11d0-a060-00aa006c33ed |



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
-   [Diritti estesi](#windows-2000-server-extended-rights)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Valore predefinito-nascondiglio        | 1                                                                                            |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | [**Impostazioni applicazione**](c-applicationsettings.md)<br/>                             |
| Possibili superiori          | [](c-server.md)[**Organizzazione** server](c-organization.md)                             |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                 |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Attributi del server Windows 2000

Questa classe contiene gli attributi seguenti per Windows 2000 Server:



| Attributo                                                                 | Obbligatorio | Derivato da                                                     |
|---------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Attributi consentiti**](a-allowedattributes.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md) | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome applicazione**](a-applicationname.md)                             | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome canonico**](a-canonicalname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome comune**](a-cn.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Creazione timestamp**](a-createtimestamp.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Descrizione**](a-description.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome visualizzato**](a-displayname.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**DMD-posizione**](a-dmdlocation.md)                                     | Falso     | **NTDS-DSA**                                                     |
| [**DSA-firma**](a-dsasignature.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome estensione**](a-extensionname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Bandiere**](a-flags.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Da-entry**](a-fromentry.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-root-path**](a-frsrootpath.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Has-Master-NCs**](a-hasmasterncs.md)                                  | Falso     | **NTDS-DSA**                                                     |
| [**Has-partial-replica-NCs**](a-haspartialreplicancs.md)                 | Falso     | **NTDS-DSA**                                                     |
| [**Tipo di istanza**](a-instancetype.md)                                   | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**ID chiamata**](a-invocationid.md)                                   | Falso     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Viene eliminato**](a-isdeleted.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Is-member-of-DL**](a-memberof.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Ultimo backup-tempo di ripristino**](a-lastbackuprestorationtime.md)       | Falso     | **NTDS-DSA**                                                     |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Gestito da**](a-managedby.md)                                         | Falso     | **NTDS-DSA**                                                     |
| [**Oggetti gestiti**](a-managedobjects.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Mastered-by**](a-masteredby.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Modifica-timestamp**](a-modifytimestamp.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Indirizzo di rete**](a-networkaddress.md)                               | Falso     | **NTDS-DSA**                                                     |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Elenco notifiche**](a-notificationlist.md)                           | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                  | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Categoria oggetto**](a-objectcategory.md)                               | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**Classe Object**](a-objectclass.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**GUID oggetto**](a-objectguid.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Versione oggetto**](a-objectversion.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Opzioni**](a-options.md)                                              | Falso     | **NTDS-DSA**                                                     |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md) | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Set di attributi parziali**](a-partialattributeset.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Possibili-inferiori**](a-possibleinferiors.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Indirizzi proxy**](a-proxyaddresses.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Query-criteri-BL**](a-querypolicybl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Query-Policy-Object**](a-querypolicyobject.md)                        | Falso     | **NTDS-DSA**                                                     |
| [**RDN**](a-name.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Report**](a-directreports.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Reps-da**](a-repsfrom.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Da Reps a**](a-repsto.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Retired-REPL-DSA-firme**](a-retiredrepldsasignatures.md)         | Falso     | **NTDS-DSA**                                                     |
| [**Revisione**](a-revision.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riferimento al server**](a-serverreference.md)                             | Falso     | **NTDS-DSA**                                                     |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riferimenti secondari**](a-subrefs.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Flag di sistema**](a-systemflags.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-modificato**](a-usnchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN creato**](a-usncreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-tra siti**](a-usnintersite.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-origine**](a-usnsource.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WBEM-percorso**](a-wbempath.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Oggetti noti**](a-wellknownobjects.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Quando-modificato**](a-whenchanged.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Data di creazione**](a-whencreated.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WWW-pagina-altro**](a-url.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |



## <a name="windows-2000-server-extended-rights"></a>Diritti estesi del server Windows 2000

Questa classe contiene i seguenti diritti estesi per Windows Server 2000:



| Nome comune                                                                    |
|--------------------------------------------------------------------------------|
| [**Abbandono-replica**](r-abandon-replication.md)                           |
| [**Operazione di Garbage Collection**](r-do-garbage-collection.md)                       |
| [**Ricalcola-gerarchia**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RID**](r-allocate-rids.md)                                       |
| [**Ricalcola-sicurezza-ereditarietà**](r-recalculate-security-inheritance.md) |
| [**DS-check-non aggiornato-fantasma**](r-ds-check-stale-phantoms.md)                   |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributes (Attributi)](#windows-server-2003-attributes)
-   [Diritti estesi](#windows-server-2003-extended-rights)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Valore predefinito-nascondiglio        | 1                                                                                            |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | [**Impostazioni applicazione**](c-applicationsettings.md)<br/>                             |
| Possibili superiori          | [](c-server.md)[**Organizzazione** server](c-organization.md)                             |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                 |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Attributi di Windows Server 2003

Questa classe contiene gli attributi seguenti per Windows Server 2003:



| Attributo                                                                   | Obbligatorio | Derivato da                                                     |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome applicazione**](a-applicationname.md)                               | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome canonico**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome comune**](a-cn.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**DMD-posizione**](a-dmdlocation.md)                                       | Falso     | **NTDS-DSA**                                                     |
| [**DSA-firma**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome estensione**](a-extensionname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Bandiere**](a-flags.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Da-entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-root-path**](a-frsrootpath.md)                                      | Falso     | **NTDS-DSA**                                                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Has-Master-NCs**](a-hasmasterncs.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**Has-partial-replica-NCs**](a-haspartialreplicancs.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**ID chiamata**](a-invocationid.md)                                     | Falso     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Viene eliminato**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Ultimo backup-tempo di ripristino**](a-lastbackuprestorationtime.md)         | Falso     | **NTDS-DSA**                                                     |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Gestito da**](a-managedby.md)                                           | Falso     | **NTDS-DSA**                                                     |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Mastered-by**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Modifica-timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-has-Domain-NCs**](a-msds-hasdomainncs.md)                         | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-ha-creata un'istanza-NCs**](a-msds-hasinstantiatedncs.md)             | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-has-Master-NCs**](a-msds-hasmasterncs.md)                         | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Retired-REPL-NC-firme**](a-msds-retiredreplncsignatures.md)  | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-impostazioni**](a-msds-settings.md)                                   | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Indirizzo di rete**](a-networkaddress.md)                                 | Falso     | **NTDS-DSA**                                                     |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Elenco notifiche**](a-notificationlist.md)                             | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Categoria oggetto**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**Classe Object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**GUID oggetto**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Opzioni**](a-options.md)                                                | Falso     | **NTDS-DSA**                                                     |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Set di attributi parziali**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Possibili-inferiori**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Query-criteri-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Query-Policy-Object**](a-querypolicyobject.md)                          | Falso     | **NTDS-DSA**                                                     |
| [**RDN**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Report**](a-directreports.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Reps-da**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Da Reps a**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Retired-REPL-DSA-firme**](a-retiredrepldsasignatures.md)           | Falso     | **NTDS-DSA**                                                     |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riferimento al server**](a-serverreference.md)                               | Falso     | **NTDS-DSA**                                                     |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-modificato**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN creato**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-tra siti**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-origine**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WBEM-percorso**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Quando-modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Data di creazione**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WWW-pagina-altro**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                  |



## <a name="windows-server-2003-extended-rights"></a>Diritti estesi di Windows Server 2003

Questa classe contiene i seguenti diritti estesi per Windows Server 2003:



| Nome comune                                                                    |
|--------------------------------------------------------------------------------|
| [**Operazione di Garbage Collection**](r-do-garbage-collection.md)                       |
| [**Ricalcola-gerarchia**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RID**](r-allocate-rids.md)                                       |
| [**Ricalcola-sicurezza-ereditarietà**](r-recalculate-security-inheritance.md) |
| [**DS-check-non aggiornato-fantasma**](r-ds-check-stale-phantoms.md)                   |
| [**Aggiornamento-gruppo-cache**](r-refresh-group-cache.md)                           |



## <a name="adam"></a>ADAM

-   [Attributes (Attributi)](#adam-attributes)
-   [Diritti estesi](#adam-extended-rights)



| Voce | Valore |
|-----------------------------|------------------------------------------------------------------|
| System-Only                 | Vero                                                             |
| Object-Category             | 1                                                                |
| Default-Object-Category     | \-                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                       |
| Valore predefinito-nascondiglio        | 1                                                                |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                           |
| Sottoclasse di                 | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| Possibili superiori          | [](c-server.md)[**Organizzazione** server](c-organization.md) |
| Classi ausiliarie           | \-                                                               |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                     |
| Descrittore di sicurezza predefinito | D:S                                                             |
| System-Flags                | 0x00000010                                                       |



## <a name="adam-attributes"></a>Attributi ADAM

Questa classe contiene gli attributi seguenti per ADAM:



| Attributo                                                                   | Obbligatorio | Derivato da                                                     |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome canonico**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome comune**](a-cn.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**DMD-posizione**](a-dmdlocation.md)                                       | Falso     | **NTDS-DSA**                                                     |
| [**DSA-firma**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Da-entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Has-Master-NCs**](a-hasmasterncs.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**Has-partial-replica-NCs**](a-haspartialreplicancs.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**ID chiamata**](a-invocationid.md)                                     | Falso     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Viene eliminato**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Ultimo backup-tempo di ripristino**](a-lastbackuprestorationtime.md)         | Falso     | **NTDS-DSA**                                                     |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Gestito da**](a-managedby.md)                                           | Falso     | **NTDS-DSA**                                                     |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Mastered-by**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Modifica-timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-has-Domain-NCs**](a-msds-hasdomainncs.md)                         | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-ha-creata un'istanza-NCs**](a-msds-hasinstantiatedncs.md)             | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-has-Master-NCs**](a-msds-hasmasterncs.md)                         | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Port-LDAP**](a-msds-portldap.md)                                  | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-porta-SSL**](a-msds-portssl.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Retired-REPL-NC-firme**](a-msds-retiredreplncsignatures.md)  | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-service-account**](a-msds-serviceaccount.md)                      | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-service-account-BL**](a-msds-serviceaccountbl.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-service-account-DNS-dominio**](a-msds-serviceaccountdnsdomain.md)  | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-impostazioni**](a-msds-settings.md)                                   | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**Indirizzo di rete**](a-networkaddress.md)                                 | Falso     | **NTDS-DSA**                                                     |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Categoria oggetto**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**Classe Object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**GUID oggetto**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Opzioni**](a-options.md)                                                | Falso     | **NTDS-DSA**                                                     |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Set di attributi parziali**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Possibili-inferiori**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Query-criteri-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Query-Policy-Object**](a-querypolicyobject.md)                          | Falso     | **NTDS-DSA**                                                     |
| [**RDN**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Reps-da**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Da Reps a**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Retired-REPL-DSA-firme**](a-retiredrepldsasignatures.md)           | Falso     | **NTDS-DSA**                                                     |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riferimento al server**](a-serverreference.md)                               | Falso     | **NTDS-DSA**                                                     |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-modificato**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN creato**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-tra siti**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-origine**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WBEM-percorso**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Quando-modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Data di creazione**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WWW-pagina-altro**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                  |



## <a name="adam-extended-rights"></a>Diritti estesi di ADAM

Questa classe contiene i seguenti diritti estesi per ADAM:



| Nome comune                                                                    |
|--------------------------------------------------------------------------------|
| [**Operazione di Garbage Collection**](r-do-garbage-collection.md)                       |
| [**Ricalcola-sicurezza-ereditarietà**](r-recalculate-security-inheritance.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributes (Attributi)](#windows-server-2003-r2-attributes)
-   [Diritti estesi](#windows-server-2003-r2-extended-rights)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Valore predefinito-nascondiglio        | 1                                                                                            |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | [**Impostazioni applicazione**](c-applicationsettings.md)<br/>                             |
| Possibili superiori          | [](c-server.md)[**Organizzazione** server](c-organization.md)                             |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                 |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Attributi di Windows Server 2003 R2

Questa classe contiene gli attributi seguenti per Windows Server 2003 R2:



| Attributo                                                                   | Obbligatorio | Derivato da                                                     |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome applicazione**](a-applicationname.md)                               | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome canonico**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome comune**](a-cn.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**DMD-posizione**](a-dmdlocation.md)                                       | Falso     | **NTDS-DSA**                                                     |
| [**DSA-firma**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome estensione**](a-extensionname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Bandiere**](a-flags.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Da-entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-root-path**](a-frsrootpath.md)                                      | Falso     | **NTDS-DSA**                                                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Has-Master-NCs**](a-hasmasterncs.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**Has-partial-replica-NCs**](a-haspartialreplicancs.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**ID chiamata**](a-invocationid.md)                                     | Falso     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Viene eliminato**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Ultimo backup-tempo di ripristino**](a-lastbackuprestorationtime.md)         | Falso     | **NTDS-DSA**                                                     |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Gestito da**](a-managedby.md)                                           | Falso     | **NTDS-DSA**                                                     |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Mastered-by**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Modifica-timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-has-Domain-NCs**](a-msds-hasdomainncs.md)                         | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-ha-creata un'istanza-NCs**](a-msds-hasinstantiatedncs.md)             | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-has-Master-NCs**](a-msds-hasmasterncs.md)                         | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Retired-REPL-NC-firme**](a-msds-retiredreplncsignatures.md)  | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-impostazioni**](a-msds-settings.md)                                   | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Indirizzo di rete**](a-networkaddress.md)                                 | Falso     | **NTDS-DSA**                                                     |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Elenco notifiche**](a-notificationlist.md)                             | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Categoria oggetto**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**Classe Object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**GUID oggetto**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Opzioni**](a-options.md)                                                | Falso     | **NTDS-DSA**                                                     |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Set di attributi parziali**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Possibili-inferiori**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Query-criteri-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Query-Policy-Object**](a-querypolicyobject.md)                          | Falso     | **NTDS-DSA**                                                     |
| [**RDN**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Report**](a-directreports.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Reps-da**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Da Reps a**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Retired-REPL-DSA-firme**](a-retiredrepldsasignatures.md)           | Falso     | **NTDS-DSA**                                                     |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riferimento al server**](a-serverreference.md)                               | Falso     | **NTDS-DSA**                                                     |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-modificato**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN creato**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-tra siti**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-origine**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WBEM-percorso**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Quando-modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Data di creazione**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WWW-pagina-altro**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                  |



## <a name="windows-server-2003-r2-extended-rights"></a>Diritti estesi di Windows Server 2003 R2

Questa classe contiene i seguenti diritti estesi per Windows Server 2003 R2:



| Nome comune                                                                    |
|--------------------------------------------------------------------------------|
| [**Operazione di Garbage Collection**](r-do-garbage-collection.md)                       |
| [**Ricalcola-gerarchia**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RID**](r-allocate-rids.md)                                       |
| [**Ricalcola-sicurezza-ereditarietà**](r-recalculate-security-inheritance.md) |
| [**DS-check-non aggiornato-fantasma**](r-ds-check-stale-phantoms.md)                   |
| [**Aggiornamento-gruppo-cache**](r-refresh-group-cache.md)                           |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributes (Attributi)](#windows-server-2008-attributes)
-   [Diritti estesi](#windows-server-2008-extended-rights)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Valore predefinito-nascondiglio        | 1                                                                                            |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | [**Impostazioni applicazione**](c-applicationsettings.md)<br/>                             |
| Possibili superiori          | [](c-server.md)[**Organizzazione** server](c-organization.md)                             |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                 |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Attributi di Windows Server 2008

Questa classe contiene gli attributi seguenti per Windows Server 2008:



| Attributo                                                                      | Obbligatorio | Derivato da                                                     |
|--------------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Attributi consentiti**](a-allowedattributes.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome applicazione**](a-applicationname.md)                                  | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome canonico**](a-canonicalname.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome comune**](a-cn.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Creazione timestamp**](a-createtimestamp.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Descrizione**](a-description.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome visualizzato**](a-displayname.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**DMD-posizione**](a-dmdlocation.md)                                          | Falso     | **NTDS-DSA**                                                     |
| [**DSA-firma**](a-dsasignature.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome estensione**](a-extensionname.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Bandiere**](a-flags.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Da-entry**](a-fromentry.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-root-path**](a-frsrootpath.md)                                         | Falso     | **NTDS-DSA**                                                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Has-Master-NCs**](a-hasmasterncs.md)                                       | Falso     | **NTDS-DSA**                                                     |
| [**Has-partial-replica-NCs**](a-haspartialreplicancs.md)                      | Falso     | **NTDS-DSA**                                                     |
| [**Tipo di istanza**](a-instancetype.md)                                        | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**ID chiamata**](a-invocationid.md)                                        | Falso     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Viene eliminato**](a-isdeleted.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Is-member-of-DL**](a-memberof.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Ultimo backup-tempo di ripristino**](a-lastbackuprestorationtime.md)            | Falso     | **NTDS-DSA**                                                     |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Gestito da**](a-managedby.md)                                              | Falso     | **NTDS-DSA**                                                     |
| [**Oggetti gestiti**](a-managedobjects.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Mastered-by**](a-masteredby.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                      | Falso     | **NTDS-DSA**                                                     |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-has-Domain-NCs**](a-msds-hasdomainncs.md)                            | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-has-full-replica-NCs**](a-msds-hasfullreplicancs.md)                 | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-ha-creata un'istanza-NCs**](a-msds-hasinstantiatedncs.md)                | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-has-Master-NCs**](a-msds-hasmasterncs.md)                            | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-isGC**](a-msds-isgc.md)                                              | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-isRODC**](a-msds-isrodc.md)                                          | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-is-User-Caching-at-RODC**](a-msds-isusercachableatrodc.md)          | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-mai-rivelare-gruppo**](a-msds-neverrevealgroup.md)                    | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                      | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Retired-REPL-NC-firme**](a-msds-retiredreplncsignatures.md)     | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Revealed-utenti**](a-msds-revealedusers.md)                           | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Reveal-OnDemand-gruppo**](a-msds-revealondemandgroup.md)              | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-impostazioni**](a-msds-settings.md)                                      | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**ms-DS-SiteName**](a-msds-sitename.md)                                      | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Indirizzo di rete**](a-networkaddress.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Elenco notifiche**](a-notificationlist.md)                                | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                       | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Categoria oggetto**](a-objectcategory.md)                                    | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**Classe Object**](a-objectclass.md)                                          | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**GUID oggetto**](a-objectguid.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Versione oggetto**](a-objectversion.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Opzioni**](a-options.md)                                                   | Falso     | **NTDS-DSA**                                                     |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Set di attributi parziali**](a-partialattributeset.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Possibili-inferiori**](a-possibleinferiors.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Query-criteri-BL**](a-querypolicybl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Query-Policy-Object**](a-querypolicyobject.md)                             | Falso     | **NTDS-DSA**                                                     |
| [**RDN**](a-name.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Report**](a-directreports.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Reps-da**](a-repsfrom.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Da Reps a**](a-repsto.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Retired-REPL-DSA-firme**](a-retiredrepldsasignatures.md)              | Falso     | **NTDS-DSA**                                                     |
| [**Revisione**](a-revision.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riferimento al server**](a-serverreference.md)                                  | Falso     | **NTDS-DSA**                                                     |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riferimenti secondari**](a-subrefs.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Flag di sistema**](a-systemflags.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-modificato**](a-usnchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN creato**](a-usncreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-tra siti**](a-usnintersite.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-origine**](a-usnsource.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WBEM-percorso**](a-wbempath.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Oggetti noti**](a-wellknownobjects.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Quando-modificato**](a-whenchanged.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Data di creazione**](a-whencreated.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WWW-pagina-altro**](a-url.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                  |



## <a name="windows-server-2008-extended-rights"></a>Diritti estesi di Windows Server 2008

Questa classe contiene i seguenti diritti estesi per Windows Server 2008:



| Nome comune                                                                    |
|--------------------------------------------------------------------------------|
| [**Operazione di Garbage Collection**](r-do-garbage-collection.md)                       |
| [**Ricalcola-gerarchia**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RID**](r-allocate-rids.md)                                       |
| [**Ricalcola-sicurezza-ereditarietà**](r-recalculate-security-inheritance.md) |
| [**DS-check-non aggiornato-fantasma**](r-ds-check-stale-phantoms.md)                   |
| [**Aggiornamento-gruppo-cache**](r-refresh-group-cache.md)                           |
| [**Ricarica-SSL-certificate**](r-reload-ssl-certificate.md)                     |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributes (Attributi)](#windows-server-2008-r2-attributes)
-   [Diritti estesi](#windows-server-2008-r2-extended-rights)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Valore predefinito-nascondiglio        | 1                                                                                            |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | [**Impostazioni applicazione**](c-applicationsettings.md)<br/>                             |
| Possibili superiori          | [](c-server.md)[**Organizzazione** server](c-organization.md)                             |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                 |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Attributi di Windows Server 2008 R2

Questa classe contiene gli attributi seguenti per Windows Server 2008 R2:



| Attributo                                                                        | Obbligatorio | Derivato da                                                     |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Attributi consentiti**](a-allowedattributes.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome applicazione**](a-applicationname.md)                                    | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome canonico**](a-canonicalname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome comune**](a-cn.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Creazione timestamp**](a-createtimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Descrizione**](a-description.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome visualizzato**](a-displayname.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**DMD-posizione**](a-dmdlocation.md)                                            | Falso     | **NTDS-DSA**                                                     |
| [**DSA-firma**](a-dsasignature.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome estensione**](a-extensionname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Bandiere**](a-flags.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Da-entry**](a-fromentry.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-root-path**](a-frsrootpath.md)                                           | Falso     | **NTDS-DSA**                                                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Has-Master-NCs**](a-hasmasterncs.md)                                         | Falso     | **NTDS-DSA**                                                     |
| [**Has-partial-replica-NCs**](a-haspartialreplicancs.md)                        | Falso     | **NTDS-DSA**                                                     |
| [**Tipo di istanza**](a-instancetype.md)                                          | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**ID chiamata**](a-invocationid.md)                                          | Falso     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Viene eliminato**](a-isdeleted.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Is-member-of-DL**](a-memberof.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riciclato**](a-isrecycled.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Ultimo backup-tempo di ripristino**](a-lastbackuprestorationtime.md)              | Falso     | **NTDS-DSA**                                                     |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Gestito da**](a-managedby.md)                                                | Falso     | **NTDS-DSA**                                                     |
| [**Oggetti gestiti**](a-managedobjects.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Mastered-by**](a-masteredby.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                        | Falso     | **NTDS-DSA**                                                     |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Funzionalità abilitata per MS-DS**](a-msds-enabledfeature.md)                           | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Enabled-feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-has-Domain-NCs**](a-msds-hasdomainncs.md)                              | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-has-full-replica-NCs**](a-msds-hasfullreplicancs.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-ha-creata un'istanza-NCs**](a-msds-hasinstantiatedncs.md)                  | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-has-Master-NCs**](a-msds-hasmasterncs.md)                              | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-host-Service-account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-isGC**](a-msds-isgc.md)                                                | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-isRODC**](a-msds-isrodc.md)                                            | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-is-User-Caching-at-RODC**](a-msds-isusercachableatrodc.md)            | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-ultimo-noto-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-locale-effettivo-eliminazione-ora**](a-msds-localeffectivedeletiontime.md) | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-local-effective-riciclo-tempo**](a-msds-localeffectiverecycletime.md)   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-mai-rivelare-gruppo**](a-msds-neverrevealgroup.md)                      | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                        | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Retired-REPL-NC-firme**](a-msds-retiredreplncsignatures.md)       | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Revealed-utenti**](a-msds-revealedusers.md)                             | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Reveal-OnDemand-gruppo**](a-msds-revealondemandgroup.md)                | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-impostazioni**](a-msds-settings.md)                                        | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**ms-DS-SiteName**](a-msds-sitename.md)                                        | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Indirizzo di rete**](a-networkaddress.md)                                      | Falso     | **NTDS-DSA**                                                     |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Elenco notifiche**](a-notificationlist.md)                                  | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                         | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Categoria oggetto**](a-objectcategory.md)                                      | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**Classe Object**](a-objectclass.md)                                            | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**GUID oggetto**](a-objectguid.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Versione oggetto**](a-objectversion.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Opzioni**](a-options.md)                                                     | Falso     | **NTDS-DSA**                                                     |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Set di attributi parziali**](a-partialattributeset.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Possibili-inferiori**](a-possibleinferiors.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Query-criteri-BL**](a-querypolicybl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Query-Policy-Object**](a-querypolicyobject.md)                               | Falso     | **NTDS-DSA**                                                     |
| [**RDN**](a-name.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Report**](a-directreports.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Reps-da**](a-repsfrom.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Da Reps a**](a-repsto.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Retired-REPL-DSA-firme**](a-retiredrepldsasignatures.md)                | Falso     | **NTDS-DSA**                                                     |
| [**Revisione**](a-revision.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riferimento al server**](a-serverreference.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riferimenti secondari**](a-subrefs.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Flag di sistema**](a-systemflags.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-modificato**](a-usnchanged.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN creato**](a-usncreated.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-tra siti**](a-usnintersite.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-origine**](a-usnsource.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WBEM-percorso**](a-wbempath.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Oggetti noti**](a-wellknownobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Quando-modificato**](a-whenchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Data di creazione**](a-whencreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WWW-pagina-altro**](a-url.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |



## <a name="windows-server-2008-r2-extended-rights"></a>Diritti estesi di Windows Server 2008 R2

Questa classe contiene i seguenti diritti estesi per Windows Server 2008 R2:



| Nome comune                                                                    |
|--------------------------------------------------------------------------------|
| [**Operazione di Garbage Collection**](r-do-garbage-collection.md)                       |
| [**Ricalcola-gerarchia**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RID**](r-allocate-rids.md)                                       |
| [**Ricalcola-sicurezza-ereditarietà**](r-recalculate-security-inheritance.md) |
| [**DS-check-non aggiornato-fantasma**](r-ds-check-stale-phantoms.md)                   |
| [**Aggiornamento-gruppo-cache**](r-refresh-group-cache.md)                           |
| [**Ricarica-SSL-certificate**](r-reload-ssl-certificate.md)                     |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributes (Attributi)](#windows-server-2012-attributes)
-   [Diritti estesi](#windows-server-2012-extended-rights)
-   [Scritture convalidate](#windows-server-2012-validated-writes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vero                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Valore predefinito-nascondiglio        | 1                                                                                            |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                       |
| Sottoclasse di                 | [**Impostazioni applicazione**](c-applicationsettings.md)<br/>                             |
| Possibili superiori          | [](c-server.md)[**Organizzazione** server](c-organization.md)                             |
| Classi ausiliarie           | \-                                                                                           |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                 |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Attributi di Windows Server 2012

Questa classe contiene gli attributi seguenti per Windows Server 2012:



| Attributo                                                                                    | Obbligatorio | Derivato da                                                     |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Attributi consentiti**](a-allowedattributes.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome applicazione**](a-applicationname.md)                                                | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome canonico**](a-canonicalname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome comune**](a-cn.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Creazione timestamp**](a-createtimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Descrizione**](a-description.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome visualizzato**](a-displayname.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**DMD-posizione**](a-dmdlocation.md)                                                        | Falso     | **NTDS-DSA**                                                     |
| [**DSA-firma**](a-dsasignature.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome estensione**](a-extensionname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Bandiere**](a-flags.md)                                                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Da-entry**](a-fromentry.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**FRS-root-path**](a-frsrootpath.md)                                                       | Falso     | **NTDS-DSA**                                                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Has-Master-NCs**](a-hasmasterncs.md)                                                     | Falso     | **NTDS-DSA**                                                     |
| [**Has-partial-replica-NCs**](a-haspartialreplicancs.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**Tipo di istanza**](a-instancetype.md)                                                      | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**ID chiamata**](a-invocationid.md)                                                      | Falso     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Viene eliminato**](a-isdeleted.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Is-member-of-DL**](a-memberof.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riciclato**](a-isrecycled.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Ultimo backup-tempo di ripristino**](a-lastbackuprestorationtime.md)                          | Falso     | **NTDS-DSA**                                                     |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Gestito da**](a-managedby.md)                                                            | Falso     | **NTDS-DSA**                                                     |
| [**Oggetti gestiti**](a-managedobjects.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Mastered-by**](a-masteredby.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Claim-shares-possible-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Funzionalità abilitata per MS-DS**](a-msds-enabledfeature.md)                                       | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Enabled-feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-has-Domain-NCs**](a-msds-hasdomainncs.md)                                          | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-has-full-replica-NCs**](a-msds-hasfullreplicancs.md)                               | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-ha-creata un'istanza-NCs**](a-msds-hasinstantiatedncs.md)                              | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-has-Master-NCs**](a-msds-hasmasterncs.md)                                          | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-host-Service-account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-isGC**](a-msds-isgc.md)                                                            | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-is-primary-computer-for**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-isRODC**](a-msds-isrodc.md)                                                        | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-is-User-Caching-at-RODC**](a-msds-isusercachableatrodc.md)                        | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-ultimo-noto-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-locale-effettivo-eliminazione-ora**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-local-effective-riciclo-tempo**](a-msds-localeffectiverecycletime.md)               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-mai-rivelare-gruppo**](a-msds-neverrevealgroup.md)                                  | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                                    | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Retired-REPL-NC-firme**](a-msds-retiredreplncsignatures.md)                   | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Revealed-utenti**](a-msds-revealedusers.md)                                         | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Reveal-OnDemand-gruppo**](a-msds-revealondemandgroup.md)                            | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-impostazioni**](a-msds-settings.md)                                                    | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**ms-DS-SiteName**](a-msds-sitename.md)                                                    | Falso     | **NTDS-DSA**                                                     |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-TDO-uscita-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-TDO-ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-DS-valore-tipo-riferimento-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Indirizzo di rete**](a-networkaddress.md)                                                  | Falso     | **NTDS-DSA**                                                     |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Elenco notifiche**](a-notificationlist.md)                                              | Falso     | [**Impostazioni applicazione**](c-applicationsettings.md)<br/> |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Categoria oggetto**](a-objectcategory.md)                                                  | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**Classe Object**](a-objectclass.md)                                                        | Vero      | [**In alto**](c-top.md)<br/>                                  |
| [**GUID oggetto**](a-objectguid.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Versione oggetto**](a-objectversion.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Opzioni**](a-options.md)                                                                 | Falso     | **NTDS-DSA**                                                     |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Set di attributi parziali**](a-partialattributeset.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Possibili-inferiori**](a-possibleinferiors.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Query-criteri-BL**](a-querypolicybl.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Query-Policy-Object**](a-querypolicyobject.md)                                           | Falso     | **NTDS-DSA**                                                     |
| [**RDN**](a-name.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Report**](a-directreports.md)                                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Reps-da**](a-repsfrom.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Da Reps a**](a-repsto.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Retired-REPL-DSA-firme**](a-retiredrepldsasignatures.md)                            | Falso     | **NTDS-DSA**                                                     |
| [**Revisione**](a-revision.md)                                                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riferimento al server**](a-serverreference.md)                                                | Falso     | **NTDS-DSA**                                                     |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Riferimenti secondari**](a-subrefs.md)                                                                | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Flag di sistema**](a-systemflags.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-modificato**](a-usnchanged.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN creato**](a-usncreated.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-tra siti**](a-usnintersite.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**USN-origine**](a-usnsource.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WBEM-percorso**](a-wbempath.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Oggetti noti**](a-wellknownobjects.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Quando-modificato**](a-whenchanged.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**Data di creazione**](a-whencreated.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                  |
| [**WWW-pagina-altro**](a-url.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                  |



## <a name="windows-server-2012-extended-rights"></a>Diritti estesi di Windows Server 2012

Questa classe contiene i seguenti diritti estesi per Windows Server 2012:



| Nome comune                                                                    |
|--------------------------------------------------------------------------------|
| [**Operazione di Garbage Collection**](r-do-garbage-collection.md)                       |
| [**Ricalcola-gerarchia**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RID**](r-allocate-rids.md)                                       |
| [**Ricalcola-sicurezza-ereditarietà**](r-recalculate-security-inheritance.md) |
| [**DS-check-non aggiornato-fantasma**](r-ds-check-stale-phantoms.md)                   |
| [**Aggiornamento-gruppo-cache**](r-refresh-group-cache.md)                           |
| [**Ricarica-SSL-certificate**](r-reload-ssl-certificate.md)                     |



## <a name="windows-server-2012-validated-writes"></a>Scritture convalidate per Windows Server 2012

Questa classe contiene le seguenti scritture convalidate per Windows Server 2012:



| Nome comune                                                                    |
|--------------------------------------------------------------------------------|
| [**Convalidato-MS-DS-Behavior-Version**](r-validated-ms-ds-behavior-version.md) |



 

 





