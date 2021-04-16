---
title: Classe Print-Queue
description: Contiene informazioni su una coda di stampa.
ms.assetid: 779eb37c-f94e-472a-9551-8a0f72fe0e2b
ms.tgt_platform: multiple
keywords:
- Schema di AD Print-Queue Class
- Schema di Active Directory della classe printQueue
topic_type:
- apiref
api_name:
- Print-Queue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7995598603af4cab7b4b9d6f150e92964f0ee616
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479512"
---
# <a name="print-queue-class"></a>Classe Print-Queue

Contiene informazioni su una coda di stampa.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Print-Queue                          |
| LDAP-Display-Name | printQueue                           |
| Privilegio aggiornamento  | Chiunque può aggiornare questo oggetto.       |
| Frequenza di aggiornamento  | \-                                   |
| Schema-ID-GUID    | bf967aa8-0de6-11d0-a285-00aa003049e2 |



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
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                    |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                               |
| Sottoclasse di                 | [**Punto di connessione**](c-connectionpoint.md)<br/>                                                                                                             |
| Possibili superiori          | Dominio del [**contenitore**](c-container.md)del [**computer**](c-computer.md)[**:**](c-domaindns.md)[**unità organizzativa**](c-organizationalunit.md) DNS                   |
| Classi ausiliarie           | \-                                                                                                                                                                   |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                         |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-2000-server-attributes"></a>Attributi del server Windows 2000

Questa classe contiene gli attributi seguenti per Windows 2000 Server:



| Attributo                                                                 | Obbligatorio | Derivato da                                                                             |
|---------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Attributi consentiti**](a-allowedattributes.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md) | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Numero asset**](a-assetnumber.md)                                     | Falso     | **Coda di stampa**                                                                          |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Byte al minuto**](a-bytesperminute.md)                              | Falso     | **Coda di stampa**                                                                          |
| [**Nome canonico**](a-canonicalname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome comune**](a-cn.md)                                               | Vero      | [**Punto di connessione**](c-connectionpoint.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Creazione timestamp**](a-createtimestamp.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Priorità predefinita**](a-defaultpriority.md)                             | Falso     | **Coda di stampa**                                                                          |
| [**Descrizione**](a-description.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome visualizzato**](a-displayname.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome driver**](a-drivername.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Driver-versione**](a-driverversion.md)                                 | Falso     | **Coda di stampa**                                                                          |
| [**DSA-firma**](a-dsasignature.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome estensione**](a-extensionname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Bandiere**](a-flags.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Da-entry**](a-fromentry.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Tipo di istanza**](a-instancetype.md)                                   | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Viene eliminato**](a-isdeleted.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-member-of-DL**](a-memberof.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Parole chiave**](a-keywords.md)                                            | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Location**](a-location.md)                                            | Falso     | **Coda di stampa**                                                                          |
| [**Gestito da**](a-managedby.md)                                         | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**Oggetti gestiti**](a-managedobjects.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Mastered-by**](a-masteredby.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Modifica-timestamp**](a-modifytimestamp.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                  | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Categoria oggetto**](a-objectcategory.md)                               | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Classe Object**](a-objectclass.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**GUID oggetto**](a-objectguid.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Versione oggetto**](a-objectversion.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Sistema operativo**](a-operatingsystem.md)                             | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-hotfix**](a-operatingsystemhotfix.md)                | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-Service-Pack**](a-operatingsystemservicepack.md)     | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-versione**](a-operatingsystemversion.md)              | Falso     | **Coda di stampa**                                                                          |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md) | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Set di attributi parziali**](a-partialattributeset.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)              | Falso     | **Coda di stampa**                                                                          |
| [**Nome porta**](a-portname.md)                                           | Falso     | **Coda di stampa**                                                                          |
| [**Possibili-inferiori**](a-possibleinferiors.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Print-attributi**](a-printattributes.md)                             | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-bin-nomi**](a-printbinnames.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**Print-COLLATE**](a-printcollate.md)                                   | Falso     | **Coda di stampa**                                                                          |
| [**Colore stampa**](a-printcolor.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Print-duplex: supportato**](a-printduplexsupported.md)                  | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-ora di fine**](a-printendtime.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**Nome stampante**](a-printername.md)                                     | Vero      | **Coda di stampa**                                                                          |
| [**Nome-formato-stampa**](a-printformname.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-Mantieni-stampa-processi**](a-printkeepprintedjobs.md)                 | Falso     | **Coda di stampa**                                                                          |
| [**Lingua di stampa**](a-printlanguage.md)                                 | Falso     | **Coda di stampa**                                                                          |
| [**Print-MAC-Address**](a-printmacaddress.md)                            | Falso     | **Coda di stampa**                                                                          |
| [**Print-max-copie**](a-printmaxcopies.md)                              | Falso     | **Coda di stampa**                                                                          |
| [**Print-max-Resolution-supportato**](a-printmaxresolutionsupported.md)   | Falso     | **Coda di stampa**                                                                          |
| [**Print-Max-X-extent**](a-printmaxxextent.md)                           | Falso     | **Coda di stampa**                                                                          |
| [**Print-Max-Y-extent**](a-printmaxyextent.md)                           | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-pronto per supporti**](a-printmediaready.md)                            | Falso     | **Coda di stampa**                                                                          |
| [**Supporto di stampa**](a-printmediasupported.md)                    | Falso     | **Coda di stampa**                                                                          |
| [**Memoria di stampa**](a-printmemory.md)                                     | Falso     | **Coda di stampa**                                                                          |
| [**Print-min-X-extent**](a-printminxextent.md)                           | Falso     | **Coda di stampa**                                                                          |
| [**Print-min-Y-extent**](a-printminyextent.md)                           | Falso     | **Coda di stampa**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                    | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-notifica**](a-printnotify.md)                                     | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-numero**](a-printnumberup.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**Orientamento stampa-supportato**](a-printorientationssupported.md)      | Falso     | **Coda di stampa**                                                                          |
| [**Proprietario stampa**](a-printowner.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Pagine di stampa al minuto**](a-printpagesperminute.md)                   | Falso     | **Coda di stampa**                                                                          |
| [**Frequenza di stampa**](a-printrate.md)                                         | Falso     | **Coda di stampa**                                                                          |
| [**Frequenza di stampa-unità**](a-printrateunit.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**File separatore di stampa**](a-printseparatorfile.md)                      | Falso     | **Coda di stampa**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                              | Falso     | **Coda di stampa**                                                                          |
| [**Spooling di stampa**](a-printspooling.md)                                 | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-graffatura-supportata**](a-printstaplingsupported.md)              | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-ora di inizio**](a-printstarttime.md)                              | Falso     | **Coda di stampa**                                                                          |
| [**Stato di stampa**](a-printstatus.md)                                     | Falso     | **Coda di stampa**                                                                          |
| [**Priority**](a-priority.md)                                            | Falso     | **Coda di stampa**                                                                          |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Indirizzi proxy**](a-proxyaddresses.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Query-criteri-BL**](a-querypolicybl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**RDN**](a-name.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Report**](a-directreports.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Reps-da**](a-repsfrom.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Da Reps a**](a-repsto.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Revisione**](a-revision.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome server**](a-servername.md)                                       | Vero      | **Coda di stampa**                                                                          |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome-server breve**](a-shortservername.md)                            | Vero      | **Coda di stampa**                                                                          |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Riferimenti secondari**](a-subrefs.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Flag di sistema**](a-systemflags.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome UNC**](a-uncname.md)                                             | Vero      | **Coda di stampa**                                                                          |
| [**USN-modificato**](a-usnchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN creato**](a-usncreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-tra siti**](a-usnintersite.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-origine**](a-usnsource.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Numero di versione**](a-versionnumber.md)                                 | Vero      | **Coda di stampa**                                                                          |
| [**WBEM-percorso**](a-wbempath.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Oggetti noti**](a-wellknownobjects.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Quando-modificato**](a-whenchanged.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Data di creazione**](a-whencreated.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**WWW-pagina-altro**](a-url.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributes (Attributi)](#windows-server-2003-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                    |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                               |
| Sottoclasse di                 | [**Punto di connessione**](c-connectionpoint.md)<br/>                                                                                                             |
| Possibili superiori          | Dominio del [**contenitore**](c-container.md)del [**computer**](c-computer.md)[**:**](c-domaindns.md)[**unità organizzativa**](c-organizationalunit.md) DNS                   |
| Classi ausiliarie           | \-                                                                                                                                                                   |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                         |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2003-attributes"></a>Attributi di Windows Server 2003

Questa classe contiene gli attributi seguenti per Windows Server 2003:



| Attributo                                                                   | Obbligatorio | Derivato da                                                                             |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Numero asset**](a-assetnumber.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Byte al minuto**](a-bytesperminute.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**Nome canonico**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome comune**](a-cn.md)                                                 | Vero      | [**Punto di connessione**](c-connectionpoint.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Priorità predefinita**](a-defaultpriority.md)                               | Falso     | **Coda di stampa**                                                                          |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome driver**](a-drivername.md)                                         | Falso     | **Coda di stampa**                                                                          |
| [**Driver-versione**](a-driverversion.md)                                   | Falso     | **Coda di stampa**                                                                          |
| [**DSA-firma**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome estensione**](a-extensionname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Bandiere**](a-flags.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Da-entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Viene eliminato**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Parole chiave**](a-keywords.md)                                              | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Location**](a-location.md)                                              | Falso     | **Coda di stampa**                                                                          |
| [**Gestito da**](a-managedby.md)                                           | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Mastered-by**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Modifica-timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-impostazioni**](a-msds-settings.md)                                   | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Categoria oggetto**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Classe Object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**GUID oggetto**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Sistema operativo**](a-operatingsystem.md)                               | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-hotfix**](a-operatingsystemhotfix.md)                  | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-Service-Pack**](a-operatingsystemservicepack.md)       | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-versione**](a-operatingsystemversion.md)                | Falso     | **Coda di stampa**                                                                          |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Set di attributi parziali**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                | Falso     | **Coda di stampa**                                                                          |
| [**Nome porta**](a-portname.md)                                             | Falso     | **Coda di stampa**                                                                          |
| [**Possibili-inferiori**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Print-attributi**](a-printattributes.md)                               | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-bin-nomi**](a-printbinnames.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**Print-COLLATE**](a-printcollate.md)                                     | Falso     | **Coda di stampa**                                                                          |
| [**Colore stampa**](a-printcolor.md)                                         | Falso     | **Coda di stampa**                                                                          |
| [**Print-duplex: supportato**](a-printduplexsupported.md)                    | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-ora di fine**](a-printendtime.md)                                    | Falso     | **Coda di stampa**                                                                          |
| [**Nome stampante**](a-printername.md)                                       | Vero      | **Coda di stampa**                                                                          |
| [**Nome-formato-stampa**](a-printformname.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-Mantieni-stampa-processi**](a-printkeepprintedjobs.md)                   | Falso     | **Coda di stampa**                                                                          |
| [**Lingua di stampa**](a-printlanguage.md)                                   | Falso     | **Coda di stampa**                                                                          |
| [**Print-MAC-Address**](a-printmacaddress.md)                              | Falso     | **Coda di stampa**                                                                          |
| [**Print-max-copie**](a-printmaxcopies.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**Print-max-Resolution-supportato**](a-printmaxresolutionsupported.md)     | Falso     | **Coda di stampa**                                                                          |
| [**Print-Max-X-extent**](a-printmaxxextent.md)                             | Falso     | **Coda di stampa**                                                                          |
| [**Print-Max-Y-extent**](a-printmaxyextent.md)                             | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-pronto per supporti**](a-printmediaready.md)                              | Falso     | **Coda di stampa**                                                                          |
| [**Supporto di stampa**](a-printmediasupported.md)                      | Falso     | **Coda di stampa**                                                                          |
| [**Memoria di stampa**](a-printmemory.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Print-min-X-extent**](a-printminxextent.md)                             | Falso     | **Coda di stampa**                                                                          |
| [**Print-min-Y-extent**](a-printminyextent.md)                             | Falso     | **Coda di stampa**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                      | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-notifica**](a-printnotify.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-numero**](a-printnumberup.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**Orientamento stampa-supportato**](a-printorientationssupported.md)        | Falso     | **Coda di stampa**                                                                          |
| [**Proprietario stampa**](a-printowner.md)                                         | Falso     | **Coda di stampa**                                                                          |
| [**Pagine di stampa al minuto**](a-printpagesperminute.md)                     | Falso     | **Coda di stampa**                                                                          |
| [**Frequenza di stampa**](a-printrate.md)                                           | Falso     | **Coda di stampa**                                                                          |
| [**Frequenza di stampa-unità**](a-printrateunit.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**File separatore di stampa**](a-printseparatorfile.md)                        | Falso     | **Coda di stampa**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**Spooling di stampa**](a-printspooling.md)                                   | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-graffatura-supportata**](a-printstaplingsupported.md)                | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-ora di inizio**](a-printstarttime.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**Stato di stampa**](a-printstatus.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Priority**](a-priority.md)                                              | Falso     | **Coda di stampa**                                                                          |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Query-criteri-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**RDN**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Report**](a-directreports.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Reps-da**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Da Reps a**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome server**](a-servername.md)                                         | Vero      | **Coda di stampa**                                                                          |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome-server breve**](a-shortservername.md)                              | Vero      | **Coda di stampa**                                                                          |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome UNC**](a-uncname.md)                                               | Vero      | **Coda di stampa**                                                                          |
| [**USN-modificato**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN creato**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-tra siti**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-origine**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Numero di versione**](a-versionnumber.md)                                   | Vero      | **Coda di stampa**                                                                          |
| [**WBEM-percorso**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Quando-modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Data di creazione**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**WWW-pagina-altro**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributes (Attributi)](#windows-server-2003-r2-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                    |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                               |
| Sottoclasse di                 | [**Punto di connessione**](c-connectionpoint.md)<br/>                                                                                                             |
| Possibili superiori          | Dominio del [**contenitore**](c-container.md)del [**computer**](c-computer.md)[**:**](c-domaindns.md)[**unità organizzativa**](c-organizationalunit.md) DNS                   |
| Classi ausiliarie           | \-                                                                                                                                                                   |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                         |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2003-r2-attributes"></a>Attributi di Windows Server 2003 R2

Questa classe contiene gli attributi seguenti per Windows Server 2003 R2:



| Attributo                                                                   | Obbligatorio | Derivato da                                                                             |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Numero asset**](a-assetnumber.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Byte al minuto**](a-bytesperminute.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**Nome canonico**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome comune**](a-cn.md)                                                 | Vero      | [**Punto di connessione**](c-connectionpoint.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Priorità predefinita**](a-defaultpriority.md)                               | Falso     | **Coda di stampa**                                                                          |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome driver**](a-drivername.md)                                         | Falso     | **Coda di stampa**                                                                          |
| [**Driver-versione**](a-driverversion.md)                                   | Falso     | **Coda di stampa**                                                                          |
| [**DSA-firma**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome estensione**](a-extensionname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Bandiere**](a-flags.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Da-entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Viene eliminato**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Parole chiave**](a-keywords.md)                                              | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Location**](a-location.md)                                              | Falso     | **Coda di stampa**                                                                          |
| [**Gestito da**](a-managedby.md)                                           | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Mastered-by**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Modifica-timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-impostazioni**](a-msds-settings.md)                                   | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Categoria oggetto**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Classe Object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**GUID oggetto**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Sistema operativo**](a-operatingsystem.md)                               | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-hotfix**](a-operatingsystemhotfix.md)                  | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-Service-Pack**](a-operatingsystemservicepack.md)       | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-versione**](a-operatingsystemversion.md)                | Falso     | **Coda di stampa**                                                                          |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Set di attributi parziali**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                | Falso     | **Coda di stampa**                                                                          |
| [**Nome porta**](a-portname.md)                                             | Falso     | **Coda di stampa**                                                                          |
| [**Possibili-inferiori**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Print-attributi**](a-printattributes.md)                               | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-bin-nomi**](a-printbinnames.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**Print-COLLATE**](a-printcollate.md)                                     | Falso     | **Coda di stampa**                                                                          |
| [**Colore stampa**](a-printcolor.md)                                         | Falso     | **Coda di stampa**                                                                          |
| [**Print-duplex: supportato**](a-printduplexsupported.md)                    | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-ora di fine**](a-printendtime.md)                                    | Falso     | **Coda di stampa**                                                                          |
| [**Nome stampante**](a-printername.md)                                       | Vero      | **Coda di stampa**                                                                          |
| [**Nome-formato-stampa**](a-printformname.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-Mantieni-stampa-processi**](a-printkeepprintedjobs.md)                   | Falso     | **Coda di stampa**                                                                          |
| [**Lingua di stampa**](a-printlanguage.md)                                   | Falso     | **Coda di stampa**                                                                          |
| [**Print-MAC-Address**](a-printmacaddress.md)                              | Falso     | **Coda di stampa**                                                                          |
| [**Print-max-copie**](a-printmaxcopies.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**Print-max-Resolution-supportato**](a-printmaxresolutionsupported.md)     | Falso     | **Coda di stampa**                                                                          |
| [**Print-Max-X-extent**](a-printmaxxextent.md)                             | Falso     | **Coda di stampa**                                                                          |
| [**Print-Max-Y-extent**](a-printmaxyextent.md)                             | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-pronto per supporti**](a-printmediaready.md)                              | Falso     | **Coda di stampa**                                                                          |
| [**Supporto di stampa**](a-printmediasupported.md)                      | Falso     | **Coda di stampa**                                                                          |
| [**Memoria di stampa**](a-printmemory.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Print-min-X-extent**](a-printminxextent.md)                             | Falso     | **Coda di stampa**                                                                          |
| [**Print-min-Y-extent**](a-printminyextent.md)                             | Falso     | **Coda di stampa**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                      | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-notifica**](a-printnotify.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-numero**](a-printnumberup.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**Orientamento stampa-supportato**](a-printorientationssupported.md)        | Falso     | **Coda di stampa**                                                                          |
| [**Proprietario stampa**](a-printowner.md)                                         | Falso     | **Coda di stampa**                                                                          |
| [**Pagine di stampa al minuto**](a-printpagesperminute.md)                     | Falso     | **Coda di stampa**                                                                          |
| [**Frequenza di stampa**](a-printrate.md)                                           | Falso     | **Coda di stampa**                                                                          |
| [**Frequenza di stampa-unità**](a-printrateunit.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**File separatore di stampa**](a-printseparatorfile.md)                        | Falso     | **Coda di stampa**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**Spooling di stampa**](a-printspooling.md)                                   | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-graffatura-supportata**](a-printstaplingsupported.md)                | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-ora di inizio**](a-printstarttime.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**Stato di stampa**](a-printstatus.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Priority**](a-priority.md)                                              | Falso     | **Coda di stampa**                                                                          |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Query-criteri-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**RDN**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Report**](a-directreports.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Reps-da**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Da Reps a**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome server**](a-servername.md)                                         | Vero      | **Coda di stampa**                                                                          |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome-server breve**](a-shortservername.md)                              | Vero      | **Coda di stampa**                                                                          |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome UNC**](a-uncname.md)                                               | Vero      | **Coda di stampa**                                                                          |
| [**USN-modificato**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN creato**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-tra siti**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-origine**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Numero di versione**](a-versionnumber.md)                                   | Vero      | **Coda di stampa**                                                                          |
| [**WBEM-percorso**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Quando-modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Data di creazione**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**WWW-pagina-altro**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributes (Attributi)](#windows-server-2008-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                    |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                               |
| Sottoclasse di                 | [**Punto di connessione**](c-connectionpoint.md)<br/>                                                                                                             |
| Possibili superiori          | Dominio del [**contenitore**](c-container.md)del [**computer**](c-computer.md)[**:**](c-domaindns.md)[**unità organizzativa**](c-organizationalunit.md) DNS                   |
| Classi ausiliarie           | \-                                                                                                                                                                   |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                         |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2008-attributes"></a>Attributi di Windows Server 2008

Questa classe contiene gli attributi seguenti per Windows Server 2008:



| Attributo                                                                      | Obbligatorio | Derivato da                                                                             |
|--------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Attributi consentiti**](a-allowedattributes.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Numero asset**](a-assetnumber.md)                                          | Falso     | **Coda di stampa**                                                                          |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Byte al minuto**](a-bytesperminute.md)                                   | Falso     | **Coda di stampa**                                                                          |
| [**Nome canonico**](a-canonicalname.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome comune**](a-cn.md)                                                    | Vero      | [**Punto di connessione**](c-connectionpoint.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Creazione timestamp**](a-createtimestamp.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Priorità predefinita**](a-defaultpriority.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**Descrizione**](a-description.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome visualizzato**](a-displayname.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome driver**](a-drivername.md)                                            | Falso     | **Coda di stampa**                                                                          |
| [**Driver-versione**](a-driverversion.md)                                      | Falso     | **Coda di stampa**                                                                          |
| [**DSA-firma**](a-dsasignature.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome estensione**](a-extensionname.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Bandiere**](a-flags.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Da-entry**](a-fromentry.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Tipo di istanza**](a-instancetype.md)                                        | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Viene eliminato**](a-isdeleted.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-member-of-DL**](a-memberof.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Parole chiave**](a-keywords.md)                                                 | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Location**](a-location.md)                                                 | Falso     | **Coda di stampa**                                                                          |
| [**Gestito da**](a-managedby.md)                                              | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**Oggetti gestiti**](a-managedobjects.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Mastered-by**](a-masteredby.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-impostazioni**](a-msds-settings.md)                                      | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                       | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Categoria oggetto**](a-objectcategory.md)                                    | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Classe Object**](a-objectclass.md)                                          | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**GUID oggetto**](a-objectguid.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Versione oggetto**](a-objectversion.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Sistema operativo**](a-operatingsystem.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-hotfix**](a-operatingsystemhotfix.md)                     | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-Service-Pack**](a-operatingsystemservicepack.md)          | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-versione**](a-operatingsystemversion.md)                   | Falso     | **Coda di stampa**                                                                          |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Set di attributi parziali**](a-partialattributeset.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                   | Falso     | **Coda di stampa**                                                                          |
| [**Nome porta**](a-portname.md)                                                | Falso     | **Coda di stampa**                                                                          |
| [**Possibili-inferiori**](a-possibleinferiors.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Print-attributi**](a-printattributes.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-bin-nomi**](a-printbinnames.md)                                     | Falso     | **Coda di stampa**                                                                          |
| [**Print-COLLATE**](a-printcollate.md)                                        | Falso     | **Coda di stampa**                                                                          |
| [**Colore stampa**](a-printcolor.md)                                            | Falso     | **Coda di stampa**                                                                          |
| [**Print-duplex: supportato**](a-printduplexsupported.md)                       | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-ora di fine**](a-printendtime.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Nome stampante**](a-printername.md)                                          | Vero      | **Coda di stampa**                                                                          |
| [**Nome-formato-stampa**](a-printformname.md)                                     | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-Mantieni-stampa-processi**](a-printkeepprintedjobs.md)                      | Falso     | **Coda di stampa**                                                                          |
| [**Lingua di stampa**](a-printlanguage.md)                                      | Falso     | **Coda di stampa**                                                                          |
| [**Print-MAC-Address**](a-printmacaddress.md)                                 | Falso     | **Coda di stampa**                                                                          |
| [**Print-max-copie**](a-printmaxcopies.md)                                   | Falso     | **Coda di stampa**                                                                          |
| [**Print-max-Resolution-supportato**](a-printmaxresolutionsupported.md)        | Falso     | **Coda di stampa**                                                                          |
| [**Print-Max-X-extent**](a-printmaxxextent.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**Print-Max-Y-extent**](a-printmaxyextent.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-pronto per supporti**](a-printmediaready.md)                                 | Falso     | **Coda di stampa**                                                                          |
| [**Supporto di stampa**](a-printmediasupported.md)                         | Falso     | **Coda di stampa**                                                                          |
| [**Memoria di stampa**](a-printmemory.md)                                          | Falso     | **Coda di stampa**                                                                          |
| [**Print-min-X-extent**](a-printminxextent.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**Print-min-Y-extent**](a-printminyextent.md)                                | Falso     | **Coda di stampa**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                         | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-notifica**](a-printnotify.md)                                          | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-numero**](a-printnumberup.md)                                     | Falso     | **Coda di stampa**                                                                          |
| [**Orientamento stampa-supportato**](a-printorientationssupported.md)           | Falso     | **Coda di stampa**                                                                          |
| [**Proprietario stampa**](a-printowner.md)                                            | Falso     | **Coda di stampa**                                                                          |
| [**Pagine di stampa al minuto**](a-printpagesperminute.md)                        | Falso     | **Coda di stampa**                                                                          |
| [**Frequenza di stampa**](a-printrate.md)                                              | Falso     | **Coda di stampa**                                                                          |
| [**Frequenza di stampa-unità**](a-printrateunit.md)                                     | Falso     | **Coda di stampa**                                                                          |
| [**File separatore di stampa**](a-printseparatorfile.md)                           | Falso     | **Coda di stampa**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                   | Falso     | **Coda di stampa**                                                                          |
| [**Spooling di stampa**](a-printspooling.md)                                      | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-graffatura-supportata**](a-printstaplingsupported.md)                   | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-ora di inizio**](a-printstarttime.md)                                   | Falso     | **Coda di stampa**                                                                          |
| [**Stato di stampa**](a-printstatus.md)                                          | Falso     | **Coda di stampa**                                                                          |
| [**Priority**](a-priority.md)                                                 | Falso     | **Coda di stampa**                                                                          |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Query-criteri-BL**](a-querypolicybl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**RDN**](a-name.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Report**](a-directreports.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Reps-da**](a-repsfrom.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Da Reps a**](a-repsto.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Revisione**](a-revision.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome server**](a-servername.md)                                            | Vero      | **Coda di stampa**                                                                          |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome-server breve**](a-shortservername.md)                                 | Vero      | **Coda di stampa**                                                                          |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Riferimenti secondari**](a-subrefs.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Flag di sistema**](a-systemflags.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome UNC**](a-uncname.md)                                                  | Vero      | **Coda di stampa**                                                                          |
| [**USN-modificato**](a-usnchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN creato**](a-usncreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-tra siti**](a-usnintersite.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-origine**](a-usnsource.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Numero di versione**](a-versionnumber.md)                                      | Vero      | **Coda di stampa**                                                                          |
| [**WBEM-percorso**](a-wbempath.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Oggetti noti**](a-wellknownobjects.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Quando-modificato**](a-whenchanged.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Data di creazione**](a-whencreated.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**WWW-pagina-altro**](a-url.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributes (Attributi)](#windows-server-2008-r2-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                    |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                               |
| Sottoclasse di                 | [**Punto di connessione**](c-connectionpoint.md)<br/>                                                                                                             |
| Possibili superiori          | Dominio del [**contenitore**](c-container.md)del [**computer**](c-computer.md)[**:**](c-domaindns.md)[**unità organizzativa**](c-organizationalunit.md) DNS                   |
| Classi ausiliarie           | \-                                                                                                                                                                   |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                         |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2008-r2-attributes"></a>Attributi di Windows Server 2008 R2

Questa classe contiene gli attributi seguenti per Windows Server 2008 R2:



| Attributo                                                                        | Obbligatorio | Derivato da                                                                             |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Attributi consentiti**](a-allowedattributes.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Numero asset**](a-assetnumber.md)                                            | Falso     | **Coda di stampa**                                                                          |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Byte al minuto**](a-bytesperminute.md)                                     | Falso     | **Coda di stampa**                                                                          |
| [**Nome canonico**](a-canonicalname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome comune**](a-cn.md)                                                      | Vero      | [**Punto di connessione**](c-connectionpoint.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Creazione timestamp**](a-createtimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Priorità predefinita**](a-defaultpriority.md)                                    | Falso     | **Coda di stampa**                                                                          |
| [**Descrizione**](a-description.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome visualizzato**](a-displayname.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome driver**](a-drivername.md)                                              | Falso     | **Coda di stampa**                                                                          |
| [**Driver-versione**](a-driverversion.md)                                        | Falso     | **Coda di stampa**                                                                          |
| [**DSA-firma**](a-dsasignature.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome estensione**](a-extensionname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Bandiere**](a-flags.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Da-entry**](a-fromentry.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Tipo di istanza**](a-instancetype.md)                                          | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Viene eliminato**](a-isdeleted.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-member-of-DL**](a-memberof.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Riciclato**](a-isrecycled.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Parole chiave**](a-keywords.md)                                                   | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Location**](a-location.md)                                                   | Falso     | **Coda di stampa**                                                                          |
| [**Gestito da**](a-managedby.md)                                                | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**Oggetti gestiti**](a-managedobjects.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Mastered-by**](a-masteredby.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Enabled-feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-host-Service-account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-ultimo-noto-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-locale-effettivo-eliminazione-ora**](a-msds-localeffectivedeletiontime.md) | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-local-effective-riciclo-tempo**](a-msds-localeffectiverecycletime.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-impostazioni**](a-msds-settings.md)                                        | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                         | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Categoria oggetto**](a-objectcategory.md)                                      | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Classe Object**](a-objectclass.md)                                            | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**GUID oggetto**](a-objectguid.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Versione oggetto**](a-objectversion.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Sistema operativo**](a-operatingsystem.md)                                    | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-hotfix**](a-operatingsystemhotfix.md)                       | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-Service-Pack**](a-operatingsystemservicepack.md)            | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-versione**](a-operatingsystemversion.md)                     | Falso     | **Coda di stampa**                                                                          |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Set di attributi parziali**](a-partialattributeset.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                     | Falso     | **Coda di stampa**                                                                          |
| [**Nome porta**](a-portname.md)                                                  | Falso     | **Coda di stampa**                                                                          |
| [**Possibili-inferiori**](a-possibleinferiors.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Print-attributi**](a-printattributes.md)                                    | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-bin-nomi**](a-printbinnames.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Print-COLLATE**](a-printcollate.md)                                          | Falso     | **Coda di stampa**                                                                          |
| [**Colore stampa**](a-printcolor.md)                                              | Falso     | **Coda di stampa**                                                                          |
| [**Print-duplex: supportato**](a-printduplexsupported.md)                         | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-ora di fine**](a-printendtime.md)                                         | Falso     | **Coda di stampa**                                                                          |
| [**Nome stampante**](a-printername.md)                                            | Vero      | **Coda di stampa**                                                                          |
| [**Nome-formato-stampa**](a-printformname.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-Mantieni-stampa-processi**](a-printkeepprintedjobs.md)                        | Falso     | **Coda di stampa**                                                                          |
| [**Lingua di stampa**](a-printlanguage.md)                                        | Falso     | **Coda di stampa**                                                                          |
| [**Print-MAC-Address**](a-printmacaddress.md)                                   | Falso     | **Coda di stampa**                                                                          |
| [**Print-max-copie**](a-printmaxcopies.md)                                     | Falso     | **Coda di stampa**                                                                          |
| [**Print-max-Resolution-supportato**](a-printmaxresolutionsupported.md)          | Falso     | **Coda di stampa**                                                                          |
| [**Print-Max-X-extent**](a-printmaxxextent.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**Print-Max-Y-extent**](a-printmaxyextent.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-pronto per supporti**](a-printmediaready.md)                                   | Falso     | **Coda di stampa**                                                                          |
| [**Supporto di stampa**](a-printmediasupported.md)                           | Falso     | **Coda di stampa**                                                                          |
| [**Memoria di stampa**](a-printmemory.md)                                            | Falso     | **Coda di stampa**                                                                          |
| [**Print-min-X-extent**](a-printminxextent.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**Print-min-Y-extent**](a-printminyextent.md)                                  | Falso     | **Coda di stampa**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                           | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-notifica**](a-printnotify.md)                                            | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-numero**](a-printnumberup.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Orientamento stampa-supportato**](a-printorientationssupported.md)             | Falso     | **Coda di stampa**                                                                          |
| [**Proprietario stampa**](a-printowner.md)                                              | Falso     | **Coda di stampa**                                                                          |
| [**Pagine di stampa al minuto**](a-printpagesperminute.md)                          | Falso     | **Coda di stampa**                                                                          |
| [**Frequenza di stampa**](a-printrate.md)                                                | Falso     | **Coda di stampa**                                                                          |
| [**Frequenza di stampa-unità**](a-printrateunit.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**File separatore di stampa**](a-printseparatorfile.md)                             | Falso     | **Coda di stampa**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                     | Falso     | **Coda di stampa**                                                                          |
| [**Spooling di stampa**](a-printspooling.md)                                        | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-graffatura-supportata**](a-printstaplingsupported.md)                     | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-ora di inizio**](a-printstarttime.md)                                     | Falso     | **Coda di stampa**                                                                          |
| [**Stato di stampa**](a-printstatus.md)                                            | Falso     | **Coda di stampa**                                                                          |
| [**Priority**](a-priority.md)                                                   | Falso     | **Coda di stampa**                                                                          |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Query-criteri-BL**](a-querypolicybl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**RDN**](a-name.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Report**](a-directreports.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Reps-da**](a-repsfrom.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Da Reps a**](a-repsto.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Revisione**](a-revision.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome server**](a-servername.md)                                              | Vero      | **Coda di stampa**                                                                          |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome-server breve**](a-shortservername.md)                                   | Vero      | **Coda di stampa**                                                                          |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Riferimenti secondari**](a-subrefs.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Flag di sistema**](a-systemflags.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome UNC**](a-uncname.md)                                                    | Vero      | **Coda di stampa**                                                                          |
| [**USN-modificato**](a-usnchanged.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN creato**](a-usncreated.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-tra siti**](a-usnintersite.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-origine**](a-usnsource.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Numero di versione**](a-versionnumber.md)                                        | Vero      | **Coda di stampa**                                                                          |
| [**WBEM-percorso**](a-wbempath.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Oggetti noti**](a-wellknownobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Quando-modificato**](a-whenchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Data di creazione**](a-whencreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**WWW-pagina-altro**](a-url.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributes (Attributi)](#windows-server-2012-attributes)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                    |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                               |
| Sottoclasse di                 | [**Punto di connessione**](c-connectionpoint.md)<br/>                                                                                                             |
| Possibili superiori          | Dominio del [**contenitore**](c-container.md)del [**computer**](c-computer.md)[**:**](c-domaindns.md)[**unità organizzativa**](c-organizationalunit.md) DNS                   |
| Classi ausiliarie           | \-                                                                                                                                                                   |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                         |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A;; RPLCLORC;;; Au |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2012-attributes"></a>Attributi di Windows Server 2012

Questa classe contiene gli attributi seguenti per Windows Server 2012:



| Attributo                                                                                    | Obbligatorio | Derivato da                                                                             |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Attributi consentiti**](a-allowedattributes.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Numero asset**](a-assetnumber.md)                                                        | Falso     | **Coda di stampa**                                                                          |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Byte al minuto**](a-bytesperminute.md)                                                 | Falso     | **Coda di stampa**                                                                          |
| [**Nome canonico**](a-canonicalname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome comune**](a-cn.md)                                                                  | Vero      | [**Punto di connessione**](c-connectionpoint.md)<br/> [**In alto**](c-top.md)<br/> |
| [**Creazione timestamp**](a-createtimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Priorità predefinita**](a-defaultpriority.md)                                                | Falso     | **Coda di stampa**                                                                          |
| [**Descrizione**](a-description.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome visualizzato**](a-displayname.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome driver**](a-drivername.md)                                                          | Falso     | **Coda di stampa**                                                                          |
| [**Driver-versione**](a-driverversion.md)                                                    | Falso     | **Coda di stampa**                                                                          |
| [**DSA-firma**](a-dsasignature.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome estensione**](a-extensionname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Bandiere**](a-flags.md)                                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Da-entry**](a-fromentry.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Tipo di istanza**](a-instancetype.md)                                                      | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Viene eliminato**](a-isdeleted.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-member-of-DL**](a-memberof.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Riciclato**](a-isrecycled.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Parole chiave**](a-keywords.md)                                                               | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Location**](a-location.md)                                                               | Falso     | **Coda di stampa**                                                                          |
| [**Gestito da**](a-managedby.md)                                                            | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**Oggetti gestiti**](a-managedobjects.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Mastered-by**](a-masteredby.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Claim-shares-possible-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Enabled-feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-host-Service-account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-is-primary-computer-for**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-ultimo-noto-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-locale-effettivo-eliminazione-ora**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-local-effective-riciclo-tempo**](a-msds-localeffectiverecycletime.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-impostazioni**](a-msds-settings.md)                                                    | Falso     | [**Punto di connessione**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-TDO-uscita-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-TDO-ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-DS-valore-tipo-riferimento-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Categoria oggetto**](a-objectcategory.md)                                                  | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**Classe Object**](a-objectclass.md)                                                        | Vero      | [**In alto**](c-top.md)<br/>                                                          |
| [**GUID oggetto**](a-objectguid.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Versione oggetto**](a-objectversion.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Sistema operativo**](a-operatingsystem.md)                                                | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-hotfix**](a-operatingsystemhotfix.md)                                   | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-Service-Pack**](a-operatingsystemservicepack.md)                        | Falso     | **Coda di stampa**                                                                          |
| [**Sistema operativo-versione**](a-operatingsystemversion.md)                                 | Falso     | **Coda di stampa**                                                                          |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Set di attributi parziali**](a-partialattributeset.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Physical-Location-Object**](a-physicallocationobject.md)                                 | Falso     | **Coda di stampa**                                                                          |
| [**Nome porta**](a-portname.md)                                                              | Falso     | **Coda di stampa**                                                                          |
| [**Possibili-inferiori**](a-possibleinferiors.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Print-attributi**](a-printattributes.md)                                                | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-bin-nomi**](a-printbinnames.md)                                                   | Falso     | **Coda di stampa**                                                                          |
| [**Print-COLLATE**](a-printcollate.md)                                                      | Falso     | **Coda di stampa**                                                                          |
| [**Colore stampa**](a-printcolor.md)                                                          | Falso     | **Coda di stampa**                                                                          |
| [**Print-duplex: supportato**](a-printduplexsupported.md)                                     | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-ora di fine**](a-printendtime.md)                                                     | Falso     | **Coda di stampa**                                                                          |
| [**Nome stampante**](a-printername.md)                                                        | Vero      | **Coda di stampa**                                                                          |
| [**Nome-formato-stampa**](a-printformname.md)                                                   | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-Mantieni-stampa-processi**](a-printkeepprintedjobs.md)                                    | Falso     | **Coda di stampa**                                                                          |
| [**Lingua di stampa**](a-printlanguage.md)                                                    | Falso     | **Coda di stampa**                                                                          |
| [**Print-MAC-Address**](a-printmacaddress.md)                                               | Falso     | **Coda di stampa**                                                                          |
| [**Print-max-copie**](a-printmaxcopies.md)                                                 | Falso     | **Coda di stampa**                                                                          |
| [**Print-max-Resolution-supportato**](a-printmaxresolutionsupported.md)                      | Falso     | **Coda di stampa**                                                                          |
| [**Print-Max-X-extent**](a-printmaxxextent.md)                                              | Falso     | **Coda di stampa**                                                                          |
| [**Print-Max-Y-extent**](a-printmaxyextent.md)                                              | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-pronto per supporti**](a-printmediaready.md)                                               | Falso     | **Coda di stampa**                                                                          |
| [**Supporto di stampa**](a-printmediasupported.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Memoria di stampa**](a-printmemory.md)                                                        | Falso     | **Coda di stampa**                                                                          |
| [**Print-min-X-extent**](a-printminxextent.md)                                              | Falso     | **Coda di stampa**                                                                          |
| [**Print-min-Y-extent**](a-printminyextent.md)                                              | Falso     | **Coda di stampa**                                                                          |
| [**Print-Network-Address**](a-printnetworkaddress.md)                                       | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-notifica**](a-printnotify.md)                                                        | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-numero**](a-printnumberup.md)                                                   | Falso     | **Coda di stampa**                                                                          |
| [**Orientamento stampa-supportato**](a-printorientationssupported.md)                         | Falso     | **Coda di stampa**                                                                          |
| [**Proprietario stampa**](a-printowner.md)                                                          | Falso     | **Coda di stampa**                                                                          |
| [**Pagine di stampa al minuto**](a-printpagesperminute.md)                                      | Falso     | **Coda di stampa**                                                                          |
| [**Frequenza di stampa**](a-printrate.md)                                                            | Falso     | **Coda di stampa**                                                                          |
| [**Frequenza di stampa-unità**](a-printrateunit.md)                                                   | Falso     | **Coda di stampa**                                                                          |
| [**File separatore di stampa**](a-printseparatorfile.md)                                         | Falso     | **Coda di stampa**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                                 | Falso     | **Coda di stampa**                                                                          |
| [**Spooling di stampa**](a-printspooling.md)                                                    | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-graffatura-supportata**](a-printstaplingsupported.md)                                 | Falso     | **Coda di stampa**                                                                          |
| [**Stampa-ora di inizio**](a-printstarttime.md)                                                 | Falso     | **Coda di stampa**                                                                          |
| [**Stato di stampa**](a-printstatus.md)                                                        | Falso     | **Coda di stampa**                                                                          |
| [**Priority**](a-priority.md)                                                               | Falso     | **Coda di stampa**                                                                          |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Query-criteri-BL**](a-querypolicybl.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**RDN**](a-name.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Report**](a-directreports.md)                                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Reps-da**](a-repsfrom.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Da Reps a**](a-repsto.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Revisione**](a-revision.md)                                                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome server**](a-servername.md)                                                          | Vero      | **Coda di stampa**                                                                          |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome-server breve**](a-shortservername.md)                                               | Vero      | **Coda di stampa**                                                                          |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Riferimenti secondari**](a-subrefs.md)                                                                | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Flag di sistema**](a-systemflags.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Nome UNC**](a-uncname.md)                                                                | Vero      | **Coda di stampa**                                                                          |
| [**USN-modificato**](a-usnchanged.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN creato**](a-usncreated.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-tra siti**](a-usnintersite.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**USN-origine**](a-usnsource.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Numero di versione**](a-versionnumber.md)                                                    | Vero      | **Coda di stampa**                                                                          |
| [**WBEM-percorso**](a-wbempath.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Oggetti noti**](a-wellknownobjects.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Quando-modificato**](a-whenchanged.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**Data di creazione**](a-whencreated.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                                          |
| [**WWW-pagina-altro**](a-url.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                                          |



 

 





