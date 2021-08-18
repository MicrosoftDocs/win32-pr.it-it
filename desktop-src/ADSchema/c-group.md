---
title: Group (classe)
description: Archivia un elenco di nomi utente. Usato per applicare le entità di sicurezza alle risorse.
ms.assetid: e8ce5c43-d0fb-4c67-a6ef-7094fb7e7669
ms.tgt_platform: multiple
keywords:
- Schema AD della classe group
- Classe group SCHEMA DI AD
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae33b53eff8305fee4698c5aed2bb072f3fa5b90a5922d0099e40e90f9b3fe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021909"
---
# <a name="group-class"></a>Group (classe)

Archivia un elenco di nomi utente. Usato per applicare le entità di sicurezza alle risorse.



| Voce | Valore |
|-------------------|------------------------------------------------|
| CN                | Group                                          |
| Ldap-Display-Name | group                                          |
| Privilegio di aggiornamento  | Questo valore viene impostato dall'amministratore di dominio. |
| Frequenza di aggiornamento  | \-                                             |
| Schema-Id-Guid    | bf967a9c-0de6-11d0-a285-00aa003049e2           |



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
-   [Diritti estesi](#windows-2000-server-extended-rights)
-   [Scritture convalidate](#windows-2000-server-validated-writes)
-   [Set di proprietà](#windows-2000-server-property-sets)



| Voce | Valore |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                                                                                               |
| Object-Category             | 1                                                                                                                                                                                                   |
| Default-Object-Category     | \-                                                                                                                                                                                                  |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                |
| Default-Hiding-Value        | 0                                                                                                                                                                                                   |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                              |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                     |
| Possibili superiori          | [**Contenitore domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain**](c-builtindomain.md)[](c-container.md)                                       |
| Classi ausiliarie           | [**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                        |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                        |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; Au) |
| System-Flags                | 0x00000010                                                                                                                                                                                          |



## <a name="windows-2000-server-attributes"></a>Windows 2000 Server Attributes

Questa classe contiene gli attributi seguenti per Windows 2000 Server:



| Attributo                                                                    | Obbligatorio | Derivato da                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Admin-Count**](a-admincount.md)                                          | Falso     | **Gruppo**                                                                                    |
| [**Admin-Description**](a-admindescription.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Attributi consentiti**](a-allowedattributes.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                   | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Canonical-Name**](a-canonicalname.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Commento**](a-info.md)                                                    | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Nome comune**](a-cn.md)                                                  | Vero      | [**In alto**](c-top.md)<br/> [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>         |
| [**Control-Access-Rights**](a-controlaccessrights.md)                       | Falso     | **Gruppo**                                                                                    |
| [**Creazione timestamp**](a-createtimestamp.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Descrizione**](a-description.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Profilo desktop**](a-desktopprofile.md)                                  | Falso     | **Gruppo**                                                                                    |
| [**Nome visualizzato**](a-displayname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Display-Name-Printable**](a-displaynameprintable.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Firma DSA**](a-dsasignature.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Indirizzi di posta elettronica**](a-mail.md)                                           | Falso     | **Gruppo**                                                                                    |
| [**Extension-Name**](a-extensionname.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Bandiere**](a-flags.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**From-Entry**](a-fromentry.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Garbage-Coll-Period**](a-garbagecollperiod.md)                           | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Attributi di gruppo**](a-groupattributes.md)                                | Falso     | **Gruppo**                                                                                    |
| [**Appartenenza a gruppi-SAM**](a-groupmembershipsam.md)                         | Falso     | **Gruppo**                                                                                    |
| [**Tipo di gruppo**](a-grouptype.md)                                            | Vero      | **Gruppo**                                                                                    |
| [**Tipo di istanza**](a-instancetype.md)                                      | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-Deleted**](a-isdeleted.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Membro di DL**](a-memberof.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Titolare del privilegio**](a-isprivilegeholder.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Gestito da**](a-managedby.md)                                            | Falso     | **Gruppo**                                                                                    |
| [**Oggetti gestiti**](a-managedobjects.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Mastered-By**](a-masteredby.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Membro**](a-member.md)                                                   | Falso     | **Gruppo**                                                                                    |
| [**Modifica timestamp**](a-modifytimestamp.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Membro non di sicurezza**](a-nonsecuritymember.md)                           | Falso     | **Gruppo**                                                                                    |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Nt-Group-Members**](a-ntgroupmembers.md)                                 | Falso     | **Gruppo**                                                                                    |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | Vero      | [**In alto**](c-top.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Categoria di oggetti**](a-objectcategory.md)                                  | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Classe object**](a-objectclass.md)                                        | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Guid oggetto**](a-objectguid.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Sid oggetto**](a-objectsid.md)                                            | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Versione oggetto**](a-objectversion.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Operator-Count**](a-operatorcount.md)                                    | Falso     | **Gruppo**                                                                                    |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Possibili eserezioni**](a-possibleinferiors.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                           | Falso     | **Gruppo**                                                                                    |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Rdn**](a-name.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Report**](a-directreports.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Reps-From**](a-repsfrom.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Reps-To**](a-repsto.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Revisione**](a-revision.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**liberarsi**](a-rid.md)                                                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**SAM-Account-Name**](a-samaccountname.md)                                 | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Sam-Account-Type**](a-samaccounttype.md)                                 | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Security-Identifier**](a-securityidentifier.md)                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                          | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SID-History**](a-sidhistory.md)                                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Sottori ref**](a-subrefs.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Credenziali supplementari**](a-supplementalcredentials.md)                | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Flag di sistema**](a-systemflags.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Numero di telefono**](a-telephonenumber.md)                                | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                    | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Gruppi di token**](a-tokengroups.md)                                        | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-Global-And-Universal**](a-tokengroupsglobalanduniversal.md) | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Certificato utente**](a-usercert.md)                                              | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                     | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Modifica di USN**](a-usnchanged.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Creato da USN**](a-usncreated.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-Intersite**](a-usnintersite.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-Source**](a-usnsource.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Wbem-Path**](a-wbempath.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Oggetti noti**](a-wellknownobjects.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Quando viene modificato**](a-whenchanged.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Quando viene creato**](a-whencreated.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Www-Home-Page**](a-wwwhomepage.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WWW-Page-Other**](a-url.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Certificato X509**](a-usercertificate.md)                                       | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-2000-server-extended-rights"></a>Windows 2000 Server Extended Rights

Questa classe contiene i diritti estesi seguenti per Windows 2000 Server:



| Nome comune                  |
|------------------------------|
| [**Invia a**](r-send-to.md) |



## <a name="windows-2000-server-validated-writes"></a>Windows 2000 Server Validated Writes

Questa classe contiene le scritture convalidate seguenti per Windows 2000 Server:



| Nome comune                                  |
|----------------------------------------------|
| [**Appartenenza self-service**](r-self-membership.md) |



## <a name="windows-2000-server-property-sets"></a>Windows set di proprietà del server 2000

Questa classe contiene i seguenti set di proprietà per Windows 2000 Server:



| Nome comune                                      |
|--------------------------------------------------|
| [**Email-Information**](r-email-information.md) |



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
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Possibili superiori          | [**Domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Classi ausiliarie           | [**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                                                     |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-attributes"></a>Windows Attributi di Server 2003

Questa classe contiene gli attributi seguenti per Windows Server 2003:



| Attributo                                                                    | Obbligatorio | Derivato da                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Admin-Count**](a-admincount.md)                                          | Falso     | **Gruppo**                                                                                    |
| [**Admin-Description**](a-admindescription.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Attributi consentiti**](a-allowedattributes.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                   | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Canonical-Name**](a-canonicalname.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Commento**](a-info.md)                                                    | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Nome comune**](a-cn.md)                                                  | Vero      | [**In alto**](c-top.md)<br/> [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>         |
| [**Control-Access-Rights**](a-controlaccessrights.md)                       | Falso     | **Gruppo**                                                                                    |
| [**Create-Time-Stamp**](a-createtimestamp.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Descrizione**](a-description.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Profilo desktop**](a-desktopprofile.md)                                  | Falso     | **Gruppo**                                                                                    |
| [**Nome visualizzato**](a-displayname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Display-Name-Printable**](a-displaynameprintable.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Firma DSA**](a-dsasignature.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Indirizzi di posta elettronica**](a-mail.md)                                           | Falso     | **Gruppo**                                                                                    |
| [**Extension-Name**](a-extensionname.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Bandiere**](a-flags.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**From-Entry**](a-fromentry.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Garbage-Coll-Period**](a-garbagecollperiod.md)                           | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Attributi di gruppo**](a-groupattributes.md)                                | Falso     | **Gruppo**                                                                                    |
| [**Appartenenza a gruppi-SAM**](a-groupmembershipsam.md)                         | Falso     | **Gruppo**                                                                                    |
| [**Tipo di gruppo**](a-grouptype.md)                                            | Vero      | **Gruppo**                                                                                    |
| [**Tipo di istanza**](a-instancetype.md)                                      | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-Deleted**](a-isdeleted.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Membro di DL**](a-memberof.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Titolare dei privilegi**](a-isprivilegeholder.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**labeledURI**](a-labeleduri.md)                                           | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Gestito da**](a-managedby.md)                                            | Falso     | **Gruppo**                                                                                    |
| [**Oggetti gestiti**](a-managedobjects.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Mastered-By**](a-masteredby.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Membro**](a-member.md)                                                   | Falso     | **Gruppo**                                                                                    |
| [**Modifica timestamp**](a-modifytimestamp.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                            | Falso     | **Gruppo**                                                                                    |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                    | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                               | Falso     | **Gruppo**                                                                                    |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                      | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Membro non di sicurezza**](a-nonsecuritymember.md)                           | Falso     | **Gruppo**                                                                                    |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Nt-Group-Members**](a-ntgroupmembers.md)                                 | Falso     | **Gruppo**                                                                                    |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | Vero      | [**In alto**](c-top.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Categoria di oggetti**](a-objectcategory.md)                                  | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Classe object**](a-objectclass.md)                                        | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Guid oggetto**](a-objectguid.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Sid oggetto**](a-objectsid.md)                                            | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Versione oggetto**](a-objectversion.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Operator-Count**](a-operatorcount.md)                                    | Falso     | **Gruppo**                                                                                    |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Possibili eserezioni**](a-possibleinferiors.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                           | Falso     | **Gruppo**                                                                                    |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Rdn**](a-name.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Report**](a-directreports.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Reps-From**](a-repsfrom.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Reps-To**](a-repsto.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Revisione**](a-revision.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**liberarsi**](a-rid.md)                                                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**SAM-Account-Name**](a-samaccountname.md)                                 | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**SAM-Account-Type**](a-samaccounttype.md)                                 | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**segretaria**](a-secretary.md)                                             | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Identificatore di sicurezza**](a-securityidentifier.md)                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                          | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SID-History**](a-sidhistory.md)                                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Classe structural-object**](a-structuralobjectclass.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Sottori ref**](a-subrefs.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Credenziali supplementari**](a-supplementalcredentials.md)                | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Flag di sistema**](a-systemflags.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Numero di telefono**](a-telephonenumber.md)                                | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                    | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Gruppi di token**](a-tokengroups.md)                                        | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-Global-And-Universal**](a-tokengroupsglobalanduniversal.md) | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Certificato utente**](a-usercert.md)                                              | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                     | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                         |
| [**Modifica di USN**](a-usnchanged.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Creato da USN**](a-usncreated.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-Intersite**](a-usnintersite.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-Source**](a-usnsource.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Wbem-Path**](a-wbempath.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Oggetti noti**](a-wellknownobjects.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Quando viene modificato**](a-whenchanged.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Quando viene creato**](a-whencreated.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Www-Home-Page**](a-wwwhomepage.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WWW-Page-Other**](a-url.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Certificato X509**](a-usercertificate.md)                                       | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-server-2003-extended-rights"></a>Windows Diritti estesi di Server 2003

Questa classe contiene i diritti estesi seguenti per Windows Server 2003:



| Nome comune                  |
|------------------------------|
| [**Invia a**](r-send-to.md) |



## <a name="windows-server-2003-validated-writes"></a>Windows Scritture convalidate di Server 2003

Questa classe contiene le scritture convalidate seguenti per Windows Server 2003:



| Nome comune                                  |
|----------------------------------------------|
| [**Appartenenza self-service**](r-self-membership.md) |



## <a name="windows-server-2003-property-sets"></a>Windows Set di proprietà di Server 2003

Questa classe contiene i seguenti set di proprietà per Windows Server 2003:



| Nome comune                                      |
|--------------------------------------------------|
| [**Informazioni di posta elettronica**](r-email-information.md) |



## <a name="adam"></a>Adam

-   [Attributes (Attributi)](#adam-attributes)
-   [Scritture convalidate](#adam-validated-writes)
-   [Set di proprietà](#adam-property-sets)



| Voce | Valore |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                                                |
| Object-Category             | 1                                                                                                                    |
| Default-Object-Category     | \-                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                 |
| Default-Hiding-Value        | 0                                                                                                                    |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                               |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                      |
| Possibili superiori          | [**Contenitore domain-DNS**](c-domaindns.md)[**organizational-unit**](c-organizationalunit.md)[](c-container.md) |
| Classi ausiliarie           | [**Entità di sicurezza**](c-securityprincipal.md) (sistema)                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                         |
| Descrittore di sicurezza predefinito | D:S:                                                                                                                 |
| System-Flags                | 0x00000010                                                                                                           |



## <a name="adam-attributes"></a>Attributi ADAM

Questa classe contiene gli attributi seguenti per ADAM:



| Attributo                                                                   | Obbligatorio | Derivato da                                                                                 |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Attributi consentiti**](a-allowedattributes.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Nome comune**](a-cn.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Creazione timestamp**](a-createtimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Descrizione**](a-description.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Profilo desktop**](a-desktopprofile.md)                                 | Falso     | **Gruppo**                                                                                    |
| [**Nome visualizzato**](a-displayname.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**From-Entry**](a-fromentry.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Tipo di gruppo**](a-grouptype.md)                                           | Vero      | **Gruppo**                                                                                    |
| [**Tipo di istanza**](a-instancetype.md)                                     | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Is-Deleted**](a-isdeleted.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Membro di DL**](a-memberof.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Gestito da**](a-managedby.md)                                           | Falso     | **Gruppo**                                                                                    |
| [**Oggetti gestiti**](a-managedobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Membro**](a-member.md)                                                  | Falso     | **Gruppo**                                                                                    |
| [**Modifica timestamp**](a-modifytimestamp.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Disable-For-Instances-BL**](a-msds-disableforinstancesbl.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**ms-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Vero      | [**In alto**](c-top.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Categoria di oggetti**](a-objectcategory.md)                                 | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Classe object**](a-objectclass.md)                                       | Vero      | [**In alto**](c-top.md)<br/>                                                              |
| [**Object-Guid**](a-objectguid.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Object-Sid**](a-objectsid.md)                                           | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Versione oggetto**](a-objectversion.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Possibili inevasi**](a-possibleinferiors.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                          | Falso     | **Gruppo**                                                                                    |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Rdn**](a-name.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Revisione**](a-revision.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Classe structural-object**](a-structuralobjectclass.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Sottori ref**](a-subrefs.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Credenziali supplementari**](a-supplementalcredentials.md)               | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Flag di sistema**](a-systemflags.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Gruppi di token**](a-tokengroups.md)                                       | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                 |
| [**Modifica di USN**](a-usnchanged.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Creato da USN**](a-usncreated.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Oggetti noti**](a-wellknownobjects.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Quando viene modificato**](a-whenchanged.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Quando creato**](a-whencreated.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**Www-Home-Page**](a-wwwhomepage.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                              |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                              |



## <a name="adam-validated-writes"></a>Scritture convalidate ADAM

Questa classe contiene le scritture convalidate seguenti per ADAM:



| Nome comune                                  |
|----------------------------------------------|
| [**Appartenenza autonoma**](r-self-membership.md) |



## <a name="adam-property-sets"></a>Set di proprietà ADAM

Questa classe contiene i seguenti set di proprietà per ADAM:



| Nome comune                                      |
|--------------------------------------------------|
| [**Informazioni sulla posta elettronica**](r-email-information.md) |



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
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Possibili superiori          | [**Domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Classi ausiliarie           | [**PosixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-r2-attributes"></a>Windows Attributi di Server 2003 R2

Questa classe contiene gli attributi seguenti per Windows Server 2003 R2:



| Attributo                                                                    | Obbligatorio | Derivato da                                                                                                                       |
|------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Conteggio amministratori**](a-admincount.md)                                          | Falso     | **Gruppo**                                                                                                                          |
| [**Descrizione dell'amministratore**](a-admindescription.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Attributi consentiti**](a-allowedattributes.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                   | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Canonical-Name**](a-canonicalname.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Commento**](a-info.md)                                                    | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Nome comune**](a-cn.md)                                                  | Vero      | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario posta elettronica**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                       | Falso     | **Gruppo**                                                                                                                          |
| [**Creazione timestamp**](a-createtimestamp.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Descrizione**](a-description.md)                                         | Falso     | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Profilo desktop**](a-desktopprofile.md)                                  | Falso     | **Gruppo**                                                                                                                          |
| [**Nome visualizzato**](a-displayname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-Printable**](a-displaynameprintable.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Firma DSA**](a-dsasignature.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi di posta elettronica**](a-mail.md)                                           | Falso     | **Gruppo**                                                                                                                          |
| [**Extension-Name**](a-extensionname.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Bandiere**](a-flags.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**From-Entry**](a-fromentry.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Garbage-Coll-Period**](a-garbagecollperiod.md)                           | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                             | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Attributi di gruppo**](a-groupattributes.md)                                | Falso     | **Gruppo**                                                                                                                          |
| [**Appartenenza a gruppi-SAM**](a-groupmembershipsam.md)                         | Falso     | **Gruppo**                                                                                                                          |
| [**Tipo di gruppo**](a-grouptype.md)                                            | Vero      | **Gruppo**                                                                                                                          |
| [**Tipo di istanza**](a-instancetype.md)                                      | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Deleted**](a-isdeleted.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Membro di DL**](a-memberof.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Titolare del privilegio**](a-isprivilegeholder.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                           | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Gestito da**](a-managedby.md)                                            | Falso     | **Gruppo**                                                                                                                          |
| [**Oggetti gestiti**](a-managedobjects.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Mastered-By**](a-masteredby.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Membro**](a-member.md)                                                   | Falso     | **Gruppo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                             | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modifica timestamp**](a-modifytimestamp.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                            | Falso     | **Gruppo**                                                                                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                    | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                               | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                      | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                       | Falso     | **Gruppo**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                            | Falso     | **Gruppo**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                        | Falso     | **Gruppo**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Membro non di sicurezza**](a-nonsecuritymember.md)                           | Falso     | **Gruppo**                                                                                                                          |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Nt-Group-Members**](a-ntgroupmembers.md)                                 | Falso     | **Gruppo**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                     | Vero      | [**In alto**](c-top.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Categoria di oggetti**](a-objectcategory.md)                                  | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classe object**](a-objectclass.md)                                        | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Guid oggetto**](a-objectguid.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Sid oggetto**](a-objectsid.md)                                            | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Versione oggetto**](a-objectversion.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Operator-Count**](a-operatorcount.md)                                    | Falso     | **Gruppo**                                                                                                                          |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Possibili eserezioni**](a-possibleinferiors.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                           | Falso     | **Gruppo**                                                                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Rdn**](a-name.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Report**](a-directreports.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Reps-From**](a-repsfrom.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Reps-To**](a-repsto.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Revisione**](a-revision.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**liberarsi**](a-rid.md)                                                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                 | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Sam-Account-Type**](a-samaccounttype.md)                                 | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**segretaria**](a-secretary.md)                                             | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Security-Identifier**](a-securityidentifier.md)                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                          | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**SID-History**](a-sidhistory.md)                                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classe structural-object**](a-structuralobjectclass.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Sottori ref**](a-subrefs.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Credenziali supplementari**](a-supplementalcredentials.md)                | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Flag di sistema**](a-systemflags.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Numero di telefono**](a-telephonenumber.md)                                | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                    | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Gruppi di token**](a-tokengroups.md)                                        | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-Global-And-Universal**](a-tokengroupsglobalanduniversal.md) | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                               | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificato utente**](a-usercert.md)                                              | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**User-Password**](a-userpassword.md)                                      | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                     | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Modifica di USN**](a-usnchanged.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Creato da USN**](a-usncreated.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-Intersite**](a-usnintersite.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-Source**](a-usnsource.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Wbem-Path**](a-wbempath.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Oggetti noti**](a-wellknownobjects.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Quando viene modificato**](a-whenchanged.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Quando viene creato**](a-whencreated.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Www-Home-Page**](a-wwwhomepage.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-Other**](a-url.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Certificato X509**](a-usercertificate.md)                                       | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2003-r2-extended-rights"></a>Windows Diritti estesi di Server 2003 R2

Questa classe contiene i diritti estesi seguenti per Windows Server 2003 R2:



| Nome comune                  |
|------------------------------|
| [**Invia a**](r-send-to.md) |



## <a name="windows-server-2003-r2-validated-writes"></a>Windows Scritture convalidate di Server 2003 R2

Questa classe contiene le scritture convalidate seguenti per Windows Server 2003 R2:



| Nome comune                                  |
|----------------------------------------------|
| [**Appartenenza self-service**](r-self-membership.md) |



## <a name="windows-server-2003-r2-property-sets"></a>Windows Set di proprietà di Server 2003 R2

Questa classe contiene i seguenti set di proprietà per Windows Server 2003 R2:



| Nome comune                                      |
|--------------------------------------------------|
| [**Informazioni di posta elettronica**](r-email-information.md) |



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
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Possibili superiori          | [**Domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Classi ausiliarie           | [**posixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-attributes"></a>Windows Attributi di Server 2008

Questa classe contiene gli attributi seguenti per Windows Server 2008:



| Attributo                                                                        | Obbligatorio | Derivato da                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                             | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Admin-Count**](a-admincount.md)                                              | Falso     | **Gruppo**                                                                                                                          |
| [**Admin-Description**](a-admindescription.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Attributi consentiti**](a-allowedattributes.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                       | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Canonical-Name**](a-canonicalname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Commento**](a-info.md)                                                        | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Nome comune**](a-cn.md)                                                      | Vero      | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                           | Falso     | **Gruppo**                                                                                                                          |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Descrizione**](a-description.md)                                             | Falso     | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Profilo desktop**](a-desktopprofile.md)                                      | Falso     | **Gruppo**                                                                                                                          |
| [**Nome visualizzato**](a-displayname.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Firma DSA**](a-dsasignature.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi di posta elettronica**](a-mail.md)                                               | Falso     | **Gruppo**                                                                                                                          |
| [**Extension-Name**](a-extensionname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Bandiere**](a-flags.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**From-Entry**](a-fromentry.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Garbage-Coll-Period**](a-garbagecollperiod.md)                               | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Attributi di gruppo**](a-groupattributes.md)                                    | Falso     | **Gruppo**                                                                                                                          |
| [**Appartenenza a gruppi-SAM**](a-groupmembershipsam.md)                             | Falso     | **Gruppo**                                                                                                                          |
| [**Tipo di gruppo**](a-grouptype.md)                                                | Vero      | **Gruppo**                                                                                                                          |
| [**Tipo di istanza**](a-instancetype.md)                                          | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-Of-DL**](a-memberof.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Titolare del privilegio Is**](a-isprivilegeholder.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Gestito da**](a-managedby.md)                                                | Falso     | **Gruppo**                                                                                                                          |
| [**Oggetti gestiti**](a-managedobjects.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Membro**](a-member.md)                                                       | Falso     | **Gruppo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modifica timestamp**](a-modifytimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Az-Application-Data**](a-msds-azapplicationdata.md)                    | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule**](a-msds-azbizrule.md)                                    | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule-Language**](a-msds-azbizrulelanguage.md)                   | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-Generic-Data**](a-msds-azgenericdata.md)                            | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-Last-Imported-Biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md) | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                                | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-Object-Guid**](a-msds-azobjectguid.md)                              | Falso     | **Gruppo**                                                                                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                        | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                                   | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                           | Falso     | **Gruppo**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                                | Falso     | **Gruppo**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                            | Falso     | **Gruppo**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Non membro della sicurezza**](a-nonsecuritymember.md)                               | Falso     | **Gruppo**                                                                                                                          |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                     | Falso     | **Gruppo**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Vero      | [**In alto**](c-top.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Categoria di oggetti**](a-objectcategory.md)                                      | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classe object**](a-objectclass.md)                                            | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Object-Guid**](a-objectguid.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Object-Sid**](a-objectsid.md)                                                | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Versione oggetto**](a-objectversion.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Operator-Count**](a-operatorcount.md)                                        | Falso     | **Gruppo**                                                                                                                          |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Possibili inevasi**](a-possibleinferiors.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                               | Falso     | **Gruppo**                                                                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Rdn**](a-name.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Report**](a-directreports.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Reps-From**](a-repsfrom.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Reps-To**](a-repsto.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Revisione**](a-revision.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**liberarsi**](a-rid.md)                                                             | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                     | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Sam-Account-Type**](a-samaccounttype.md)                                     | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**segretaria**](a-secretary.md)                                                 | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Security-Identifier**](a-securityidentifier.md)                              | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                              | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Cronologia SID**](a-sidhistory.md)                                              | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Riferimenti secondari**](a-subrefs.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Credenziali supplementari**](a-supplementalcredentials.md)                    | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Flag di sistema**](a-systemflags.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Numero di telefono**](a-telephonenumber.md)                                    | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                        | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Gruppi di token**](a-tokengroups.md)                                            | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-Global-and-Universal**](a-tokengroupsglobalanduniversal.md)     | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)             | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificato utente**](a-usercert.md)                                                  | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Password utente**](a-userpassword.md)                                          | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                         | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**USN modificato**](a-usnchanged.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Creato da USN**](a-usncreated.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN intersito**](a-usnintersite.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Oggetti noti**](a-wellknownobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Quando viene modificato**](a-whenchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Quando viene creato**](a-whencreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Www-Home-Page**](a-wwwhomepage.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Certificato X509**](a-usercertificate.md)                                           | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-extended-rights"></a>Windows Diritti estesi di Server 2008

Questa classe contiene i diritti estesi seguenti per Windows Server 2008:



| Nome comune                  |
|------------------------------|
| [**Invia a**](r-send-to.md) |



## <a name="windows-server-2008-validated-writes"></a>Windows Scritture convalidate di Server 2008

Questa classe contiene le scritture convalidate seguenti per Windows Server 2008:



| Nome comune                                  |
|----------------------------------------------|
| [**Appartenenza self-service**](r-self-membership.md) |



## <a name="windows-server-2008-property-sets"></a>Windows Set di proprietà di Server 2008

Questa classe contiene i seguenti set di proprietà per Windows Server 2008:



| Nome comune                                      |
|--------------------------------------------------|
| [**Email-Information**](r-email-information.md) |



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
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Possibili superiori          | [**Domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Classi ausiliarie           | [**posixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-r2-attributes"></a>Windows Attributi di Server 2008 R2

Questa classe contiene gli attributi seguenti per Windows Server 2008 R2:



| Attributo                                                                        | Obbligatorio | Derivato da                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                             | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Admin-Count**](a-admincount.md)                                              | Falso     | **Gruppo**                                                                                                                          |
| [**Admin-Description**](a-admindescription.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Attributi consentiti**](a-allowedattributes.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                       | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Canonical-Name**](a-canonicalname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Commento**](a-info.md)                                                        | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Nome comune**](a-cn.md)                                                      | Vero      | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                           | Falso     | **Gruppo**                                                                                                                          |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Descrizione**](a-description.md)                                             | Falso     | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Profilo desktop**](a-desktopprofile.md)                                      | Falso     | **Gruppo**                                                                                                                          |
| [**Nome visualizzato**](a-displayname.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-Printable**](a-displaynameprintable.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Firma DSA**](a-dsasignature.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi di posta elettronica**](a-mail.md)                                               | Falso     | **Gruppo**                                                                                                                          |
| [**Extension-Name**](a-extensionname.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Bandiere**](a-flags.md)                                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**From-Entry**](a-fromentry.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Garbage-Coll-Period**](a-garbagecollperiod.md)                               | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Attributi di gruppo**](a-groupattributes.md)                                    | Falso     | **Gruppo**                                                                                                                          |
| [**Appartenenza a gruppi-SAM**](a-groupmembershipsam.md)                             | Falso     | **Gruppo**                                                                                                                          |
| [**Tipo di gruppo**](a-grouptype.md)                                                | Vero      | **Gruppo**                                                                                                                          |
| [**Tipo di istanza**](a-instancetype.md)                                          | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Deleted**](a-isdeleted.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-Of-DL**](a-memberof.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Titolare del privilegio Is**](a-isprivilegeholder.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Recycled**](a-isrecycled.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Gestito da**](a-managedby.md)                                                | Falso     | **Gruppo**                                                                                                                          |
| [**Oggetti gestiti**](a-managedobjects.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Membro**](a-member.md)                                                       | Falso     | **Gruppo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modifica timestamp**](a-modifytimestamp.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Az-Application-Data**](a-msds-azapplicationdata.md)                    | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule**](a-msds-azbizrule.md)                                    | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule-Language**](a-msds-azbizrulelanguage.md)                   | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-Generic-Data**](a-msds-azgenericdata.md)                            | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-Last-Imported-Biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md) | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                                | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-Object-Guid**](a-msds-azobjectguid.md)                              | Falso     | **Gruppo**                                                                                                                          |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                        | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                                   | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                          | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                           | Falso     | **Gruppo**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                                | Falso     | **Gruppo**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                            | Falso     | **Gruppo**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Non membro della sicurezza**](a-nonsecuritymember.md)                               | Falso     | **Gruppo**                                                                                                                          |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                     | Falso     | **Gruppo**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Vero      | [**In alto**](c-top.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Categoria di oggetti**](a-objectcategory.md)                                      | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classe object**](a-objectclass.md)                                            | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Object-Guid**](a-objectguid.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Object-Sid**](a-objectsid.md)                                                | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Versione oggetto**](a-objectversion.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Operator-Count**](a-operatorcount.md)                                        | Falso     | **Gruppo**                                                                                                                          |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Possibili inevasi**](a-possibleinferiors.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                               | Falso     | **Gruppo**                                                                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Rdn**](a-name.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Report**](a-directreports.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Reps-From**](a-repsfrom.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Reps-To**](a-repsto.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Revisione**](a-revision.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**liberarsi**](a-rid.md)                                                             | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                     | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Type**](a-samaccounttype.md)                                     | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**segretaria**](a-secretary.md)                                                 | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificatore di sicurezza**](a-securityidentifier.md)                              | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                              | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**SID-History**](a-sidhistory.md)                                              | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classe structural-object**](a-structuralobjectclass.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Sottori ref**](a-subrefs.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Credenziali supplementari**](a-supplementalcredentials.md)                    | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Flag di sistema**](a-systemflags.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Numero di telefono**](a-telephonenumber.md)                                    | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                        | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Gruppi di token**](a-tokengroups.md)                                            | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-Global-And-Universal**](a-tokengroupsglobalanduniversal.md)     | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)             | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificato utente**](a-usercert.md)                                                  | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**User-Password**](a-userpassword.md)                                          | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                         | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Modifica di USN**](a-usnchanged.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Creato da USN**](a-usncreated.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-Intersite**](a-usnintersite.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Oggetti noti**](a-wellknownobjects.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Quando viene modificato**](a-whenchanged.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Quando viene creato**](a-whencreated.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Www-Home-Page**](a-wwwhomepage.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Certificato X509**](a-usercertificate.md)                                           | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-r2-extended-rights"></a>Windows Diritti estesi di Server 2008 R2

Questa classe contiene i diritti estesi seguenti per Windows Server 2008 R2:



| Nome comune                  |
|------------------------------|
| [**Invia a**](r-send-to.md) |



## <a name="windows-server-2008-r2-validated-writes"></a>Windows Scritture convalidate di Server 2008 R2

Questa classe contiene le scritture convalidate seguenti per Windows Server 2008 R2:



| Nome comune                                  |
|----------------------------------------------|
| [**Appartenenza self-service**](r-self-membership.md) |



## <a name="windows-server-2008-r2-property-sets"></a>Windows Set di proprietà di Server 2008 R2

Questa classe contiene i set di proprietà seguenti per Windows Server 2008 R2:



| Nome comune                                      |
|--------------------------------------------------|
| [**Email-Information**](r-email-information.md) |



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
| Default-Hiding-Value        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Possibili superiori          | [**Domain-DNS**](c-domaindns.md)[**Organizational-Unit**](c-organizationalunit.md)[**Builtin-Domain**](c-builtindomain.md)[**Container**](c-container.md)[**ms-DS-Az-Admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-Az-Application**](c-msds-azapplication.md)[**ms-DS-Az-Scope**](c-msds-azscope.md) |
| Classi ausiliarie           | [**posixGroup**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (System)[**Mail-Recipient**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                     |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO)(A;; RPLCLORC;;; PS)(OA;; CR;ab721a55-1e2f-11d0-9819-00aa0040529b;; AU)(OA;; RP;46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attributi

Questa classe contiene gli attributi seguenti per Windows Server 2012:



| Attributo                                                                                    | Obbligatorio | Derivato da                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Account-Name-History**](a-accountnamehistory.md)                                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Admin-Count**](a-admincount.md)                                                          | Falso     | **Gruppo**                                                                                                                          |
| [**Admin-Description**](a-admindescription.md)                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Attributi consentiti**](a-allowedattributes.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security-Identities**](a-altsecurityidentities.md)                                   | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Canonical-Name**](a-canonicalname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Commento**](a-info.md)                                                                    | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Nome comune**](a-cn.md)                                                                  | Vero      | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/> |
| [**Control-Access-Rights**](a-controlaccessrights.md)                                       | Falso     | **Gruppo**                                                                                                                          |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Descrizione**](a-description.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Profilo desktop**](a-desktopprofile.md)                                                  | Falso     | **Gruppo**                                                                                                                          |
| [**Nome visualizzato**](a-displayname.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Firma DSA**](a-dsasignature.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi di posta elettronica**](a-mail.md)                                                           | Falso     | **Gruppo**                                                                                                                          |
| [**Extension-Name**](a-extensionname.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Bandiere**](a-flags.md)                                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**From-Entry**](a-fromentry.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Garbage-Coll-Period**](a-garbagecollperiod.md)                                           | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                             | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Attributi di gruppo**](a-groupattributes.md)                                                | Falso     | **Gruppo**                                                                                                                          |
| [**Appartenenza a gruppi-SAM**](a-groupmembershipsam.md)                                         | Falso     | **Gruppo**                                                                                                                          |
| [**Tipo di gruppo**](a-grouptype.md)                                                            | Vero      | **Gruppo**                                                                                                                          |
| [**Tipo di istanza**](a-instancetype.md)                                                      | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Deleted**](a-isdeleted.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-Of-DL**](a-memberof.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Titolare del privilegio Is**](a-isprivilegeholder.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Is-Recycled**](a-isrecycled.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                                           | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                             | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Gestito da**](a-managedby.md)                                                            | Falso     | **Gruppo**                                                                                                                          |
| [**Oggetti gestiti**](a-managedobjects.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Mastered-By**](a-masteredby.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Membro**](a-member.md)                                                                   | Falso     | **Gruppo**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                             | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Modifica timestamp**](a-modifytimestamp.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Az-Application-Data**](a-msds-azapplicationdata.md)                                | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule**](a-msds-azbizrule.md)                                                | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-Biz-Rule-Language**](a-msds-azbizrulelanguage.md)                               | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-Generic-Data**](a-msds-azgenericdata.md)                                        | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-Last-Imported-Biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md)             | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-LDAP-Query**](a-msds-azldapquery.md)                                            | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Az-Object-Guid**](a-msds-azobjectguid.md)                                          | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-GeoCoordinates-Altitudine**](a-msds-geocoordinatesaltitude.md)                       | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-GeoCoordinates-Latitude**](a-msds-geocoordinateslatitude.md)                       | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-GeoCoordinates-Longitude**](a-msds-geocoordinateslongitude.md)                     | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-Domain-For**](a-msds-isdomainfor.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                                    | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Non-Members**](a-msds-nonmembers.md)                                               | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Phonetic-Display-Name**](a-msds-phoneticdisplayname.md)                            | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Primary-Computer**](a-msds-primarycomputer.md)                                     | Falso     | **Gruppo**                                                                                                                          |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-Name**](a-msexchassistantname.md)                                      | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                             | Falso     | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-Name**](a-mssfu30name.md)                                                       | Falso     | **Gruppo**                                                                                                                          |
| [**msSFU-30-Nis-Domain**](a-mssfu30nisdomain.md)                                            | Falso     | **Gruppo**                                                                                                                          |
| [**msSFU-30-Posix-Member**](a-mssfu30posixmember.md)                                        | Falso     | **Gruppo**                                                                                                                          |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Non membro della sicurezza**](a-nonsecuritymember.md)                                           | Falso     | **Gruppo**                                                                                                                          |
| [**Non security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                                 | Falso     | **Gruppo**                                                                                                                          |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Vero      | [**In alto**](c-top.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Categoria di oggetti**](a-objectcategory.md)                                                  | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Classe object**](a-objectclass.md)                                                        | Vero      | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Object-Guid**](a-objectguid.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Object-Sid**](a-objectsid.md)                                                            | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Versione oggetto**](a-objectversion.md)                                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Operator-Count**](a-operatorcount.md)                                                    | Falso     | **Gruppo**                                                                                                                          |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Possibili eserezioni**](a-possibleinferiors.md)                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                                           | Falso     | **Gruppo**                                                                                                                          |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Rdn**](a-name.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Report**](a-directreports.md)                                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Reps-From**](a-repsfrom.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Reps-To**](a-repsto.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Revisione**](a-revision.md)                                                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**liberarsi**](a-rid.md)                                                                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-Account-Name**](a-samaccountname.md)                                                 | Vero      | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Sam-Account-Type**](a-samaccounttype.md)                                                 | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**segretaria**](a-secretary.md)                                                             | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Security-Identifier**](a-securityidentifier.md)                                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Show-In-Address-Book**](a-showinaddressbook.md)                                          | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                               | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Cronologia SID**](a-sidhistory.md)                                                          | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                                     | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Riferimenti secondari**](a-subrefs.md)                                                                | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Credenziali supplementari**](a-supplementalcredentials.md)                                | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Flag di sistema**](a-systemflags.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Numero di telefono**](a-telephonenumber.md)                                                | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Text-Encoded-OR-Address**](a-textencodedoraddress.md)                                    | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Gruppi di token**](a-tokengroups.md)                                                        | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-Global-and-Universal**](a-tokengroupsglobalanduniversal.md)                 | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-No-GC-Acceptable**](a-tokengroupsnogcacceptable.md)                         | Falso     | [**Entità di sicurezza**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                               | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Certificato utente**](a-usercert.md)                                                              | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**Password utente**](a-userpassword.md)                                                      | Falso     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                                     | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |
| [**USN modificato**](a-usnchanged.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Creato da USN**](a-usncreated.md)                                                          | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN intersito**](a-usnintersite.md)                                                      | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**USN-Source**](a-usnsource.md)                                                            | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Oggetti noti**](a-wellknownobjects.md)                                             | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Quando viene modificato**](a-whenchanged.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Quando creato**](a-whencreated.md)                                                        | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Www-Home-Page**](a-wwwhomepage.md)                                                       | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page-Other**](a-url.md)                                                              | Falso     | [**In alto**](c-top.md)<br/>                                                                                                    |
| [**Certificato X509**](a-usercertificate.md)                                                       | Falso     | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012 Diritti estesi

Questa classe contiene i seguenti diritti estesi per Windows Server 2012:



| Nome comune                  |
|------------------------------|
| [**Invia a**](r-send-to.md) |



## <a name="windows-server-2012-validated-writes"></a>Windows Server 2012 Scritture convalidate

Questa classe contiene le scritture convalidate seguenti per Windows Server 2012:



| Nome comune                                  |
|----------------------------------------------|
| [**Appartenenza autonoma**](r-self-membership.md) |



## <a name="windows-server-2012-property-sets"></a>Windows Server 2012 Set di proprietà

Questa classe contiene i seguenti set di proprietà per Windows Server 2012:



| Nome comune                                      |
|--------------------------------------------------|
| [**Informazioni sulla posta elettronica**](r-email-information.md) |



 

 





