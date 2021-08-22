---
title: Win32_TSLicenseReport classe
description: Fornisce istanze di Servizi Desktop remoto di accesso client per utente (Servizi Desktop remoto \ 160; Licenza CAL per utente) report sull'utilizzo generati nel server licenze Desktop remoto e metodi per le operazioni di generazione, recupero ed eliminazione dei report delle licenze.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReport classe Servizi Desktop remoto
- Win32_TSLicenseReport classe Servizi Desktop remoto , descritto
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
ms.openlocfilehash: 93280c00cbd20993907901e1f9b8c16330863a47bddd4e08bc86d51b4b837233
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137834"
---
# <a name="win32_tslicensereport-class"></a>Classe \_ TSLicenseReport Win32

Fornisce le istanze dei report sull'utilizzo delle licenze CAL per utente di Servizi Desktop remoto per utente generati nel server licenze Desktop remoto e i metodi per la generazione, il recupero e l'eliminazione dei report delle licenze.

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

La **classe \_ Win32 TSLicenseReport** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ Win32 TSLicenseReport** include questi metodi.



| Metodo                                                                                                         | Descrizione                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteReport**](deletereport-win32-tslicensereport.md)                                                     | Elimina un oggetto report nel server Desktop remoto licenze. Non si tratta di un metodo statico.<br/>                                                                                           |
| [**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)                                         | Recupera le voci nell'oggetto report.<br/>                                                                                                                                              |
| [**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)               | Recupera dal report i dettagli Servizi Desktop remoto licenze CAL (Client Access License) per utente per utente non riuscite.<br/>                                                             |
| [**FetchReportFailedPerUserSummaryEntries**](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | Recupera dal report le informazioni di riepilogo Servizi Desktop remoto licenze CAL client per utente non riuscite .<br/>                                                 |
| [**FetchReportPerDeviceEntries**](fetchreportperdeviceentries-win32-tslicensereport.md)                       | Recupera dal report le informazioni Servizi Desktop remoto licenze CAL per dispositivo rilasciate per ogni dispositivo.<br/>                                                     |
| [**FetchReportSummaryEntries**](win32-tslicensereport-fetchreportsummaryentries.md)                           | Recupera i riepiloghi delle licenze dall'oggetto report.<br/>                                                                                                                                  |
| [**GenerateReport**](generatereport-win32-tslicensereport.md)                                                 | Questo metodo non è supportato.<br/> **Windows Server 2008 R2 e Windows Server 2008:** Genera un report corrente sull'utilizzo delle licenze per utente nel server Desktop remoto licenze.<br/> |
| [**GenerateReportEx**](generatereportex-win32-tslicensereport.md)                                             | Genera un report corrente sull'utilizzo delle licenze per utente nel server Desktop remoto licenze.<br/>                                                                                              |



 

### <a name="properties"></a>Proprietà

La **classe \_ Win32 TSLicenseReport** ha queste proprietà.

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome del report.

</dd> <dt>

**GenerationDateTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **[DATETIME](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di generazione dei report di Licenze Desktop remoto.

</dd> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **DEPRECATO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Questa proprietà non è supportata.

**Windows Server 2008 R2 e Windows Server 2008:** Numero di licenze CAL Per Utente di Servizi Desktop remoto installate.

</dd> <dt>

**LicenseUsageCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **DEPRECATO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Questa proprietà non è supportata.

**Windows Server 2008 R2 e Windows Server 2008:** Numero di licenze CAL Servizi Desktop remoto per utente attualmente in uso.

</dd> <dt>

**ScopeType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **DEPRECATO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Questa proprietà non è supportata.

**Windows Server 2008 R2 e Windows Server 2008:** Tipo di ambito del report licenze Desktop remoto.

</dd> <dt>

**Valore ambito**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **DEPRECATO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Questa proprietà non è supportata.

**Windows Server 2008 R2 e Windows Server 2008:** Valore dell'ambito del report di Licenze Desktop remoto.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione del report di Licenze Desktop remoto.

</dd> </dl>

## <a name="remarks"></a>Commenti

I report generati tramite WMI vengono visualizzati in Gestione licenze Desktop remoto. Anche i report eliminati tramite WMI vengono eliminati da Gestione licenze Desktop remoto.

Per utilizzare questa classe, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

