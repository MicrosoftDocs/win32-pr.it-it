---
title: Classe Win32_TSLicenseReport
description: Fornisce istanze di Servizi Desktop remoto licenza di accesso client per utente (RDS \ 160; Report sull'utilizzo di licenze CAL per utente) generate nel server licenze Desktop remoto e metodi per le operazioni di generazione, recupero ed eliminazione dei report delle licenze.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLicenseReport Servizi Desktop remoto
- Classe Win32_TSLicenseReport Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport
- Win32_TSLicenseReport.FileName
- Win32_TSLicenseReport.LicenseUsageCount
- Win32_TSLicenseReport.InstalledLicenses
- Win32_TSLicenseReport.GenerationDateTime
- Win32_TSLicenseReport.ScopeType
- Win32_TSLicenseReport.ScopeValue
- Win32_TSLicenseReport.Version
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de997056222c1b525253f320f6fe191f017614f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873405"
---
# <a name="win32_tslicensereport-class"></a>Win32 \_ TSLicenseReport (classe)

Fornisce istanze di Servizi Desktop remoto report sull'utilizzo della licenza di accesso client per utente (RDS per utente CAL) generati nel server licenze Desktop remoto, nonché i metodi per le operazioni di generazione, recupero ed eliminazione dei report delle licenze.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseReport
{
  string   FileName;
  uint32   LicenseUsageCount;
  uint32   InstalledLicenses;
  DATETIME GenerationDateTime;
  uint32   ScopeType;
  string   ScopeValue;
  uint32   Version;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TSLicenseReport** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSLicenseReport** presenta questi metodi.



| Metodo                                                                                                         | Descrizione                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteReport**](deletereport-win32-tslicensereport.md)                                                     | Elimina un oggetto report nel server licenze Desktop remoto. Non si tratta di un metodo statico.<br/>                                                                                           |
| [**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)                                         | Recupera le voci nell'oggetto report.<br/>                                                                                                                                              |
| [**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)               | Recupera i dettagli relativi alle licenze CAL per utente non riuscite Servizi Desktop remoto per utente dal report.<br/>                                                             |
| [**FetchReportFailedPerUserSummaryEntries**](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | Recupera le informazioni di riepilogo di Servizi Desktop remoto non riuscite per licenze CAL per utente per utente dal report.<br/>                                                 |
| [**FetchReportPerDeviceEntries**](fetchreportperdeviceentries-win32-tslicensereport.md)                       | Recupera le informazioni sulle licenze di accesso client per dispositivo di Servizi Desktop remoto emesse dal report.<br/>                                                     |
| [**FetchReportSummaryEntries**](win32-tslicensereport-fetchreportsummaryentries.md)                           | Recupera i riepiloghi delle licenze dall'oggetto report.<br/>                                                                                                                                  |
| [**GenerateReport**](generatereport-win32-tslicensereport.md)                                                 | Questo metodo non è supportato.<br/> **Windows server 2008 R2 e Windows server 2008:** Genera un report di utilizzo delle licenze per utente corrente nel server licenze Desktop remoto.<br/> |
| [**GenerateReportEx**](generatereportex-win32-tslicensereport.md)                                             | Genera un report di utilizzo delle licenze per utente corrente nel server licenze Desktop remoto.<br/>                                                                                              |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSLicenseReport** dispone di queste proprietà.

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome del report.

</dd> <dt>

**GenerationDateTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **[DateTime](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di generazione del report di licenze Desktop remoto.

</dd> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Questa proprietà non è supportata.

**Windows server 2008 R2 e Windows server 2008:** Numero di licenze CAL per utente di Servizi Desktop remoto installate.

</dd> <dt>

**LicenseUsageCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Questa proprietà non è supportata.

**Windows server 2008 R2 e Windows server 2008:** Numero di licenze CAL per utente per utente attualmente in uso.

</dd> <dt>

**ScopeType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Questa proprietà non è supportata.

**Windows server 2008 R2 e Windows server 2008:** Tipo di ambito del report di licenze Desktop remoto.

</dd> <dt>

**ScopeValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Questa proprietà non è supportata.

**Windows server 2008 R2 e Windows server 2008:** Valore dell'ambito del report di licenze Desktop remoto.

</dd> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione del report di licenze Desktop remoto.

</dd> </dl>

## <a name="remarks"></a>Commenti

I report generati tramite WMI vengono visualizzati in gestione licenze Desktop remoto. Anche i report eliminati tramite WMI vengono eliminati da gestione licenze Desktop remoto.

Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.

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

[**\_TSLicenseReportEntry Win32**](win32-tslicensereportentry.md)
</dt> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

