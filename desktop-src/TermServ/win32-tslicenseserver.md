---
title: Win32_TSLicenseServer classe
description: Fornisce metodi e proprietà per visualizzare e configurare Desktop remoto Licenze Desktop remoto in un Desktop remoto licenze.
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseServer classe Servizi Desktop remoto
- Win32_TSLicenseServer classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer
- Win32_TSLicenseServer.FirstName
- Win32_TSLicenseServer.LastName
- Win32_TSLicenseServer.Company
- Win32_TSLicenseServer.CountryRegion
- Win32_TSLicenseServer.eMail
- Win32_TSLicenseServer.OrgUnit
- Win32_TSLicenseServer.Address
- Win32_TSLicenseServer.City
- Win32_TSLicenseServer.State
- Win32_TSLicenseServer.PostalCode
- Win32_TSLicenseServer.ServerRole
- Win32_TSLicenseServer.DatabasePath
- Win32_TSLicenseServer.ProductId
- Win32_TSLicenseServer.Version
- Win32_TSLicenseServer.VersionNumber
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7c73c1d1a48bbc76b4988afca8a07fd9ce505d0633c74f67306901259d9f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126511"
---
# <a name="win32_tslicenseserver-class"></a>Classe \_ TSLicenseServer Win32

Fornisce metodi e proprietà per visualizzare e configurare Desktop remoto Licenze Desktop remoto in un Desktop remoto licenze.

## <a name="syntax"></a>Sintassi

``` syntax
[singleton, dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseServer
{
  string FirstName;
  string LastName;
  string Company;
  string CountryRegion;
  string eMail;
  string OrgUnit;
  string Address;
  string City;
  string State;
  string PostalCode;
  uint32 ServerRole;
  string DatabasePath;
  string ProductId;
  string Version;
  string VersionNumber;
};
```

## <a name="members"></a>Members

La **classe \_ Win32 TSLicenseServer** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe Win32 \_ TSLicenseServer** include questi metodi.



| Metodo                                                                                   | Descrizione                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateServer**](activateserver-win32-tslicenseserver.md)                           | Attiva il server Desktop remoto licenze usando un ID Desktop remoto server licenze ottenuto tramite telefono o Internet.<br/>                                                                                           |
| [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md)         | Attiva automaticamente Desktop remoto server licenze tramite Internet. Le **proprietà FirstName**, **LastName**, **Company** e **CountryRegion** non devono essere vuote quando viene chiamato questo metodo oppure il metodo avrà esito negativo.<br/> |
| [**AddLStoTSLSGroup**](addlstotslsgroup-win32-tslicenseserver.md)                       | Aggiunge il Desktop remoto server licenze al gruppo Desktop remoto server licenze in un controller di dominio nello stesso dominio del server licenze.<br/>                                                                                |
| [**ChangeRole**](changerole-win32-tslicenseserver.md)                                   | Modifica l'ambito di individuazione del Desktop remoto licenze.<br/>                                                                                                                                                                  |
| [**CreateTSCGroup**](createtscgroup-win32-tslicenseserver.md)                           | Questo metodo non è supportato.<br/> **Windows Server 2008 R2 e Windows Server 2008:** Crea il gruppo locale Computer Terminal Server nel server Desktop remoto licenze.<br/>                                               |
| [**DeactivateServer**](deactivateserver-win32-tslicenseserver.md)                       | Disattiva il Desktop remoto licenze usando un codice di conferma ricevuto al telefono.<br/>                                                                                                                        |
| [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md)     | Disattiva il server Desktop remoto licenze tramite Internet. Le **proprietà FirstName** **e LastName** non devono essere vuote quando viene chiamato questo metodo oppure il metodo avrà esito negativo.<br/>                                              |
| [**GetActivationStatus**](getactivationstatus-win32-tslicenseserver.md)                 | Recupera lo stato di attivazione corrente.<br/>                                                                                                                                                                                           |
| [**GetLicenseServerId**](getlicenseserverid-win32-tslicenseserver.md)                   | Recupera un ID Desktop remoto server licenze se il server è attualmente attivato.<br/>                                                                                                                                                 |
| [**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)                         | Recupera un valore che indica se Desktop remoto server licenze è membro del gruppo Desktop remoto server licenze in un controller di dominio in un determinato dominio.<br/>                                                                              |
| [**IsLSonDC**](islsondc-win32-tslicenseserver.md)                                       | Recupera se Licenze Desktop remoto è installato in un controller di dominio.<br/>                                                                                                                                                                |
| [**IsLSPreventUpgradeGPEnabled**](islspreventupgradegpenabled-win32-tslicenseserver.md) | Recupera se l'impostazione dei criteri di gruppo "Impedisci aggiornamento licenze" è abilitata nel server Desktop remoto licenze.<br/>                                                                                                              |
| [**IsLSPublished**](islspublished-win32-tslicenseserver.md)                             | Recupera un valore che indica se Desktop remoto server licenze viene pubblicato in Active Directory Domain Services (Ad DS).<br/>                                                                                                                      |
| [**IsLSRegisteredToSCP**](win32-tslicenseserver-islsregisteredtoscp.md)                 | Recupera un valore che indica se Desktop remoto server licenze è registrato come punto di connessione del servizio Active Directory Domain Services.<br/>                                                                                               |
| [**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)                 | Recupera se l'impostazione dei criteri di gruppo "Gruppo di sicurezza del server licenze" è abilitata nel server Desktop remoto licenze.<br/>                                                                                                        |
| [**IsSecureAccessAllowed**](issecureaccessallowed-win32-tslicenseserver.md)             | Recupera un valore che indica se a un server Host sessione Desktop remoto è consentito richiedere Servizi Desktop remoto licenze CAL (Client Access License) dal server licenze Desktop remoto servizi Desktop remoto.<br/>                                                                |
| [**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)                     | Questo metodo non è supportato.<br/> **Windows Server 2008 R2 e Windows Server 2008:** Recupera se il gruppo locale Terminal Server Computers esiste nel server Desktop remoto licenze.<br/>                              |
| [**IsTSinTSCGroup**](istsintscgroup-win32-tslicenseserver.md)                           | Recupera un valore che indica se un server Host sessione Desktop remoto è membro del gruppo locale Terminal Server Computers Desktop remoto licenze.<br/>                                                                                         |
| [**PublishLS**](publishls-win32-tslicenseserver.md)                                     | Pubblica il server Desktop remoto licenze in Servizi di dominio Active Directory.<br/>                                                                                                                                                                              |
| [**Riattiva server**](reactivateserver-win32-tslicenseserver.md)                       | Riattiva il Desktop remoto licenze usando un nuovo ID Desktop remoto server licenze ottenuto tramite telefono o Internet.<br/>                                                                                     |
| [**Riattivazioneserverautomatica**](reactivateserverautomatic-win32-tslicenseserver.md)     | Riattiva il server Desktop remoto licenze tramite Internet. Le **proprietà FirstName** **e LastName** non devono essere vuote quando viene chiamato questo metodo oppure il metodo avrà esito negativo.<br/>                                              |
| [**RegisterLSToSCP**](win32-tslicenseserver-registerlstoscp.md)                         | Registra il server licenze Desktop remoto come punto di connessione del servizio in Active Directory Domain Services.<br/>                                                                                                                     |
| [**RemoveLSfromTSLSGroup**](removelsfromtslsgroup-win32-tslicenseserver.md)             | Rimuove il Desktop remoto server licenze dal gruppo Desktop remoto server licenze in un controller di dominio nello stesso dominio del server licenze.<br/>                                                                           |
| [**RemoveTSCGroup**](removetscgroup-win32-tslicenseserver.md)                           | Questo metodo non è supportato.<br/> **Windows Server 2008 R2 e Windows Server 2008:** Rimuove il gruppo locale Computer Terminal Server dal server Desktop remoto licenze.<br/>                                             |
| [**Annulla pubblicazioneLS**](unpublishls-win32-tslicenseserver.md)                                 | Annulla la pubblicazione di Desktop remoto server licenze da Servizi di dominio Active Directory.<br/>                                                                                                                                                                            |
| [**UnRegisterLSFromSCP**](win32-tslicenseserver-unregisterlsfromscp.md)                 | Rimuove il Desktop remoto server licenze come punto di connessione del servizio in Active Directory Domain Services.<br/>                                                                                                                       |



 

### <a name="properties"></a>Proprietà

La **classe Win32 \_ TSLicenseServer** ha queste proprietà.

<dl> <dt>

**Indirizzo**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Via del contatto per Licenze Desktop remoto. Questa proprietà viene usata quando viene chiamato il metodo [**ActivateServerAutomatic.**](activateserverautomatic-win32-tslicenseserver.md) Questa proprietà è facoltativa quando si usa il **metodo ActivateServerAutomatic.**

</dd> <dt>

**Città**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Città del contatto per Licenze Desktop remoto. Questa proprietà viene usata quando viene chiamato il metodo [**ActivateServerAutomatic.**](activateserverautomatic-win32-tslicenseserver.md) Questa proprietà è facoltativa quando si usa il **metodo ActivateServerAutomatic.**

</dd> <dt>

**Company**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Società del contatto per Licenze Desktop remoto. Questa proprietà viene usata (e obbligatoria) quando viene chiamato il [**metodo ActivateServerAutomatic.**](activateserverautomatic-win32-tslicenseserver.md)

</dd> <dt>

**CountryRegion**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Paese/area geografica del contatto per Licenze Desktop remoto. Questa proprietà viene usata (e obbligatoria) quando viene chiamato il [**metodo ActivateServerAutomatic.**](activateserverautomatic-win32-tslicenseserver.md)

</dd> <dt>

**Databasepath**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso del database delle licenze Servizi Desktop remoto.

</dd> <dt>

**Posta elettronica**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indirizzo di posta elettronica del contatto per Servizio licenze Desktop remoto. Questa proprietà viene usata quando vengono chiamati i [**metodi ActivateServerAutomatic,**](activateserverautomatic-win32-tslicenseserver.md) [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic.**](deactivateserverautomatic-win32-tslicenseserver.md) Questa proprietà è facoltativa per queste chiamate al metodo.

</dd> <dt>

**FirstName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Nome del contatto per Servizio licenze Desktop remoto. Questa proprietà viene usata (e obbligatoria) quando vengono chiamati i metodi [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic.**](deactivateserverautomatic-win32-tslicenseserver.md)

</dd> <dt>

**LastName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Cognome del contatto per Le licenze Desktop remoto. Questa proprietà viene usata (e obbligatoria) quando vengono chiamati i metodi [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic.**](deactivateserverautomatic-win32-tslicenseserver.md)

</dd> <dt>

**OrgUnit**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Unità organizzativa del contatto per Licenze Desktop remoto. Questa proprietà viene usata quando [**viene chiamato ActivateServerAutomatic.**](activateserverautomatic-win32-tslicenseserver.md) Questa proprietà è facoltativa quando si usa il **metodo ActivateServerAutomatic.**

</dd> <dt>

**PostalCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Codice postale del contatto per Le licenze Desktop remoto. Questa proprietà viene usata quando viene chiamato il metodo [**ActivateServerAutomatic.**](activateserverautomatic-win32-tslicenseserver.md) Questa proprietà è facoltativa quando si usa il **metodo ActivateServerAutomatic.**

</dd> <dt>

**ProductId**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID prodotto del server Desktop remoto licenze.

</dd> <dt>

**Serverrole**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive l'ambito di gestione delle licenze per Desktop remoto server licenze all'interno dell'organizzazione.

<dt>

0
</dt> <dd>

I server Host sessione Desktop remoto nello stesso gruppo di lavoro possono individuare il server licenze.

</dd> <dt>

1
</dt> <dd>

I server Host sessione Desktop remoto nello stesso dominio possono individuare il server licenze.

</dd> <dt>

2
</dt> <dd>

I server Host sessione Desktop remoto da più domini nella stessa foresta possono individuare il server licenze.

</dd> </dl>

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Stato del contatto per Le licenze Desktop remoto. Questa proprietà viene usata quando viene chiamato il metodo [**ActivateServerAutomatic.**](activateserverautomatic-win32-tslicenseserver.md) Questa proprietà è facoltativa quando si usa il **metodo ActivateServerAutomatic.**

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione del server Desktop remoto licenze.

</dd> <dt>

**Versionnumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di versione del server Desktop remoto licenze.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa classe è una [classe singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) e può avere una sola istanza. Tutti i metodi contenuti in questa classe sono statici.

Per utilizzare questa classe, è necessario essere un membro del gruppo Administrators. Se il chiamante non è membro del gruppo Administrators, le proprietà restituite saranno vuote.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> </dl>

 

