---
title: Classe Win32_TSLicenseServer
description: Fornisce metodi e proprietà per visualizzare e Desktop remoto configurare licenze Desktop remoto in un server licenze Desktop remoto.
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLicenseServer Servizi Desktop remoto
- Classe Win32_TSLicenseServer Servizi Desktop remoto, descritta
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
ms.openlocfilehash: 31951b943723e620414b2f714327db8c786f9ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964498"
---
# <a name="win32_tslicenseserver-class"></a>Win32 \_ TSLicenseServer (classe)

Fornisce metodi e proprietà per visualizzare e Desktop remoto configurare licenze Desktop remoto in un server licenze Desktop remoto.

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

La classe **Win32 \_ TSLicenseServer** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSLicenseServer** presenta questi metodi.



| Metodo                                                                                   | Descrizione                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateServer**](activateserver-win32-tslicenseserver.md)                           | Attiva il server licenze Desktop remoto usando un ID del server licenze Desktop remoto ottenuto sul telefono o su Internet.<br/>                                                                                           |
| [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md)         | Attiva automaticamente il server licenze Desktop remoto tramite Internet. Le proprietà **FirstName**, **LastName**, **Company** e **CountryRegion** non devono essere vuote quando viene chiamato questo metodo oppure il metodo avrà esito negativo.<br/> |
| [**AddLStoTSLSGroup**](addlstotslsgroup-win32-tslicenseserver.md)                       | Aggiunge il server licenze Desktop remoto al gruppo server licenze Desktop remoto in un controller di dominio nello stesso dominio del server licenze.<br/>                                                                                |
| [**ChangeRole**](changerole-win32-tslicenseserver.md)                                   | Modifica l'ambito di individuazione del server licenze Desktop remoto.<br/>                                                                                                                                                                  |
| [**CreateTSCGroup**](createtscgroup-win32-tslicenseserver.md)                           | Questo metodo non è supportato.<br/> **Windows server 2008 R2 e Windows server 2008:** Consente di creare il gruppo locale computer Terminal Server nel server licenze Desktop remoto.<br/>                                               |
| [**DeactivateServer**](deactivateserver-win32-tslicenseserver.md)                       | Disattiva il server licenze Desktop remoto utilizzando un codice di conferma ricevuto tramite telefono.<br/>                                                                                                                        |
| [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md)     | Disattiva il server licenze Desktop remoto tramite Internet. Le proprietà **FirstName** e **LastName** non devono essere vuote quando viene chiamato questo metodo, altrimenti il metodo avrà esito negativo.<br/>                                              |
| [**GetActivationStatus**](getactivationstatus-win32-tslicenseserver.md)                 | Recupera lo stato di attivazione corrente.<br/>                                                                                                                                                                                           |
| [**GetLicenseServerId**](getlicenseserverid-win32-tslicenseserver.md)                   | Recupera un ID del server licenze Desktop remoto se il server è attualmente attivato.<br/>                                                                                                                                                 |
| [**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)                         | Recupera un valore che indica se il server licenze Desktop remoto è un membro del gruppo server licenze Desktop remoto in un controller di dominio in un determinato dominio.<br/>                                                                              |
| [**IsLSonDC**](islsondc-win32-tslicenseserver.md)                                       | Recupera un valore che indica se le licenze Desktop remoto sono installate in un controller di dominio.<br/>                                                                                                                                                                |
| [**IsLSPreventUpgradeGPEnabled**](islspreventupgradegpenabled-win32-tslicenseserver.md) | Recupera un valore che indica se l'impostazione di criteri di gruppo "Impedisci aggiornamento licenza" è abilitata nel server licenze Desktop remoto.<br/>                                                                                                              |
| [**IsLSPublished**](islspublished-win32-tslicenseserver.md)                             | Recupera un valore che indica se il server licenze Desktop remoto è pubblicato in Active Directory Domain Services (AD DS).<br/>                                                                                                                      |
| [**IsLSRegisteredToSCP**](win32-tslicenseserver-islsregisteredtoscp.md)                 | Recupera un valore che indica se il server licenze Desktop remoto viene registrato come punto di connessione del servizio nel Active Directory Domain Services.<br/>                                                                                               |
| [**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)                 | Recupera un valore che indica se l'impostazione di criteri di gruppo "gruppo di sicurezza del server licenze" è abilitata nel server licenze Desktop remoto.<br/>                                                                                                        |
| [**IsSecureAccessAllowed**](issecureaccessallowed-win32-tslicenseserver.md)             | Recupera un valore che indica se un server Host sessione Desktop remoto è autorizzato a richiedere Servizi Desktop remoto licenze CAL (Client Access License) del server licenze di Desktop remoto.<br/>                                                                |
| [**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)                     | Questo metodo non è supportato.<br/> **Windows server 2008 R2 e Windows server 2008:** Recupera un valore che indica se il gruppo locale computer Terminal Server esiste nel server licenze Desktop remoto.<br/>                              |
| [**IsTSinTSCGroup**](istsintscgroup-win32-tslicenseserver.md)                           | Recupera un valore che indica se un server Host sessione Desktop remoto è un membro del gruppo locale computer Terminal Server nel server licenze Desktop remoto.<br/>                                                                                         |
| [**PublishLS**](publishls-win32-tslicenseserver.md)                                     | Pubblica il server licenze Desktop remoto in servizi di dominio Active Directory.<br/>                                                                                                                                                                              |
| [**ReactivateServer**](reactivateserver-win32-tslicenseserver.md)                       | Riattiva il server licenze Desktop remoto utilizzando un nuovo ID server licenze Desktop remoto ottenuto tramite telefono o Internet.<br/>                                                                                     |
| [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)     | Riattiva il server licenze Desktop remoto tramite Internet. Le proprietà **FirstName** e **LastName** non devono essere vuote quando viene chiamato questo metodo, altrimenti il metodo avrà esito negativo.<br/>                                              |
| [**RegisterLSToSCP**](win32-tslicenseserver-registerlstoscp.md)                         | Registra il server licenze Desktop remoto come punto di connessione del servizio in Active Directory Domain Services.<br/>                                                                                                                     |
| [**RemoveLSfromTSLSGroup**](removelsfromtslsgroup-win32-tslicenseserver.md)             | Rimuove il server licenze Desktop remoto dal gruppo server licenze Desktop remoto in un controller di dominio nello stesso dominio del server licenze.<br/>                                                                           |
| [**RemoveTSCGroup**](removetscgroup-win32-tslicenseserver.md)                           | Questo metodo non è supportato.<br/> **Windows server 2008 R2 e Windows server 2008:** Rimuove il gruppo locale computer Terminal Server dal server licenze Desktop remoto.<br/>                                             |
| [**UnpublishLS**](unpublishls-win32-tslicenseserver.md)                                 | Annulla la pubblicazione di un server licenze Desktop remoto da servizi di dominio Active Directory.<br/>                                                                                                                                                                            |
| [**UnRegisterLSFromSCP**](win32-tslicenseserver-unregisterlsfromscp.md)                 | Rimuove il server licenze Desktop remoto come punto di connessione del servizio in Active Directory Domain Services.<br/>                                                                                                                       |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSLicenseServer** dispone di queste proprietà.

<dl> <dt>

**Indirizzo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Via indirizzo del contatto per licenze Desktop remoto. Questa proprietà viene utilizzata quando viene chiamato il metodo [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) . Questa proprietà è facoltativa quando si usa il metodo **ActivateServerAutomatic** .

</dd> <dt>

**Città**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Città del contatto per licenze Desktop remoto. Questa proprietà viene utilizzata quando viene chiamato il metodo [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) . Questa proprietà è facoltativa quando si usa il metodo **ActivateServerAutomatic** .

</dd> <dt>

**Company**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Società del contatto per licenze Desktop remoto. Questa proprietà viene utilizzata (e obbligatoria) quando viene chiamato il metodo [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .

</dd> <dt>

**CountryRegion**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Paese/area geografica del contatto per licenze Desktop remoto. Questa proprietà viene utilizzata (e obbligatoria) quando viene chiamato il metodo [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .

</dd> <dt>

**DatabasePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso del database di gestione licenze Servizi Desktop remoto.

</dd> <dt>

**Posta elettronica**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indirizzo di posta elettronica del contatto per licenze Desktop remoto. Questa proprietà viene utilizzata quando vengono chiamati i metodi [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) . Questa proprietà è facoltativa per le chiamate al metodo.

</dd> <dt>

**FirstName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Nome del contatto per licenze Desktop remoto. Questa proprietà viene utilizzata (e obbligatoria) quando vengono chiamati i metodi [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) .

</dd> <dt>

**LastName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Cognome del contatto per le licenze Desktop remoto. Questa proprietà viene utilizzata (e obbligatoria) quando vengono chiamati i metodi [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) .

</dd> <dt>

**OrgUnit**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Unità organizzativa del contatto per licenze Desktop remoto. Questa proprietà viene utilizzata quando viene chiamato [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) . Questa proprietà è facoltativa quando si usa il metodo **ActivateServerAutomatic** .

</dd> <dt>

**PostalCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Cap del contatto per licenze Desktop remoto. Questa proprietà viene utilizzata quando viene chiamato il metodo [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) . Questa proprietà è facoltativa quando si usa il metodo **ActivateServerAutomatic** .

</dd> <dt>

**ProductId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID prodotto del server licenze Desktop remoto.

</dd> <dt>

**ServerRole**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive l'ambito di gestione licenze per il server licenze Desktop remoto all'interno dell'organizzazione.

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

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Stato del contatto per licenze Desktop remoto. Questa proprietà viene utilizzata quando viene chiamato il metodo [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) . Questa proprietà è facoltativa quando si usa il metodo **ActivateServerAutomatic** .

</dd> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione del server licenze Desktop remoto.

</dd> <dt>

**VersionNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di versione del server licenze Desktop remoto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa classe è una classe [singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) e può avere una sola istanza. Tutti i metodi contenuti in questa classe sono statici.

Per utilizzare questa classe, è necessario essere membri del gruppo Administrators. Se il chiamante non è un membro del gruppo Administrators, le proprietà restituite saranno vuote.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSIssuedLicense Win32**](win32-tsissuedlicense.md)
</dt> <dt>

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> <dt>

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_TSLicenseReportEntry Win32**](win32-tslicensereportentry.md)
</dt> </dl>

 

