---
title: Supporto del provider di interfacce ADSI
description: La tabella seguente elenca una breve descrizione delle interfacce supportate dai provider inclusi in ADSI per Windows 2000 e il client DS.
ms.assetid: 8eb9a88c-cf18-4fe4-b256-1d6fcaf96c62
ms.tgt_platform: multiple
keywords:
- Supporto provider di ADSI Interfaces ADSI
- ADSI ADSI, provider di servizi, interfacce supportate da ogni provider
- Supporto del provider per IADsUser
- Supporto del provider per IADsComputer
- Supporto del provider per IADsComputerOperations
- Supporto del provider per IADsDomain
- Supporto del provider per IADsFileService
- Supporto del provider per IADsGroup
- Supporto del provider per IADsClass
- Supporto del provider per IADsProperty
- Supporto del provider per IADsSyntax
- Supporto del provider per IADsContainer
- Supporto del provider per IADsNamespaces
- Supporto del provider per IADsAccessControlEntry
- Supporto del provider per IADsAccessControlList
- Supporto del provider per IADsSecurityDescriptor
- Supporto del provider per IADsObjectOptions
- Supporto del provider per IADsCollection
- Supporto del provider per IADsMembers
- Supporto del provider per IADsPathname
- Supporto del provider per IADsPrintQueue
- Supporto del provider per IADsPrintQueueOperations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12803929d96a61aac6603be2c528084c91693c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328391"
---
# <a name="provider-support-of-adsi-interfaces"></a>Supporto del provider di interfacce ADSI

La tabella seguente elenca una breve descrizione delle interfacce supportate dai provider inclusi in ADSI per Windows 2000 e il client DS. Una voce contrassegnata con "Yes" indica che almeno un oggetto ADSI del provider specificato supporta l'interfaccia associata. "No" indica che nessun oggetto del provider supporta l'interfaccia in questa versione. In futuro, le interfacce attualmente non supportate possono essere supportate dai provider forniti dal sistema.

Per ulteriori informazioni sui dettagli di implementazione specifici del provider ADSI, vedere:

-   [Provider LDAP ADSI](adsi-ldap-provider.md)
-   [Provider ADSI WinNT](adsi-winnt-provider.md)
-   [ROUTER ADSI](adsi-router.md)

Per ulteriori informazioni sulla proprietà o sul metodo supportato per ogni interfaccia, fare clic sul nome dell'interfaccia appropriato nella prima colonna della tabella.



| Interface Name (Nome interfaccia)                                                 | LDAP | WinNT |
|----------------------------------------------------------------|------|-------|
| [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)                                           | Sì  | Sì   |
| [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)       | Sì  | No    |
| [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)         | Sì  | No    |
| [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl)                                     | No   | No    |
| [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink)                           | No   | No    |
| [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)               | No   | No    |
| [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)                                 | Sì  | Sì   |
| [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)                       | No   | Sì   |
| [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                           | No   | Sì   |
| [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)       | No   | Sì   |
| [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)                         | Sì  | Sì   |
| [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)                         | Sì  | No    |
| [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                               | No   | Sì   |
| [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail)                                 | No   | No    |
| [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)                         | Sì  | Sì   |
| [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)                         | No   | No    |
| [**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)                     | No   | Sì   |
| [**IADsFileServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations) | No   | Sì   |
| [**IADsFileShare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare)                         | No   | Sì   |
| [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)                                 | Sì  | Sì   |
| [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold)                                   | No   | No    |
| [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                   | Sì  | No    |
| [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality)                           | Sì  | No    |
| [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                             | Sì  | Sì   |
| [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)                       | Sì  | Sì   |
| [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)                       | No   | No    |
| [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso)                                         | Sì  | No    |
| [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)                 | Sì  | No    |
| [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)                         | No   | No    |
| [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)                   | Sì  | Sì   |
| [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou)                                       | Sì  | No    |
| [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath)                                   | No   | No    |
| [**IADsPathName**](/windows/desktop/api/Iads/nn-iads-iadspathname)                           | Sì  | Sì   |
| [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)                 | No   | No    |
| [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)                           | No   | Sì   |
| [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)       | No   | Sì   |
| [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)                       | Sì  | Sì   |
| [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)   | Sì  | Sì   |
| [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)                           | Sì  | Sì   |
| [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                 | Sì  | Sì   |
| [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)                   | Sì  | Sì   |
| [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                 | Sì  | Sì   |
| [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)               | Sì  | Sì   |
| [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)               | No   | No    |
| [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource)                           | No   | Sì   |
| [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)       | Sì  | No    |
| [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)                             | No   | Sì   |
| [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)         | No   | Sì   |
| [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession)                             | No   | Sì   |
| [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)                               | Sì  | Sì   |
| [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp)                         | No   | No    |
| [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname)                         | No   | No    |
| [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                   | Sì  | Sì   |
| [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)                   | Sì  | No    |
| [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)                   | Sì  | No    |



 

## <a name="provider-support-for-iadsuser"></a>Supporto del provider per IADsUser



| Proprietà                                                    | LDAP          | WinNT         |
|-------------------------------------------------------------|---------------|---------------|
| [**AccountDisabled**](iadsuser-property-methods.md)        | Supportato     | Supportato     |
| [**AccountExpirationDate**](iadsuser-property-methods.md)  | Supportato     | Supportato     |
| [**BadLoginAddress**](iadsuser-property-methods.md)        | Non supportato   | Non supportato |
| [**BadLoginCount**](iadsuser-property-methods.md)          | Supportato     | Supportato     |
| [**Reparto**](iadsuser-property-methods.md)             | Supportato     | Non supportato   |
| [**Descrizione**](iadsuser-property-methods.md)            | Supportato     | Supportato     |
| [**Divisione**](iadsuser-property-methods.md)               | Supportato     | Non supportato   |
| [**EmailAddress**](iadsuser-property-methods.md)           | Supportato     | Non supportato   |
| [**EmployeeID**](iadsuser-property-methods.md)             | Supportato     | Non supportato   |
| [**NumeroFax**](iadsuser-property-methods.md)              | Supportato     | Non supportato   |
| [**FirstName**](iadsuser-property-methods.md)              | Supportato     | Non supportato   |
| [**FullName**](iadsuser-property-methods.md)               | Supportato     | Supportato     |
| [**GraceLoginsAllowed**](iadsuser-property-methods.md)     | Non supportato | Non supportato   |
| [**GraceLoginsRemaining**](iadsuser-property-methods.md)   | Non supportato | Non supportato   |
| [**HomeDirectory**](iadsuser-property-methods.md)          | Supportato     | Supportato     |
| [**Home page**](iadsuser-property-methods.md)               | Supportato     | Non supportato   |
| [**IsAccountLocked**](iadsuser-property-methods.md)        | Supportato     | Supportato     |
| [**Linguaggi**](iadsuser-property-methods.md)              | Non supportato | Non supportato   |
| [**LastFailedLogin**](iadsuser-property-methods.md)        | Supportato     | Non supportato   |
| [**LastLogin**](iadsuser-property-methods.md)              | Supportato     | Supportato     |
| [**LastLogoff**](iadsuser-property-methods.md)             | Supportato     | Supportato     |
| [**LastName**](iadsuser-property-methods.md)               | Supportato     | Non supportato   |
| [**LoginHours**](iadsuser-property-methods.md)             | Supportato     | Supportato     |
| [**LoginScript**](iadsuser-property-methods.md)            | Supportato     | Supportato     |
| [**LoginWorkstations**](iadsuser-property-methods.md)      | Supportato     | Supportato     |
| [**Manager**](iadsuser-property-methods.md)                | Supportato     | Non supportato   |
| [**MaxLogins**](iadsuser-property-methods.md)              | Non supportato   | Non supportato   |
| [**MaxStorage**](iadsuser-property-methods.md)             | Supportato     | Supportato     |
| [**NamePrefix**](iadsuser-property-methods.md)             | Supportato     | Non supportato   |
| [**NameSuffix**](iadsuser-property-methods.md)             | Supportato     | Non supportato   |
| [**OfficeLocations**](iadsuser-property-methods.md)        | Supportato     | Non supportato   |
| [**UPN**](iadsuser-property-methods.md)              | Supportato     | Non supportato   |
| [**PasswordExpirationDate**](iadsuser-property-methods.md) | Non supportato   | Supportato     |
| [**PasswordLastChanged**](iadsuser-property-methods.md)    | Supportato     | Non supportato   |
| [**PasswordMinimumLength**](iadsuser-property-methods.md)  | Non supportato   | Supportato     |
| [**PasswordRequired**](iadsuser-property-methods.md)       | Supportato     | Supportato     |
| [**Immagine**](iadsuser-property-methods.md)                | Supportato     | Non supportato   |
| [**PostalAddresses**](iadsuser-property-methods.md)        | Supportato     | Non supportato   |
| [**PostalCodes**](iadsuser-property-methods.md)            | Supportato     | Non supportato   |
| [**Profilo**](iadsuser-property-methods.md)                | Supportato     | Supportato     |
| [**RequireUniquePassword**](iadsuser-property-methods.md)  | Non supportato   | Non supportato   |
| [**SeeAlso**](iadsuser-property-methods.md)                | Supportato     | Non supportato   |
| [**TelephoneHome**](iadsuser-property-methods.md)          | Supportato     | Non supportato   |
| [**TelephoneMobile**](iadsuser-property-methods.md)        | Supportato     | Non supportato   |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | Supportato     | Non supportato   |
| [**TelephonePager**](iadsuser-property-methods.md)         | Supportato     | Non supportato   |
| [**Titolo**](iadsuser-property-methods.md)                  | Supportato     | Non supportato   |



 

## <a name="provider-support-for-iadscomputer"></a>Supporto del provider per IADsComputer



| Proprietà                                     | LDAP                    | WinNT       |
|------------------------------------------------|-------------------------|-------------|
| [**Con informatizzazione**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Interfaccia non supportata | Non supportato |
| [**Reparto**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Interfaccia non supportata | Non supportato |
| [**Descrizione**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | Interfaccia non supportata | Non supportato |
| [**Divisione**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | Interfaccia non supportata | Supportato   |
| [**Location**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | Interfaccia non supportata | Non supportato |
| [**MemorySize**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Interfaccia non supportata | Non supportato |
| [**Modello**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | Interfaccia non supportata | Non supportato |
| [**NetAddresses**](/windows/desktop/api/Iads/nn-iads-iadscomputer)           | Interfaccia non supportata | Non supportato |
| [**OperatingSystem**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | Interfaccia non supportata | Supportato   |
| [**OperatingSystemVersion**](/windows/desktop/api/Iads/nn-iads-iadscomputer) | Interfaccia non supportata | Supportato   |
| [**Proprietario**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | Interfaccia non supportata | Supportato   |
| [**PrimaryUser**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | Interfaccia non supportata | Non supportato |
| [**Processore**](/windows/desktop/api/Iads/nn-iads-iadscomputer)              | Interfaccia non supportata | Supportato   |
| [**ProcessorCount**](/windows/desktop/api/Iads/nn-iads-iadscomputer)         | Interfaccia non supportata | Supportato   |
| [**Role**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | Interfaccia non supportata | Non supportato |
| [**Sito**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | Interfaccia non supportata | Non supportato |
| [**StorageCapacity**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | Interfaccia non supportata | Non supportato |



 

## <a name="provider-support-for-iadscomputeroperations"></a>Supporto del provider per IADsComputerOperations



| Proprietà                                   | LDAP                    | WinNT           |
|--------------------------------------------|-------------------------|-----------------|
| [**Arresto**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) | Interfaccia non supportata | Non implementato |
| [**Stato**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)   | Interfaccia non supportata | Non implementato |



 

## <a name="provider-support-for-iadsdomain"></a>Supporto del provider per IADsDomain



| Proprietà                                         | LDAP                    | WinNT           |
|--------------------------------------------------|-------------------------|-----------------|
| [**Gruppo di lavoro**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                | Interfaccia non supportata | Non implementato |
| [**MinPasswordLength**](/windows/desktop/api/Iads/nn-iads-iadsdomain)          | Interfaccia non supportata | Supportato       |
| [**MinPasswordAge**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | Interfaccia non supportata | Supportato       |
| [**MaxpasswordAge**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | Interfaccia non supportata | Supportato       |
| [**MaxBadPasswordsAllowed**](/windows/desktop/api/Iads/nn-iads-iadsdomain)     | Interfaccia non supportata | Supportato       |
| [**PasswordHistoryLength**](/windows/desktop/api/Iads/nn-iads-iadsdomain)      | Interfaccia non supportata | Supportato       |
| [**PasswordAttributes**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | Interfaccia non supportata | Non supportato     |
| [**AutoUnlockInterval**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | Interfaccia non supportata | Supportato       |
| [**LockoutObservationInterval**](/windows/desktop/api/Iads/nn-iads-iadsdomain) | Interfaccia non supportata | Supportato       |



 

## <a name="provider-support-for-iadsfileservice"></a>Supporto del provider per IADsFileService



| Proprietà                                | LDAP                    | WinNT     |
|-----------------------------------------|-------------------------|-----------|
| [**Descrizione**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)  | Interfaccia non supportata | Supportato |
| [**MaxUserCount**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) | Interfaccia non supportata | Supportato |



 

## <a name="provider-support-for-iadsgroup"></a>Supporto del provider per IADsGroup



| Proprietà                         | LDAP      | WinNT     |
|----------------------------------|-----------|-----------|
| [**Descrizione**](/windows/desktop/api/Iads/nn-iads-iadsgroup) | Supportato | Supportato |



 

## <a name="provider-support-for-iadsclass"></a>Supporto del provider per IADsClass



| Proprietà                                   | LDAP               | WinNT           |
|--------------------------------------------|--------------------|-----------------|
| [**PrimaryInterface**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | Supportato          | Supportato       |
| [**CLSID**](/windows/desktop/api/Iads/nn-iads-iadsclass)                 | Supportato          | Supportato       |
| [**OID**](/windows/desktop/api/Iads/nn-iads-iadsclass)                   | Supportato          | Supportato       |
| [**Contenuto**](/windows/desktop/api/Iads/nn-iads-iadsclass)              | Supportato          | Supportato       |
| [**Ausiliario**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | Supportato          | Supportato       |
| [**MandatoryProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)   | Supportato          | Supportato       |
| [**OptionalProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)    | Supportato          | Supportato       |
| [**NamingProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | Supportato          | Non implementato |
| [**Estratta da**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | Supportato          | Non supportato     |
| [**AuxDerivedFrom**](/windows/desktop/api/Iads/nn-iads-iadsclass)        | Supportato          | Non supportato     |
| [**PossibleSuperiors**](/windows/desktop/api/Iads/nn-iads-iadsclass)     | Supportato          | Supportato       |
| [**Contenimento**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | Supportato per la lettura | Supportato       |
| [**Contenitore**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | Supportato per la lettura | Supportato       |
| [**HelpFileName**](/windows/desktop/api/Iads/nn-iads-iadsclass)          | Supportato          | Supportato       |
| [**HelpFileContext**](/windows/desktop/api/Iads/nn-iads-iadsclass)       | Supportato          | Supportato       |
| Metodo                                     | LDAP               | WinNT           |
| [**Qualificatori**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers) | Non implementato    | Non implementato |



 

## <a name="provider-support-for-iadsproperty"></a>Supporto del provider per IADsProperty



| Proprietà                            | LDAP      | WinNT     |
|-------------------------------------|-----------|-----------|
| [**OID**](/windows/desktop/api/Iads/nn-iads-iadsproperty)         | Supportato | Supportato |
| [**Sintassi**](/windows/desktop/api/Iads/nn-iads-iadsproperty)      | Supportato | Supportato |
| [**MaxRange**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | Supportato | Supportato |
| [**MinRange**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | Supportato | Supportato |
| [**Multivalore**](/windows/desktop/api/Iads/nn-iads-iadsproperty) | Supportato | Supportato |



 

## <a name="provider-support-for-iadssyntax"></a>Supporto del provider per IADsSyntax



| Proprietà                              | LDAP      | WinNT     |
|---------------------------------------|-----------|-----------|
| [**OleAutoDataType**](/windows/desktop/api/Iads/nn-iads-iadssyntax) | Supportato | Supportato |



 

## <a name="provider-support-for-iadscontainer"></a>Supporto del provider per IADsContainer



| Proprietà                        | LDAP            | WinNT           |
|---------------------------------|-----------------|-----------------|
| [**Conteggio**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | Non implementato | Non implementato |
| [**Hint**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | Supportato       | Non implementato |
| [**Filtra**](/windows/desktop/api/Iads/nn-iads-iadscontainer) | Supportato       | Supportato       |



 

## <a name="provider-support-for-iadsnamespaces"></a>Supporto del provider per IADsNamespaces



| Proprietà                                   | LDAP      | WinNT     |
|--------------------------------------------|-----------|-----------|
| [**defaultContainer**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) | Supportato | Supportato |



 

## <a name="provider-support-for-iadsaccesscontrolentry"></a>Supporto del provider per IADsAccessControlEntry



| Proprietà                                              | LDAP      | WinNT       |
|-------------------------------------------------------|-----------|-------------|
| [**AccessMask**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Supportato | Non supportato |
| [**AccessType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Supportato | Non supportato |
| [**AccessFlags**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)         | Supportato | Non supportato |
| [**Bandiere**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)               | Supportato | Non supportato |
| [**ObjectType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Supportato | Non supportato |
| [**InheritedObjectType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) | Supportato | Non supportato |
| [**Fiduciario**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)             | Supportato | Non supportato |



 

## <a name="provider-support-for-iadsaccesscontrollist"></a>Supporto del provider per IADsAccessControlList



| Proprietà                                                       | LDAP      | WinNT       |
|----------------------------------------------------------------|-----------|-------------|
| [**AceCount**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                      | Supportato | Non supportato |
| [**AceRevision**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                   | Supportato | Non supportato |
| Metodo                                                         | LDAP      | WinNT       |
| [**AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace)                 | Supportato | Non supportato |
| [**CopyAccessList**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-copyaccesslist) | Supportato | Non supportato |
| [**RemoveAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-removeace)           | Supportato | Non supportato |
| [**ottenere \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-get__newenum)   | Supportato | Non supportato |



 

## <a name="provider-support-for-iadssecuritydescriptor"></a>Supporto del provider per IADsSecurityDescriptor



| Proprietà                                                                        | LDAP      | WinNT       |
|---------------------------------------------------------------------------------|-----------|-------------|
| [**Control**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                       | Supportato | Non supportato |
| [**DaclDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | Supportato | Non supportato |
| [**DiscretionaryAcl**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                              | Supportato | Non supportato |
| [**Group**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | Supportato | Non supportato |
| [**GroupDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | Supportato | Non supportato |
| [**Proprietario**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | Supportato | Non supportato |
| [**OwnerDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | Supportato | Non supportato |
| [**SaclDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | Supportato | Non supportato |
| [**SystemAcl**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                     | Supportato | Non supportato |
| Metodo                                                                          | LDAP      | WinNT       |
| [**CopySecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecuritydescriptor-copysecuritydescriptor) | Supportato | Non supportato |



 

## <a name="provider-support-for-iadsobjectoptions"></a>Supporto del provider per IADsObjectOptions



| Metodo                                           | LDAP      | WinNT                   |
|--------------------------------------------------|-----------|-------------------------|
| [**GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) | Supportato | Interfaccia non supportata |
| [**SetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) | Supportato | Interfaccia non supportata |



 

## <a name="provider-support-for-iadscollection"></a>Supporto del provider per IADsCollection



| Metodo                                                | LDAP                    | WinNT       |
|-------------------------------------------------------|-------------------------|-------------|
| [**Aggiungere**](/windows/desktop/api/Iads/nf-iads-iadscollection-add)                     | Interfaccia non supportata | Non supportato |
| [**ottenere \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscollection-get__newenum) | Interfaccia non supportata | Supportato   |
| [**GetObject**](/windows/desktop/api/Iads/nf-iads-iadscollection-getobject)         | Interfaccia non supportata | Supportato   |
| [**Rimuovi**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove)               | Interfaccia non supportata | Supportato   |



 

## <a name="provider-support-for-iadsmembers"></a>Supporto del provider per IADsMembers



| Proprietà                                           | LDAP                                                      | WinNT       |
|----------------------------------------------------|-----------------------------------------------------------|-------------|
| [**Conteggio**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                       | Supportato per GroupCollection, ma non per UserCollection | Non supportato |
| [**Filtra**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                      | Supportato                                                 | Supportato   |
| Metodo                                             | LDAP                                                      | WinNT       |
| [**ottenere \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum) | Supportato                                                 | Supportato   |



 

## <a name="provider-support-for-iadspathname"></a>Supporto del provider per IADsPathname



| Proprietà                                                    | LDAP      | WinNT       |
|-------------------------------------------------------------|-----------|-------------|
| [**EscapedMode**](/windows/desktop/api/Iads/nn-iads-iadspathname)                         | Supportato | Supportato   |
| Metodo                                                      | LDAP      | WinNT       |
| [**Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)                             | Supportato | Supportato   |
| [**SetDisplayType**](/windows/desktop/api/Iads/nf-iads-iadspathname-setdisplaytype)       | Supportato | Supportato   |
| [**Recupero**](/windows/desktop/api/Iads/nf-iads-iadspathname-retrieve)                   | Supportato | Supportato   |
| [**GetNumElements**](/windows/desktop/api/Iads/nf-iads-iadspathname-getnumelements)       | Supportato | Supportato   |
| [**GetElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-getelement)               | Supportato | Supportato   |
| [**GetEscapedElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-getescapedelement) | Supportato | Non supportato |
| [**RemoveLeafElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-removeleafelement) | Supportato | Supportato   |
| [**CopyPath**](/windows/desktop/api/Iads/nf-iads-iadspathname-copypath)                   | Supportato | Supportato   |



 

## <a name="provider-support-for-iadsprintqueue"></a>Supporto del provider per IADsPrintQueue



| Proprietà                                     | LDAP        | WinNT       |
|----------------------------------------------|-------------|-------------|
| [**PrinterPath**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | Supportato   | Non supportato |
| [**Modello**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)              | Supportato   | Supportata.  |
| [**Tipo**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Non supportato | Supportato   |
| [**PrintProcessor**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)     | Non supportato | Supportato   |
| [**Descrizione**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | Supportato   | Supportato   |
| [**Location**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Supportato   | Supportato   |
| [**StartTime**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | Supportato   | Supportato   |
| [**UntilTime**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | Supportato   | Supportato   |
| [**DefaultJobPriority**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) | Non supportato | Supportato   |
| [**Priority**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Supportato   | Supportato   |
| [**BannerPage**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)         | Supportato   | Supportato   |
| [**PrintDevices**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | Supportato   | Supportato   |
| [**NetAddresses**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | Non supportato | Non supportato |



 

## <a name="provider-support-for-iadsprintqueueoperations"></a>Supporto del provider per IADsPrintQueueOperations



| Proprietà                                                | LDAP      | WinNT      |
|---------------------------------------------------------|-----------|------------|
| [**Stato**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)              | Supportato | Supportato  |
| Metodo                                                  | LDAP      | WinNT      |
| [**Sospendere**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-pause)         | Supportato | Supportata. |
| [**PrintJobs**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-printjobs) | Supportato | Supportato  |
| [**Ripulisci**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-purge)         | Supportato | Supportato  |
| [**Riprendi**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-resume)       | Supportato | Supportato  |



 

 

 




