---
title: Classe ms-DS-Password-Impostazioni
description: Oggetto impostazioni password per gli account.
ms.assetid: 4e3a5a80-4f55-4c26-b5af-ace9dd853836
ms.tgt_platform: multiple
keywords:
- Schema AD della classe ms-DS-Password-Impostazioni
- Schema AD della classe msDS-PasswordSettings
topic_type:
- apiref
api_name:
- ms-DS-Password-Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76459a04701bac5f7c6abad40d9cbc2222c8346c288f67a702958d85f2aa0d64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959780"
---
# <a name="ms-ds-password-settings-class"></a>Classe ms-DS-Password-Impostazioni

Oggetto impostazioni password per gli account.

> [!Note]  
> Questo oggetto classSchema viene creato con un elenco di OID systemMustContain. Si tratta di un elenco di attributi che un oggetto Impostazioni password (PSO) deve contenere oppure la creazione dell'oggetto PSO avrà esito negativo.

 



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | ms-DS-Password-Impostazioni              |
| Ldap-Display-Name | msDS-PasswordSettings                |
| Privilegio di aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Schema-Id-Guid    | 3bcd9db8-f84b-451c-952f-6c52b81f9ec6 |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributes (Attributi)](#windows-server-2008-attributes)



| Voce | Valore |
|-----------------------------|-------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                         |
| Object-Category             | 1                                                                             |
| Default-Object-Category     | \-                                                                            |
| Governs-Id                  | 1.2.840.113556.1.5.255                                                        |
| Default-Hiding-Value        | 0                                                                             |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                        |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                               |
| Possibili superiori          | [**ms-DS-Password-Impostazioni-Container**](c-msds-passwordsettingscontainer.md) |
| Classi ausiliarie           | \-                                                                            |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                  |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)    |
| System-Flags                | 0x00000010                                                                    |



## <a name="windows-server-2008-attributes"></a>Windows Attributi di Server 2008

Questa classe contiene gli attributi seguenti per Windows Server 2008:



| Attributo                                                                                          | Obbligatorio | Derivato da                    |
|----------------------------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Description**](a-admindescription.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Canonical-Name**](a-canonicalname.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Descrizione**](a-description.md)                                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome visualizzato**](a-displayname.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Extension-Name**](a-extensionname.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Bandiere**](a-flags.md)                                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Tipo di istanza**](a-instancetype.md)                                                            | Vero      | [**In alto**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Membro di DL**](a-memberof.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Titolare dei privilegi**](a-isprivilegeholder.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti gestiti**](a-managedobjects.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica timestamp**](a-modifytimestamp.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-Domain-For**](a-msds-isdomainfor.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Lockout-Duration**](a-msds-lockoutduration.md)                                           | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Lockout-Observation-Window**](a-msds-lockoutobservationwindow.md)                        | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Lockout-Threshold**](a-msds-lockoutthreshold.md)                                         | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Maximum-Password-Age**](a-msds-maximumpasswordage.md)                                    | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Minimum-Password-Age**](a-msds-minimumpasswordage.md)                                    | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Minimum-Password-Length**](a-msds-minimumpasswordlength.md)                              | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-NC-Type**](a-msds-nctype.md)                                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Password-Complexity-Enabled**](a-msds-passwordcomplexityenabled.md)                      | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Password-History-Length**](a-msds-passwordhistorylength.md)                              | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Password-Reversible-Encryption-Enabled**](a-msds-passwordreversibleencryptionenabled.md) | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Password-Impostazioni-Precedence**](a-msds-passwordsettingsprecedence.md)                    | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-PSO-Applies-To**](a-msds-psoappliesto.md)                                                | Falso     | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                           | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria di oggetti**](a-objectcategory.md)                                                        | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe object**](a-objectclass.md)                                                              | Vero      | [**In alto**](c-top.md)<br/> |
| [**Guid oggetto**](a-objectguid.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Possibili inevasi**](a-possibleinferiors.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classe structural-object**](a-structuralobjectclass.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Sottori ref**](a-subrefs.md)                                                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica di USN**](a-usnchanged.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creato da USN**](a-usncreated.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene modificato**](a-whenchanged.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene creato**](a-whencreated.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributes (Attributi)](#windows-server-2008-r2-attributes)



| Voce | Valore |
|-----------------------------|-------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                         |
| Object-Category             | 1                                                                             |
| Default-Object-Category     | \-                                                                            |
| Governs-Id                  | 1.2.840.113556.1.5.255                                                        |
| Default-Hiding-Value        | 0                                                                             |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                        |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                               |
| Possibili superiori          | [**ms-DS-Password-Impostazioni-Container**](c-msds-passwordsettingscontainer.md) |
| Classi ausiliarie           | \-                                                                            |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                  |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)    |
| System-Flags                | 0x00000010                                                                    |



## <a name="windows-server-2008-r2-attributes"></a>Windows Attributi di Server 2008 R2

Questa classe contiene gli attributi seguenti per Windows Server 2008 R2:



| Attributo                                                                                          | Obbligatorio | Derivato da                    |
|----------------------------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Admin-Description**](a-admindescription.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi consentite-figlio**](a-allowedchildclasses.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Testa di ponte-Server-List-BL**](a-bridgeheadserverlistbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Canonical-Name**](a-canonicalname.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Descrizione**](a-description.md)                                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome visualizzato**](a-displayname.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Extension-Name**](a-extensionname.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Bandiere**](a-flags.md)                                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Tipo di istanza**](a-instancetype.md)                                                            | Vero      | [**In alto**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Member-Of-DL**](a-memberof.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Titolare del privilegio Is**](a-isprivilegeholder.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Recycled**](a-isrecycled.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti gestiti**](a-managedobjects.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica timestamp**](a-modifytimestamp.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Lockout-Duration**](a-msds-lockoutduration.md)                                           | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Lockout-Observation-Window**](a-msds-lockoutobservationwindow.md)                        | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Lockout-Threshold**](a-msds-lockoutthreshold.md)                                         | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Maximum-Password-Age**](a-msds-maximumpasswordage.md)                                    | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Minimum-Password-Age**](a-msds-minimumpasswordage.md)                                    | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Minimum-Password-Length**](a-msds-minimumpasswordlength.md)                              | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-NC-Type**](a-msds-nctype.md)                                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Password-Complexity-Enabled**](a-msds-passwordcomplexityenabled.md)                      | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Password-History-Length**](a-msds-passwordhistorylength.md)                              | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Password-Reversible-Encryption-Enabled**](a-msds-passwordreversibleencryptionenabled.md) | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Password-Impostazioni-Precedence**](a-msds-passwordsettingsprecedence.md)                    | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-PSO-Applies-To**](a-msds-psoappliesto.md)                                                | Falso     | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                           | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria di oggetti**](a-objectcategory.md)                                                        | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe object**](a-objectclass.md)                                                              | Vero      | [**In alto**](c-top.md)<br/> |
| [**Guid oggetto**](a-objectguid.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Possibili inevasi**](a-possibleinferiors.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classe structural-object**](a-structuralobjectclass.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Sottori ref**](a-subrefs.md)                                                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica di USN**](a-usnchanged.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creato da USN**](a-usncreated.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Intersite**](a-usnintersite.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene modificato**](a-whenchanged.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene creato**](a-whencreated.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Home-Page**](a-wwwhomepage.md)                                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributes (Attributi)](#windows-server-2012-attributes)



| Voce | Valore |
|-----------------------------|-------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                         |
| Object-Category             | 1                                                                             |
| Default-Object-Category     | \-                                                                            |
| Governs-Id                  | 1.2.840.113556.1.5.255                                                        |
| Default-Hiding-Value        | 0                                                                             |
| Rdn-Att-Id                  | [**Nome comune**](a-cn.md)<br/>                                        |
| Sottoclasse di                 | [**In alto**](c-top.md)<br/>                                               |
| Possibili superiori          | [**ms-DS-Password-Impostazioni-Container**](c-msds-passwordsettingscontainer.md) |
| Classi ausiliarie           | \-                                                                            |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                  |
| Descrittore di sicurezza predefinito | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)    |
| System-Flags                | 0x00000010                                                                    |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attributi

Questa classe contiene gli attributi seguenti per Windows Server 2012:



| Attributo                                                                                          | Obbligatorio | Derivato da                    |
|----------------------------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Descrizione dell'amministratore**](a-admindescription.md)                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Attributi consentiti**](a-allowedattributes.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Classi figlio consentite**](a-allowedchildclasses.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Canonical-Name**](a-canonicalname.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome comune**](a-cn.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creazione timestamp**](a-createtimestamp.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Descrizione**](a-description.md)                                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Nome visualizzato**](a-displayname.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Firma DSA**](a-dsasignature.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Extension-Name**](a-extensionname.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Bandiere**](a-flags.md)                                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**From-Entry**](a-fromentry.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Tipo di istanza**](a-instancetype.md)                                                            | Vero      | [**In alto**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Is-Deleted**](a-isdeleted.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Membro di DL**](a-memberof.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Titolare dei privilegi**](a-isprivilegeholder.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Viene riciclato**](a-isrecycled.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ultimo elemento padre noto**](a-lastknownparent.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti gestiti**](a-managedobjects.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Mastered-By**](a-masteredby.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Modifica timestamp**](a-modifytimestamp.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md)       | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-Domain-For**](a-msds-isdomainfor.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-is-full-replica-for**](a-msds-isfullreplicafor.md)                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Lockout-Duration**](a-msds-lockoutduration.md)                                           | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Lockout-Observation-Window**](a-msds-lockoutobservationwindow.md)                        | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Lockout-Threshold**](a-msds-lockoutthreshold.md)                                         | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Maximum-Password-Age**](a-msds-maximumpasswordage.md)                                    | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)       | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Minimum-Password-Age**](a-msds-minimumpasswordage.md)                                    | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Minimum-Password-Length**](a-msds-minimumpasswordlength.md)                              | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-NC-Type**](a-msds-nctype.md)                                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Password-Complexity-Enabled**](a-msds-passwordcomplexityenabled.md)                      | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Password-History-Length**](a-msds-passwordhistorylength.md)                              | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Password-Reversible-Encryption-Enabled**](a-msds-passwordreversibleencryptionenabled.md) | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Password-Impostazioni-Precedence**](a-msds-passwordsettingsprecedence.md)                    | Vero      | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-PSO-Applies-To**](a-msds-psoappliesto.md)                                                | Falso     | **ms-DS-Password-Impostazioni**     |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-Revealed-DSAs**](a-msds-revealeddsas.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Non-Security-Member-BL**](a-nonsecuritymemberbl.md)                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                           | Vero      | [**In alto**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                       | Falso     | [**In alto**](c-top.md)<br/> |
| [**Categoria di oggetti**](a-objectcategory.md)                                                        | Vero      | [**In alto**](c-top.md)<br/> |
| [**Classe object**](a-objectclass.md)                                                              | Vero      | [**In alto**](c-top.md)<br/> |
| [**Guid oggetto**](a-objectguid.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Versione oggetto**](a-objectversion.md)                                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Altri oggetti noti**](a-otherwellknownobjects.md)                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**Possibili eserezioni**](a-possibleinferiors.md)                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Indirizzi proxy**](a-proxyaddresses.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Rdn**](a-name.md)                                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                          | Falso     | [**In alto**](c-top.md)<br/> |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                               | Falso     | [**In alto**](c-top.md)<br/> |
| [**Report**](a-directreports.md)                                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-From**](a-repsfrom.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Reps-To**](a-repsto.md)                                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**Revisione**](a-revision.md)                                                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                                 | Falso     | [**In alto**](c-top.md)<br/> |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                                     | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetto sito -BL**](a-siteobjectbl.md)                                                           | Falso     | [**In alto**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**Riferimenti secondari**](a-subrefs.md)                                                                      | Falso     | [**In alto**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Flag di sistema**](a-systemflags.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN modificato**](a-usnchanged.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**Creato da USN**](a-usncreated.md)                                                                | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                         | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN intersito**](a-usnintersite.md)                                                            | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                        | Falso     | [**In alto**](c-top.md)<br/> |
| [**USN-Source**](a-usnsource.md)                                                                  | Falso     | [**In alto**](c-top.md)<br/> |
| [**Wbem-Path**](a-wbempath.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/> |
| [**Oggetti noti**](a-wellknownobjects.md)                                                   | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene modificato**](a-whenchanged.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Quando viene creato**](a-whencreated.md)                                                              | Falso     | [**In alto**](c-top.md)<br/> |
| [**Www-Home-Page**](a-wwwhomepage.md)                                                             | Falso     | [**In alto**](c-top.md)<br/> |
| [**WWW-Page-Other**](a-url.md)                                                                    | Falso     | [**In alto**](c-top.md)<br/> |



 

 





