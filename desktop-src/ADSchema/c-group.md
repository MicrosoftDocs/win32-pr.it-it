---
title: Group (classe)
description: Archivia un elenco di nomi utente. Utilizzato per applicare le entità di sicurezza sulle risorse.
ms.assetid: e8ce5c43-d0fb-4c67-a6ef-7094fb7e7669
ms.tgt_platform: multiple
keywords:
- Classe gruppo-schema AD
- Classe gruppo-schema AD
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 618adb97220f4cc1b1e4af7f42fd043c7bb1e6c5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104121915"
---
# <a name="group-class"></a>Group (classe)

Archivia un elenco di nomi utente. Utilizzato per applicare le entità di sicurezza sulle risorse.



| Voce | Valore |
|-------------------|------------------------------------------------|
| CN                | Group                                          |
| LDAP-Display-Name | group                                          |
| Privilegio aggiornamento  | Questo valore viene impostato dall'amministratore di dominio. |
| Frequenza di aggiornamento  | \-                                             |
| Schema-ID-GUID    | bf967a9c-0de6-11d0-a285-00aa003049e2           |



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
-   [Scritture convalidate](#windows-2000-server-validated-writes)
-   [Set di proprietà](#windows-2000-server-property-sets)



| Voce | Valore |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                               |
| Object-Category             | 1                                                                                                                                                                                                   |
| Default-Object-Category     | \-                                                                                                                                                                                                  |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                                                   |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                              |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                     |
| Possibili superiori          | [**Dominio-**](c-domaindns.md)[**unità organizzativa**](c-organizationalunit.md)DNS [**-dominio**](c-container.md) [**incorporato**](c-builtindomain.md)                                       |
| Classi ausiliarie           | [**Sicurezza-**](c-securityprincipal.md) [**destinatario posta elettronica**](c-mailrecipient.md) (sistema)-destinatario (sistema)                                                                                        |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                                                        |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; Au |
| System-Flags                | 0x00000010                                                                                                                                                                                          |



## <a name="windows-2000-server-attributes"></a>Attributi del server Windows 2000

Questa classe contiene gli attributi seguenti per Windows 2000 Server:



| Attributo                                                                    | Obbligatorio | Derivato da                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Nome-account-cronologia**](a-accountnamehistory.md)                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Amministratore-conteggio**](a-admincount.md)                                          | Falso     | **Gruppo**                                                                                    |
| [**Admin-Descrizione**](a-admindescription.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Attributi consentiti**](a-allowedattributes.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Alt-sicurezza-identità**](a-altsecurityidentities.md)                   | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Nome canonico**](a-canonicalname.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Commento**](a-info.md)                                                    | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**Nome comune**](a-cn.md)                                                  | Vero      | [**In alto**](c-top.md)<br/> [**Destinatario posta**](c-mailrecipient.md)<br/>         |
| [**Controllo-accesso-diritti**](a-controlaccessrights.md)                       | Falso     | **Gruppo**                                                                                    |
| [**Creazione timestamp**](a-createtimestamp.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Descrizione**](a-description.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Profilo desktop**](a-desktopprofile.md)                                  | Falso     | **Gruppo**                                                                                    |
| [**Nome visualizzato**](a-displayname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**DSA-firma**](a-dsasignature.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Indirizzi di posta elettronica**](a-mail.md)                                           | Falso     | **Gruppo**                                                                                    |
| [**Nome estensione**](a-extensionname.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Bandiere**](a-flags.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Da-entry**](a-fromentry.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Garbage-Coll-period**](a-garbagecollperiod.md)                           | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**Attributi di gruppo**](a-groupattributes.md)                                | Falso     | **Gruppo**                                                                                    |
| [**Gruppo-appartenenza-SAM**](a-groupmembershipsam.md)                         | Falso     | **Gruppo**                                                                                    |
| [**Tipo di gruppo**](a-grouptype.md)                                            | Vero      | **Gruppo**                                                                                    |
| [**Tipo di istanza**](a-instancetype.md)                                      | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Viene eliminato**](a-isdeleted.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-member-of-DL**](a-memberof.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**DN-Exchange legacy**](a-legacyexchangedn.md)                             | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**Gestito da**](a-managedby.md)                                            | Falso     | **Gruppo**                                                                                    |
| [**Oggetti gestiti**](a-managedobjects.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Mastered-by**](a-masteredby.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Membro**](a-member.md)                                                   | Falso     | **Gruppo**                                                                                    |
| [**Modifica-timestamp**](a-modifytimestamp.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**-SCP-BL**](a-netbootscpbl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Membro non di sicurezza**](a-nonsecuritymember.md)                           | Falso     | **Gruppo**                                                                                    |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**NT-gruppo-membri**](a-ntgroupmembers.md)                                 | Falso     | **Gruppo**                                                                                    |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                     | Vero      | [**In alto**](c-top.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Categoria oggetto**](a-objectcategory.md)                                  | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Classe Object**](a-objectclass.md)                                        | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**GUID oggetto**](a-objectguid.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Oggetto-SID**](a-objectsid.md)                                            | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Versione oggetto**](a-objectversion.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Operatore-conteggio**](a-operatorcount.md)                                    | Falso     | **Gruppo**                                                                                    |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Set di attributi parziali**](a-partialattributeset.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Possibili-inferiori**](a-possibleinferiors.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Primary-Group-token**](a-primarygrouptoken.md)                           | Falso     | **Gruppo**                                                                                    |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Query-criteri-BL**](a-querypolicybl.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Report**](a-directreports.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Reps-da**](a-repsfrom.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Da Reps a**](a-repsto.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Revisione**](a-revision.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Sbarazzarsi**](a-rid.md)                                                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Nome account SAM**](a-samaccountname.md)                                 | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Tipo di account SAM**](a-samaccounttype.md)                                 | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Identificatore di sicurezza**](a-securityidentifier.md)                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Mostra-in-indirizzo-libro**](a-showinaddressbook.md)                          | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SID-cronologia**](a-sidhistory.md)                                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Riferimenti secondari**](a-subrefs.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Supplementare-credenziali**](a-supplementalcredentials.md)                | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Flag di sistema**](a-systemflags.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Numero di telefono**](a-telephonenumber.md)                                | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**Con codifica di testo o indirizzo**](a-textencodedoraddress.md)                    | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**Gruppi di token**](a-tokengroups.md)                                        | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Token-gruppi-globale e universale**](a-tokengroupsglobalanduniversal.md) | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-No-GC-accettabile**](a-tokengroupsnogcacceptable.md)         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Certificato utente**](a-usercert.md)                                              | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**User-SMIME-certificate**](a-usersmimecertificate.md)                     | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**USN-modificato**](a-usnchanged.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN creato**](a-usncreated.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-tra siti**](a-usnintersite.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-origine**](a-usnsource.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WBEM-percorso**](a-wbempath.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Oggetti noti**](a-wellknownobjects.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Quando-modificato**](a-whenchanged.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Data di creazione**](a-whencreated.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WWW-pagina-altro**](a-url.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**X509-Cert**](a-usercertificate.md)                                       | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-2000-server-extended-rights"></a>Diritti estesi del server Windows 2000

Questa classe contiene i seguenti diritti estesi per Windows Server 2000:



| Nome comune                  |
|------------------------------|
| [**Invia a**](r-send-to.md) |



## <a name="windows-2000-server-validated-writes"></a>Scritture convalidate per Windows Server 2000

Questa classe contiene le seguenti scritture convalidate per Windows 2000 Server:



| Nome comune                                  |
|----------------------------------------------|
| [**Appartenenza automatica**](r-self-membership.md) |



## <a name="windows-2000-server-property-sets"></a>Set di proprietà del server Windows 2000

Questa classe contiene i set di proprietà seguenti per Windows Server 2000:



| Nome comune                                      |
|--------------------------------------------------|
| [**Posta elettronica-informazioni**](r-email-information.md) |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributes (Attributi)](#windows-server-2003-attributes)
-   [Diritti estesi](#windows-server-2003-extended-rights)
-   [Scritture convalidate](#windows-server-2003-validated-writes)
-   [Set di proprietà](#windows-server-2003-property-sets)



| Voce | Valore |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Possibili superiori          | [**Dominio-**](c-domaindns.md)[**unità organizzativa**](c-organizationalunit.md)[**DNS incorporata-**](c-builtindomain.md)[**contenitore**](c-container.md)di dominio [**ms-DS-AZ-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-AZ-Application**](c-msds-azapplication.md)[**ms-DS-AZ-scope**](c-msds-azscope.md) |
| Classi ausiliarie           | [**Sicurezza-**](c-securityprincipal.md) [**destinatario posta elettronica**](c-mailrecipient.md) (sistema)-destinatario (sistema)                                                                                                                                                                                                     |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                     |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60AE-405A-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-attributes"></a>Attributi di Windows Server 2003

Questa classe contiene gli attributi seguenti per Windows Server 2003:



| Attributo                                                                    | Obbligatorio | Derivato da                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Nome-account-cronologia**](a-accountnamehistory.md)                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Amministratore-conteggio**](a-admincount.md)                                          | Falso     | **Gruppo**                                                                                    |
| [**Admin-Descrizione**](a-admindescription.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Attributi consentiti**](a-allowedattributes.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Alt-sicurezza-identità**](a-altsecurityidentities.md)                   | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Nome canonico**](a-canonicalname.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Commento**](a-info.md)                                                    | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**Nome comune**](a-cn.md)                                                  | Vero      | [**In alto**](c-top.md)<br/> [**Destinatario posta**](c-mailrecipient.md)<br/>         |
| [**Controllo-accesso-diritti**](a-controlaccessrights.md)                       | Falso     | **Gruppo**                                                                                    |
| [**Creazione timestamp**](a-createtimestamp.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Descrizione**](a-description.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Profilo desktop**](a-desktopprofile.md)                                  | Falso     | **Gruppo**                                                                                    |
| [**Nome visualizzato**](a-displayname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**DSA-firma**](a-dsasignature.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Indirizzi di posta elettronica**](a-mail.md)                                           | Falso     | **Gruppo**                                                                                    |
| [**Nome estensione**](a-extensionname.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Bandiere**](a-flags.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Da-entry**](a-fromentry.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Garbage-Coll-period**](a-garbagecollperiod.md)                           | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**Attributi di gruppo**](a-groupattributes.md)                                | Falso     | **Gruppo**                                                                                    |
| [**Gruppo-appartenenza-SAM**](a-groupmembershipsam.md)                         | Falso     | **Gruppo**                                                                                    |
| [**Tipo di gruppo**](a-grouptype.md)                                            | Vero      | **Gruppo**                                                                                    |
| [**Tipo di istanza**](a-instancetype.md)                                      | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Viene eliminato**](a-isdeleted.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-member-of-DL**](a-memberof.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**labeledURI**](a-labeleduri.md)                                           | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**DN-Exchange legacy**](a-legacyexchangedn.md)                             | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**Gestito da**](a-managedby.md)                                            | Falso     | **Gruppo**                                                                                    |
| [**Oggetti gestiti**](a-managedobjects.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Mastered-by**](a-masteredby.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Membro**](a-member.md)                                                   | Falso     | **Gruppo**                                                                                    |
| [**Modifica-timestamp**](a-modifytimestamp.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-AZ-LDAP-query**](a-msds-azldapquery.md)                            | Falso     | **Gruppo**                                                                                    |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                    | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-non membri**](a-msds-nonmembers.md)                               | Falso     | **Gruppo**                                                                                    |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                      | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**-SCP-BL**](a-netbootscpbl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Membro non di sicurezza**](a-nonsecuritymember.md)                           | Falso     | **Gruppo**                                                                                    |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**NT-gruppo-membri**](a-ntgroupmembers.md)                                 | Falso     | **Gruppo**                                                                                    |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                     | Vero      | [**In alto**](c-top.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Categoria oggetto**](a-objectcategory.md)                                  | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Classe Object**](a-objectclass.md)                                        | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**GUID oggetto**](a-objectguid.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Oggetto-SID**](a-objectsid.md)                                            | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Versione oggetto**](a-objectversion.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Operatore-conteggio**](a-operatorcount.md)                                    | Falso     | **Gruppo**                                                                                    |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Set di attributi parziali**](a-partialattributeset.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Possibili-inferiori**](a-possibleinferiors.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Primary-Group-token**](a-primarygrouptoken.md)                           | Falso     | **Gruppo**                                                                                    |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Query-criteri-BL**](a-querypolicybl.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Report**](a-directreports.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Reps-da**](a-repsfrom.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Da Reps a**](a-repsto.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Revisione**](a-revision.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Sbarazzarsi**](a-rid.md)                                                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Nome account SAM**](a-samaccountname.md)                                 | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Tipo di account SAM**](a-samaccounttype.md)                                 | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**segretaria**](a-secretary.md)                                             | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**Identificatore di sicurezza**](a-securityidentifier.md)                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Mostra-in-indirizzo-libro**](a-showinaddressbook.md)                          | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SID-cronologia**](a-sidhistory.md)                                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Riferimenti secondari**](a-subrefs.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Supplementare-credenziali**](a-supplementalcredentials.md)                | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Flag di sistema**](a-systemflags.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Numero di telefono**](a-telephonenumber.md)                                | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**Con codifica di testo o indirizzo**](a-textencodedoraddress.md)                    | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**Gruppi di token**](a-tokengroups.md)                                        | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Token-gruppi-globale e universale**](a-tokengroupsglobalanduniversal.md) | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-No-GC-accettabile**](a-tokengroupsnogcacceptable.md)         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Certificato utente**](a-usercert.md)                                              | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**User-SMIME-certificate**](a-usersmimecertificate.md)                     | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |
| [**USN-modificato**](a-usnchanged.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN creato**](a-usncreated.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-tra siti**](a-usnintersite.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-origine**](a-usnsource.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WBEM-percorso**](a-wbempath.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Oggetti noti**](a-wellknownobjects.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Quando-modificato**](a-whenchanged.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Data di creazione**](a-whencreated.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WWW-pagina-altro**](a-url.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**X509-Cert**](a-usercertificate.md)                                       | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-server-2003-extended-rights"></a>Diritti estesi di Windows Server 2003

Questa classe contiene i seguenti diritti estesi per Windows Server 2003:



| Nome comune                  |
|------------------------------|
| [**Invia a**](r-send-to.md) |



## <a name="windows-server-2003-validated-writes"></a>Scritture convalidate per Windows Server 2003

Questa classe contiene le seguenti scritture convalidate per Windows Server 2003:



| Nome comune                                  |
|----------------------------------------------|
| [**Appartenenza automatica**](r-self-membership.md) |



## <a name="windows-server-2003-property-sets"></a>Set di proprietà di Windows Server 2003

Questa classe contiene i set di proprietà seguenti per Windows Server 2003:



| Nome comune                                      |
|--------------------------------------------------|
| [**Posta elettronica-informazioni**](r-email-information.md) |



## <a name="adam"></a>ADAM

-   [Attributes (Attributi)](#adam-attributes)
-   [Scritture convalidate](#adam-validated-writes)
-   [Set di proprietà](#adam-property-sets)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                |
| Object-Category             | 1                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                 |
| Valore predefinito-nascondiglio        | 0                                                                                                                    |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                                               |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                      |
| Possibili superiori          | [**Dominio-**](c-domaindns.md)[**contenitore**](c-container.md) di [**unità organizzative**](c-organizationalunit.md)DNS |
| Classi ausiliarie           | [**Sicurezza-entità di sicurezza**](c-securityprincipal.md) (sistema)                                                           |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                         |
| Descrittore di sicurezza predefinito | D:S                                                                                                                 |
| System-Flags                | 0x00000010                                                                                                           |



## <a name="adam-attributes"></a>Attributi ADAM

Questa classe contiene gli attributi seguenti per ADAM:



| Attributo                                                                   | Obbligatorio | Derivato da                                                                                 |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Admin-Descrizione**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Nome canonico**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Nome comune**](a-cn.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Profilo desktop**](a-desktopprofile.md)                                 | Falso     | **Gruppo**                                                                                    |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**DSA-firma**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Da-entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Tipo di gruppo**](a-grouptype.md)                                           | Vero      | **Gruppo**                                                                                    |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Viene eliminato**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-member-of-DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Gestito da**](a-managedby.md)                                           | Falso     | **Gruppo**                                                                                    |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Mastered-by**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Membro**](a-member.md)                                                  | Falso     | **Gruppo**                                                                                    |
| [**Modifica-timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-service-account-BL**](a-msds-serviceaccountbl.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Categoria oggetto**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Classe Object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**GUID oggetto**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Oggetto-SID**](a-objectsid.md)                                           | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Set di attributi parziali**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Possibili-inferiori**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Primary-Group-token**](a-primarygrouptoken.md)                          | Falso     | **Gruppo**                                                                                    |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Query-criteri-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Reps-da**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Da Reps a**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Riferimenti secondari**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Supplementare-credenziali**](a-supplementalcredentials.md)               | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Gruppi di token**](a-tokengroups.md)                                       | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**USN-modificato**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN creato**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-tra siti**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-origine**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WBEM-percorso**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Quando-modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Data di creazione**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WWW-pagina-altro**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |



## <a name="adam-validated-writes"></a>Scritture convalidate da ADAM

Questa classe contiene le seguenti scritture convalidate per ADAM:



| Nome comune                                  |
|----------------------------------------------|
| [**Appartenenza automatica**](r-self-membership.md) |



## <a name="adam-property-sets"></a>Set di proprietà ADAM

Questa classe contiene i set di proprietà seguenti per ADAM:



| Nome comune                                      |
|--------------------------------------------------|
| [**Posta elettronica-informazioni**](r-email-information.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributes (Attributi)](#windows-server-2003-r2-attributes)
-   [Diritti estesi](#windows-server-2003-r2-extended-rights)
-   [Scritture convalidate](#windows-server-2003-r2-validated-writes)
-   [Set di proprietà](#windows-server-2003-r2-property-sets)



| Voce | Valore |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Possibili superiori          | [**Dominio-**](c-domaindns.md)[**unità organizzativa**](c-organizationalunit.md)[**DNS incorporata-**](c-builtindomain.md)[**contenitore**](c-container.md)di dominio [**ms-DS-AZ-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-AZ-Application**](c-msds-azapplication.md)[**ms-DS-AZ-scope**](c-msds-azscope.md) |
| Classi ausiliarie           | [**posixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**mail-destinatario**](c-mailrecipient.md) (sistema)                                                                                                                                                                   |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                     |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60AE-405A-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-r2-attributes"></a>Attributi di Windows Server 2003 R2

Questa classe contiene gli attributi seguenti per Windows Server 2003 R2:



| Attributo                                                                    | Obbligatorio | Derivato da                                                                                                                       |
|------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome-account-cronologia**](a-accountnamehistory.md)                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Amministratore-conteggio**](a-admincount.md)                                          | Falso     | **Gruppo**                                                                                                                          |
| [**Admin-Descrizione**](a-admindescription.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Attributi consentiti**](a-allowedattributes.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Alt-sicurezza-identità**](a-altsecurityidentities.md)                   | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Nome canonico**](a-canonicalname.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Commento**](a-info.md)                                                    | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Nome comune**](a-cn.md)                                                  | Vero      | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario posta**](c-mailrecipient.md)<br/> |
| [**Controllo-accesso-diritti**](a-controlaccessrights.md)                       | Falso     | **Gruppo**                                                                                                                          |
| [**Creazione timestamp**](a-createtimestamp.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Descrizione**](a-description.md)                                         | Falso     | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Profilo desktop**](a-desktopprofile.md)                                  | Falso     | **Gruppo**                                                                                                                          |
| [**Nome visualizzato**](a-displayname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DSA-firma**](a-dsasignature.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi di posta elettronica**](a-mail.md)                                           | Falso     | **Gruppo**                                                                                                                          |
| [**Nome estensione**](a-extensionname.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Bandiere**](a-flags.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Da-entry**](a-fromentry.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Garbage-Coll-period**](a-garbagecollperiod.md)                           | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                             | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Attributi di gruppo**](a-groupattributes.md)                                | Falso     | **Gruppo**                                                                                                                          |
| [**Gruppo-appartenenza-SAM**](a-groupmembershipsam.md)                         | Falso     | **Gruppo**                                                                                                                          |
| [**Tipo di gruppo**](a-grouptype.md)                                            | Vero      | **Gruppo**                                                                                                                          |
| [**Tipo di istanza**](a-instancetype.md)                                      | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Viene eliminato**](a-isdeleted.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-member-of-DL**](a-memberof.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                           | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DN-Exchange legacy**](a-legacyexchangedn.md)                             | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Gestito da**](a-managedby.md)                                            | Falso     | **Gruppo**                                                                                                                          |
| [**Oggetti gestiti**](a-managedobjects.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Mastered-by**](a-masteredby.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Membro**](a-member.md)                                                   | Falso     | **Gruppo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                             | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modifica-timestamp**](a-modifytimestamp.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-LDAP-query**](a-msds-azldapquery.md)                            | Falso     | **Gruppo**                                                                                                                          |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                    | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-non membri**](a-msds-nonmembers.md)                               | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                      | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Attributo msSFU-30-nome**](a-mssfu30name.md)                                       | Falso     | **Gruppo**                                                                                                                          |
| [**Attributo msSFU-30-NIS-domain**](a-mssfu30nisdomain.md)                            | Falso     | **Gruppo**                                                                                                                          |
| [**Attributo msSFU-30-POSIX-membro**](a-mssfu30posixmember.md)                        | Falso     | **Gruppo**                                                                                                                          |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**-SCP-BL**](a-netbootscpbl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Membro non di sicurezza**](a-nonsecuritymember.md)                           | Falso     | **Gruppo**                                                                                                                          |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**NT-gruppo-membri**](a-ntgroupmembers.md)                                 | Falso     | **Gruppo**                                                                                                                          |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                     | Vero      | [**In alto**](c-top.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Categoria oggetto**](a-objectcategory.md)                                  | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classe Object**](a-objectclass.md)                                        | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**GUID oggetto**](a-objectguid.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Oggetto-SID**](a-objectsid.md)                                            | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Versione oggetto**](a-objectversion.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Operatore-conteggio**](a-operatorcount.md)                                    | Falso     | **Gruppo**                                                                                                                          |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Set di attributi parziali**](a-partialattributeset.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Possibili-inferiori**](a-possibleinferiors.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-token**](a-primarygrouptoken.md)                           | Falso     | **Gruppo**                                                                                                                          |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Query-criteri-BL**](a-querypolicybl.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Report**](a-directreports.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Reps-da**](a-repsfrom.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Da Reps a**](a-repsto.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Revisione**](a-revision.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Sbarazzarsi**](a-rid.md)                                                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Nome account SAM**](a-samaccountname.md)                                 | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Tipo di account SAM**](a-samaccounttype.md)                                 | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**segretaria**](a-secretary.md)                                             | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificatore di sicurezza**](a-securityidentifier.md)                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Mostra-in-indirizzo-libro**](a-showinaddressbook.md)                          | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**SID-cronologia**](a-sidhistory.md)                                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Riferimenti secondari**](a-subrefs.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Supplementare-credenziali**](a-supplementalcredentials.md)                | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Flag di sistema**](a-systemflags.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Numero di telefono**](a-telephonenumber.md)                                | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Con codifica di testo o indirizzo**](a-textencodedoraddress.md)                    | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Gruppi di token**](a-tokengroups.md)                                        | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-gruppi-globale e universale**](a-tokengroupsglobalanduniversal.md) | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-accettabile**](a-tokengroupsnogcacceptable.md)         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                               | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificato utente**](a-usercert.md)                                              | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Password utente**](a-userpassword.md)                                      | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-certificate**](a-usersmimecertificate.md)                     | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-modificato**](a-usnchanged.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN creato**](a-usncreated.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-tra siti**](a-usnintersite.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-origine**](a-usnsource.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WBEM-percorso**](a-wbempath.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Oggetti noti**](a-wellknownobjects.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Quando-modificato**](a-whenchanged.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Data di creazione**](a-whencreated.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WWW-pagina-altro**](a-url.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                       | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2003-r2-extended-rights"></a>Diritti estesi di Windows Server 2003 R2

Questa classe contiene i seguenti diritti estesi per Windows Server 2003 R2:



| Nome comune                  |
|------------------------------|
| [**Invia a**](r-send-to.md) |



## <a name="windows-server-2003-r2-validated-writes"></a>Scritture convalidate di Windows Server 2003 R2

Questa classe contiene le seguenti scritture convalidate per Windows Server 2003 R2:



| Nome comune                                  |
|----------------------------------------------|
| [**Appartenenza automatica**](r-self-membership.md) |



## <a name="windows-server-2003-r2-property-sets"></a>Set di proprietà di Windows Server 2003 R2

Questa classe contiene i set di proprietà seguenti per Windows Server 2003 R2:



| Nome comune                                      |
|--------------------------------------------------|
| [**Posta elettronica-informazioni**](r-email-information.md) |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributes (Attributi)](#windows-server-2008-attributes)
-   [Diritti estesi](#windows-server-2008-extended-rights)
-   [Scritture convalidate](#windows-server-2008-validated-writes)
-   [Set di proprietà](#windows-server-2008-property-sets)



| Voce | Valore |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Possibili superiori          | [**Dominio-**](c-domaindns.md)[**unità organizzativa**](c-organizationalunit.md)[**DNS incorporata-**](c-builtindomain.md)[**contenitore**](c-container.md)di dominio [**ms-DS-AZ-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-AZ-Application**](c-msds-azapplication.md)[**ms-DS-AZ-scope**](c-msds-azscope.md) |
| Classi ausiliarie           | [**posixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**mail-destinatario**](c-mailrecipient.md) (sistema)                                                                                                                                                                   |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                     |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60AE-405A-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-attributes"></a>Attributi di Windows Server 2008

Questa classe contiene gli attributi seguenti per Windows Server 2008:



| Attributo                                                                        | Obbligatorio | Derivato da                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome-account-cronologia**](a-accountnamehistory.md)                             | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Amministratore-conteggio**](a-admincount.md)                                              | Falso     | **Gruppo**                                                                                                                          |
| [**Admin-Descrizione**](a-admindescription.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Attributi consentiti**](a-allowedattributes.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Alt-sicurezza-identità**](a-altsecurityidentities.md)                       | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Nome canonico**](a-canonicalname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Commento**](a-info.md)                                                        | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Nome comune**](a-cn.md)                                                      | Vero      | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario posta**](c-mailrecipient.md)<br/> |
| [**Controllo-accesso-diritti**](a-controlaccessrights.md)                           | Falso     | **Gruppo**                                                                                                                          |
| [**Creazione timestamp**](a-createtimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Descrizione**](a-description.md)                                             | Falso     | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Profilo desktop**](a-desktopprofile.md)                                      | Falso     | **Gruppo**                                                                                                                          |
| [**Nome visualizzato**](a-displayname.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DSA-firma**](a-dsasignature.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi di posta elettronica**](a-mail.md)                                               | Falso     | **Gruppo**                                                                                                                          |
| [**Nome estensione**](a-extensionname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Bandiere**](a-flags.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Da-entry**](a-fromentry.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Garbage-Coll-period**](a-garbagecollperiod.md)                               | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Attributi di gruppo**](a-groupattributes.md)                                    | Falso     | **Gruppo**                                                                                                                          |
| [**Gruppo-appartenenza-SAM**](a-groupmembershipsam.md)                             | Falso     | **Gruppo**                                                                                                                          |
| [**Tipo di gruppo**](a-grouptype.md)                                                | Vero      | **Gruppo**                                                                                                                          |
| [**Tipo di istanza**](a-instancetype.md)                                          | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Viene eliminato**](a-isdeleted.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-member-of-DL**](a-memberof.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DN-Exchange legacy**](a-legacyexchangedn.md)                                 | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Gestito da**](a-managedby.md)                                                | Falso     | **Gruppo**                                                                                                                          |
| [**Oggetti gestiti**](a-managedobjects.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Mastered-by**](a-masteredby.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Membro**](a-member.md)                                                       | Falso     | **Gruppo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                    | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule**](a-msds-azbizrule.md)                                    | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule-Language**](a-msds-azbizrulelanguage.md)                   | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-Generic-Data**](a-msds-azgenericdata.md)                            | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-Last-importated-biz-rule-path**](a-msds-azlastimportedbizrulepath.md) | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-LDAP-query**](a-msds-azldapquery.md)                                | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                              | Falso     | **Gruppo**                                                                                                                          |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                        | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-non membri**](a-msds-nonmembers.md)                                   | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-fonetica-Display-Name**](a-msds-phoneticdisplayname.md)                | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Attributo msSFU-30-nome**](a-mssfu30name.md)                                           | Falso     | **Gruppo**                                                                                                                          |
| [**Attributo msSFU-30-NIS-domain**](a-mssfu30nisdomain.md)                                | Falso     | **Gruppo**                                                                                                                          |
| [**Attributo msSFU-30-POSIX-membro**](a-mssfu30posixmember.md)                            | Falso     | **Gruppo**                                                                                                                          |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Membro non di sicurezza**](a-nonsecuritymember.md)                               | Falso     | **Gruppo**                                                                                                                          |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**NT-gruppo-membri**](a-ntgroupmembers.md)                                     | Falso     | **Gruppo**                                                                                                                          |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                         | Vero      | [**In alto**](c-top.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Categoria oggetto**](a-objectcategory.md)                                      | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classe Object**](a-objectclass.md)                                            | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**GUID oggetto**](a-objectguid.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Oggetto-SID**](a-objectsid.md)                                                | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Versione oggetto**](a-objectversion.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Operatore-conteggio**](a-operatorcount.md)                                        | Falso     | **Gruppo**                                                                                                                          |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Set di attributi parziali**](a-partialattributeset.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Possibili-inferiori**](a-possibleinferiors.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-token**](a-primarygrouptoken.md)                               | Falso     | **Gruppo**                                                                                                                          |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Query-criteri-BL**](a-querypolicybl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Report**](a-directreports.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Reps-da**](a-repsfrom.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Da Reps a**](a-repsto.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Revisione**](a-revision.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Sbarazzarsi**](a-rid.md)                                                             | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Nome account SAM**](a-samaccountname.md)                                     | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Tipo di account SAM**](a-samaccounttype.md)                                     | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**segretaria**](a-secretary.md)                                                 | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificatore di sicurezza**](a-securityidentifier.md)                              | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Mostra-in-indirizzo-libro**](a-showinaddressbook.md)                              | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**SID-cronologia**](a-sidhistory.md)                                              | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Riferimenti secondari**](a-subrefs.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Supplementare-credenziali**](a-supplementalcredentials.md)                    | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Flag di sistema**](a-systemflags.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Numero di telefono**](a-telephonenumber.md)                                    | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Con codifica di testo o indirizzo**](a-textencodedoraddress.md)                        | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Gruppi di token**](a-tokengroups.md)                                            | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-gruppi-globale e universale**](a-tokengroupsglobalanduniversal.md)     | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-accettabile**](a-tokengroupsnogcacceptable.md)             | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificato utente**](a-usercert.md)                                                  | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Password utente**](a-userpassword.md)                                          | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-certificate**](a-usersmimecertificate.md)                         | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-modificato**](a-usnchanged.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN creato**](a-usncreated.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-tra siti**](a-usnintersite.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-origine**](a-usnsource.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WBEM-percorso**](a-wbempath.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Oggetti noti**](a-wellknownobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Quando-modificato**](a-whenchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Data di creazione**](a-whencreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WWW-pagina-altro**](a-url.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                           | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-extended-rights"></a>Diritti estesi di Windows Server 2008

Questa classe contiene i seguenti diritti estesi per Windows Server 2008:



| Nome comune                  |
|------------------------------|
| [**Invia a**](r-send-to.md) |



## <a name="windows-server-2008-validated-writes"></a>Scritture convalidate per Windows Server 2008

Questa classe contiene le seguenti scritture convalidate per Windows Server 2008:



| Nome comune                                  |
|----------------------------------------------|
| [**Appartenenza automatica**](r-self-membership.md) |



## <a name="windows-server-2008-property-sets"></a>Set di proprietà di Windows Server 2008

Questa classe contiene i set di proprietà seguenti per Windows Server 2008:



| Nome comune                                      |
|--------------------------------------------------|
| [**Posta elettronica-informazioni**](r-email-information.md) |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributes (Attributi)](#windows-server-2008-r2-attributes)
-   [Diritti estesi](#windows-server-2008-r2-extended-rights)
-   [Scritture convalidate](#windows-server-2008-r2-validated-writes)
-   [Set di proprietà](#windows-server-2008-r2-property-sets)



| Voce | Valore |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Possibili superiori          | [**Dominio-**](c-domaindns.md)[**unità organizzativa**](c-organizationalunit.md)[**DNS incorporata-**](c-builtindomain.md)[**contenitore**](c-container.md)di dominio [**ms-DS-AZ-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-AZ-Application**](c-msds-azapplication.md)[**ms-DS-AZ-scope**](c-msds-azscope.md) |
| Classi ausiliarie           | [**posixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**mail-destinatario**](c-mailrecipient.md) (sistema)                                                                                                                                                                   |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                     |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60AE-405A-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-r2-attributes"></a>Attributi di Windows Server 2008 R2

Questa classe contiene gli attributi seguenti per Windows Server 2008 R2:



| Attributo                                                                        | Obbligatorio | Derivato da                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome-account-cronologia**](a-accountnamehistory.md)                             | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Amministratore-conteggio**](a-admincount.md)                                              | Falso     | **Gruppo**                                                                                                                          |
| [**Admin-Descrizione**](a-admindescription.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Attributi consentiti**](a-allowedattributes.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Alt-sicurezza-identità**](a-altsecurityidentities.md)                       | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Nome canonico**](a-canonicalname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Commento**](a-info.md)                                                        | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Nome comune**](a-cn.md)                                                      | Vero      | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario posta**](c-mailrecipient.md)<br/> |
| [**Controllo-accesso-diritti**](a-controlaccessrights.md)                           | Falso     | **Gruppo**                                                                                                                          |
| [**Creazione timestamp**](a-createtimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Descrizione**](a-description.md)                                             | Falso     | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Profilo desktop**](a-desktopprofile.md)                                      | Falso     | **Gruppo**                                                                                                                          |
| [**Nome visualizzato**](a-displayname.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DSA-firma**](a-dsasignature.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi di posta elettronica**](a-mail.md)                                               | Falso     | **Gruppo**                                                                                                                          |
| [**Nome estensione**](a-extensionname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Bandiere**](a-flags.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Da-entry**](a-fromentry.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Garbage-Coll-period**](a-garbagecollperiod.md)                               | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Attributi di gruppo**](a-groupattributes.md)                                    | Falso     | **Gruppo**                                                                                                                          |
| [**Gruppo-appartenenza-SAM**](a-groupmembershipsam.md)                             | Falso     | **Gruppo**                                                                                                                          |
| [**Tipo di gruppo**](a-grouptype.md)                                                | Vero      | **Gruppo**                                                                                                                          |
| [**Tipo di istanza**](a-instancetype.md)                                          | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Viene eliminato**](a-isdeleted.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-member-of-DL**](a-memberof.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Riciclato**](a-isrecycled.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DN-Exchange legacy**](a-legacyexchangedn.md)                                 | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Gestito da**](a-managedby.md)                                                | Falso     | **Gruppo**                                                                                                                          |
| [**Oggetti gestiti**](a-managedobjects.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Mastered-by**](a-masteredby.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Membro**](a-member.md)                                                       | Falso     | **Gruppo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                    | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule**](a-msds-azbizrule.md)                                    | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule-Language**](a-msds-azbizrulelanguage.md)                   | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-Generic-Data**](a-msds-azgenericdata.md)                            | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-Last-importated-biz-rule-path**](a-msds-azlastimportedbizrulepath.md) | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-LDAP-query**](a-msds-azldapquery.md)                                | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                              | Falso     | **Gruppo**                                                                                                                          |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Enabled-feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-host-Service-account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                        | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-ultimo-noto-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-locale-effettivo-eliminazione-ora**](a-msds-localeffectivedeletiontime.md) | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-effective-riciclo-tempo**](a-msds-localeffectiverecycletime.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-non membri**](a-msds-nonmembers.md)                                   | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-fonetica-Display-Name**](a-msds-phoneticdisplayname.md)                | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Attributo msSFU-30-nome**](a-mssfu30name.md)                                           | Falso     | **Gruppo**                                                                                                                          |
| [**Attributo msSFU-30-NIS-domain**](a-mssfu30nisdomain.md)                                | Falso     | **Gruppo**                                                                                                                          |
| [**Attributo msSFU-30-POSIX-membro**](a-mssfu30posixmember.md)                            | Falso     | **Gruppo**                                                                                                                          |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Membro non di sicurezza**](a-nonsecuritymember.md)                               | Falso     | **Gruppo**                                                                                                                          |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**NT-gruppo-membri**](a-ntgroupmembers.md)                                     | Falso     | **Gruppo**                                                                                                                          |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                         | Vero      | [**In alto**](c-top.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Categoria oggetto**](a-objectcategory.md)                                      | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classe Object**](a-objectclass.md)                                            | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**GUID oggetto**](a-objectguid.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Oggetto-SID**](a-objectsid.md)                                                | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Versione oggetto**](a-objectversion.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Operatore-conteggio**](a-operatorcount.md)                                        | Falso     | **Gruppo**                                                                                                                          |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Set di attributi parziali**](a-partialattributeset.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Possibili-inferiori**](a-possibleinferiors.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-token**](a-primarygrouptoken.md)                               | Falso     | **Gruppo**                                                                                                                          |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Query-criteri-BL**](a-querypolicybl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Report**](a-directreports.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Reps-da**](a-repsfrom.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Da Reps a**](a-repsto.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Revisione**](a-revision.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Sbarazzarsi**](a-rid.md)                                                             | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Nome account SAM**](a-samaccountname.md)                                     | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Tipo di account SAM**](a-samaccounttype.md)                                     | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**segretaria**](a-secretary.md)                                                 | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificatore di sicurezza**](a-securityidentifier.md)                              | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Mostra-in-indirizzo-libro**](a-showinaddressbook.md)                              | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**SID-cronologia**](a-sidhistory.md)                                              | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Riferimenti secondari**](a-subrefs.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Supplementare-credenziali**](a-supplementalcredentials.md)                    | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Flag di sistema**](a-systemflags.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Numero di telefono**](a-telephonenumber.md)                                    | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Con codifica di testo o indirizzo**](a-textencodedoraddress.md)                        | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Gruppi di token**](a-tokengroups.md)                                            | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-gruppi-globale e universale**](a-tokengroupsglobalanduniversal.md)     | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-accettabile**](a-tokengroupsnogcacceptable.md)             | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificato utente**](a-usercert.md)                                                  | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Password utente**](a-userpassword.md)                                          | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-certificate**](a-usersmimecertificate.md)                         | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-modificato**](a-usnchanged.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN creato**](a-usncreated.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-tra siti**](a-usnintersite.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-origine**](a-usnsource.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WBEM-percorso**](a-wbempath.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Oggetti noti**](a-wellknownobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Quando-modificato**](a-whenchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Data di creazione**](a-whencreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WWW-pagina-altro**](a-url.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                           | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-r2-extended-rights"></a>Diritti estesi di Windows Server 2008 R2

Questa classe contiene i seguenti diritti estesi per Windows Server 2008 R2:



| Nome comune                  |
|------------------------------|
| [**Invia a**](r-send-to.md) |



## <a name="windows-server-2008-r2-validated-writes"></a>Scritture convalidate di Windows Server 2008 R2

Questa classe contiene le seguenti scritture convalidate per Windows Server 2008 R2:



| Nome comune                                  |
|----------------------------------------------|
| [**Appartenenza automatica**](r-self-membership.md) |



## <a name="windows-server-2008-r2-property-sets"></a>Set di proprietà di Windows Server 2008 R2

Questa classe contiene i set di proprietà seguenti per Windows Server 2008 R2:



| Nome comune                                      |
|--------------------------------------------------|
| [**Posta elettronica-informazioni**](r-email-information.md) |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributes (Attributi)](#windows-server-2012-attributes)
-   [Diritti estesi](#windows-server-2012-extended-rights)
-   [Scritture convalidate](#windows-server-2012-validated-writes)
-   [Set di proprietà](#windows-server-2012-property-sets)



| Voce | Valore |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-Category     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valore predefinito-nascondiglio        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-att-ID                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Possibili superiori          | [**Dominio-**](c-domaindns.md)[**unità organizzativa**](c-organizationalunit.md)[**DNS incorporata-**](c-builtindomain.md)[**contenitore**](c-container.md)di dominio [**ms-DS-AZ-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-AZ-Application**](c-msds-azapplication.md)[**ms-DS-AZ-scope**](c-msds-azscope.md) |
| Classi ausiliarie           | [**posixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**mail-destinatario**](c-mailrecipient.md) (sistema)                                                                                                                                                                   |
| NT-Security-descrittore      | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                     |
| Descrittore di sicurezza predefinito | D: (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A;; RPLCLORC;;; AU) (A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A;; RPLCLORC;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60AE-405A-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2012-attributes"></a>Attributi di Windows Server 2012

Questa classe contiene gli attributi seguenti per Windows Server 2012:



| Attributo                                                                                    | Obbligatorio | Derivato da                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome-account-cronologia**](a-accountnamehistory.md)                                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Amministratore-conteggio**](a-admincount.md)                                                          | Falso     | **Gruppo**                                                                                                                          |
| [**Admin-Descrizione**](a-admindescription.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Attributi consentiti**](a-allowedattributes.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Consentito-attributi-valido**](a-allowedattributeseffective.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Consentito-classi figlio-valide**](a-allowedchildclasseseffective.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Alt-sicurezza-identità**](a-altsecurityidentities.md)                                   | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Testa di ponte-server-list-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Nome canonico**](a-canonicalname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Commento**](a-info.md)                                                                    | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Nome comune**](a-cn.md)                                                                  | Vero      | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario posta**](c-mailrecipient.md)<br/> |
| [**Controllo-accesso-diritti**](a-controlaccessrights.md)                                       | Falso     | **Gruppo**                                                                                                                          |
| [**Creazione timestamp**](a-createtimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Descrizione**](a-description.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Profilo desktop**](a-desktopprofile.md)                                                  | Falso     | **Gruppo**                                                                                                                          |
| [**Nome visualizzato**](a-displayname.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-stampabile**](a-displaynameprintable.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DSA-firma**](a-dsasignature.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagazione-dati**](a-dscorepropagationdata.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi di posta elettronica**](a-mail.md)                                                           | Falso     | **Gruppo**                                                                                                                          |
| [**Nome estensione**](a-extensionname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Bandiere**](a-flags.md)                                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Da-entry**](a-fromentry.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FRS-computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FRS-member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Garbage-Coll-period**](a-garbagecollperiod.md)                                           | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                             | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Attributi di gruppo**](a-groupattributes.md)                                                | Falso     | **Gruppo**                                                                                                                          |
| [**Gruppo-appartenenza-SAM**](a-groupmembershipsam.md)                                         | Falso     | **Gruppo**                                                                                                                          |
| [**Tipo di gruppo**](a-grouptype.md)                                                            | Vero      | **Gruppo**                                                                                                                          |
| [**Tipo di istanza**](a-instancetype.md)                                                      | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Viene eliminato**](a-isdeleted.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-member-of-DL**](a-memberof.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Riciclato**](a-isrecycled.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                                           | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DN-Exchange legacy**](a-legacyexchangedn.md)                                             | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Gestito da**](a-managedby.md)                                                            | Falso     | **Gruppo**                                                                                                                          |
| [**Oggetti gestiti**](a-managedobjects.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Mastered-by**](a-masteredby.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Membro**](a-member.md)                                                                   | Falso     | **Gruppo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                             | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modifica-timestamp**](a-modifytimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-approx-immed-subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accounting**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                                | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule**](a-msds-azbizrule.md)                                                | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule-Language**](a-msds-azbizrulelanguage.md)                               | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-Generic-Data**](a-msds-azgenericdata.md)                                        | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-Last-importated-biz-rule-path**](a-msds-azlastimportedbizrulepath.md)             | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-LDAP-query**](a-msds-azldapquery.md)                                            | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                                          | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Claim-shares-possible-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-coerenza-figlio-conteggio**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Enabled-feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-GeoCoordinate-altitudine**](a-msds-geocoordinatesaltitude.md)                       | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-GeoCoordinate-Latitudine**](a-msds-geocoordinateslatitude.md)                       | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-GeoCoordinate-Longitudine**](a-msds-geocoordinateslongitude.md)                     | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-host-Service-account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-domain-for**](a-msds-isdomainfor.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-Full-replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-partial-replica-for**](a-msds-ispartialreplicafor.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-primary-computer-for**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                                    | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-ultimo-noto-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-locale-effettivo-eliminazione-ora**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-effective-riciclo-tempo**](a-msds-localeffectiverecycletime.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Mastered-by**](a-msds-masteredby.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-REPL-cursori**](a-msds-ncreplcursors.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-REPL-inbound-neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-REPL-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-replica-locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-non membri**](a-msds-nonmembers.md)                                               | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-non membri-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-OIDToGroup-link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-fonetica-Display-Name**](a-msds-phoneticdisplayname.md)                            | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-primario-computer**](a-msds-primarycomputer.md)                                     | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-nome-entità**](a-msds-principalname.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-applicato**](a-msds-psoapplied.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-attribute-meta-data**](a-msds-replattributemetadata.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-value-meta-dati**](a-msds-replvaluemetadata.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-list-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-uscita-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-valore-tipo-riferimento-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                                      | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                             | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Attributo msSFU-30-nome**](a-mssfu30name.md)                                                       | Falso     | **Gruppo**                                                                                                                          |
| [**Attributo msSFU-30-NIS-domain**](a-mssfu30nisdomain.md)                                            | Falso     | **Gruppo**                                                                                                                          |
| [**Attributo msSFU-30-POSIX-membro**](a-mssfu30posixmember.md)                                        | Falso     | **Gruppo**                                                                                                                          |
| [**Attributo msSFU-30-POSIX-member-of**](a-mssfu30posixmemberof.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Membro non di sicurezza**](a-nonsecuritymember.md)                                           | Falso     | **Gruppo**                                                                                                                          |
| [**Non-Security-member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**NT-gruppo-membri**](a-ntgroupmembers.md)                                                 | Falso     | **Gruppo**                                                                                                                          |
| [**NT-Security-descrittore**](a-ntsecuritydescriptor.md)                                     | Vero      | [**In alto**](c-top.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Categoria oggetto**](a-objectcategory.md)                                                  | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classe Object**](a-objectclass.md)                                                        | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**GUID oggetto**](a-objectguid.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Oggetto-SID**](a-objectsid.md)                                                            | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Versione oggetto**](a-objectversion.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Operatore-conteggio**](a-operatorcount.md)                                                    | Falso     | **Gruppo**                                                                                                                          |
| [**Altri oggetti-well-known**](a-otherwellknownobjects.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Elenco di eliminazione-attributo parziale**](a-partialattributedeletionlist.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Set di attributi parziali**](a-partialattributeset.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Possibili-inferiori**](a-possibleinferiors.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-token**](a-primarygrouptoken.md)                                           | Falso     | **Gruppo**                                                                                                                          |
| [**Nome-oggetto-proxy**](a-proxiedobjectname.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Query-criteri-BL**](a-querypolicybl.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-meta-dati**](a-replpropertymetadata.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Report**](a-directreports.md)                                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Reps-da**](a-repsfrom.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Da Reps a**](a-repsto.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Revisione**](a-revision.md)                                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Sbarazzarsi**](a-rid.md)                                                                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Nome account SAM**](a-samaccountname.md)                                                 | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Tipo di account SAM**](a-samaccounttype.md)                                                 | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-diritti-efficacia**](a-sdrightseffective.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**segretaria**](a-secretary.md)                                                             | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificatore di sicurezza**](a-securityidentifier.md)                                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-riferimento-BL**](a-serverreferencebl.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Mostra-in-indirizzo-libro**](a-showinaddressbook.md)                                          | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Mostra-in-solo visualizzazione avanzata**](a-showinadvancedviewonly.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**SID-cronologia**](a-sidhistory.md)                                                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classe strutturale-oggetto**](a-structuralobjectclass.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Riferimenti secondari**](a-subrefs.md)                                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Supplementare-credenziali**](a-supplementalcredentials.md)                                | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Flag di sistema**](a-systemflags.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Numero di telefono**](a-telephonenumber.md)                                                | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Con codifica di testo o indirizzo**](a-textencodedoraddress.md)                                    | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Gruppi di token**](a-tokengroups.md)                                                        | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-gruppi-globale e universale**](a-tokengroupsglobalanduniversal.md)                 | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-accettabile**](a-tokengroupsnogcacceptable.md)                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                               | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificato utente**](a-usercert.md)                                                              | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**Password utente**](a-userpassword.md)                                                      | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-certificate**](a-usersmimecertificate.md)                                     | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-modificato**](a-usnchanged.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN creato**](a-usncreated.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-rimosso**](a-usndsalastobjremoved.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-tra siti**](a-usnintersite.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-ultimo-obj-REM**](a-usnlastobjrem.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-origine**](a-usnsource.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WBEM-percorso**](a-wbempath.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Oggetti noti**](a-wellknownobjects.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Quando-modificato**](a-whenchanged.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Data di creazione**](a-whencreated.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WWW-Home-pagina**](a-wwwhomepage.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WWW-pagina-altro**](a-url.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                                       | Falso     | [**Destinatario posta**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2012-extended-rights"></a>Diritti estesi di Windows Server 2012

Questa classe contiene i seguenti diritti estesi per Windows Server 2012:



| Nome comune                  |
|------------------------------|
| [**Invia a**](r-send-to.md) |



## <a name="windows-server-2012-validated-writes"></a>Scritture convalidate per Windows Server 2012

Questa classe contiene le seguenti scritture convalidate per Windows Server 2012:



| Nome comune                                  |
|----------------------------------------------|
| [**Appartenenza automatica**](r-self-membership.md) |



## <a name="windows-server-2012-property-sets"></a>Set di proprietà di Windows Server 2012

Questa classe contiene i set di proprietà seguenti per Windows Server 2012:



| Nome comune                                      |
|--------------------------------------------------|
| [**Posta elettronica-informazioni**](r-email-information.md) |



 

 





