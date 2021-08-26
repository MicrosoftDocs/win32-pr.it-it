---
title: Win32_TSLicenseReportPerDeviceEntry classe
description: Fornisce informazioni dettagliate sull'errore Servizi Desktop remoto licenza di accesso client per dispositivo (Servizi Desktop remoto \ 160; Cal per dispositivo).
ms.assetid: b26f2518-439c-4562-9492-a0cfa60c457a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportPerDeviceEntry classe Servizi Desktop remoto
- Win32_TSLicenseReportPerDeviceEntry classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportPerDeviceEntry
- Win32_TSLicenseReportPerDeviceEntry.sIssuedToComputer
- Win32_TSLicenseReportPerDeviceEntry.sHardwareId
- Win32_TSLicenseReportPerDeviceEntry.ExpirationDate
- Win32_TSLicenseReportPerDeviceEntry.CALType
- Win32_TSLicenseReportPerDeviceEntry.ProductVersion
- Win32_TSLicenseReportPerDeviceEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfbcdad271a346820b318c94bed7ce6b9b9527d3fdd7df9cc3f1dc9d9a97aae3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008421"
---
# <a name="win32_tslicensereportperdeviceentry-class"></a>Classe Win32 \_ TSLicenseReportPerDeviceEntry

Fornisce informazioni dettagliate sull'errore di Servizi Desktop remoto di accesso client per dispositivo (LICENZA CAL Per dispositivo di Servizi Desktop remoto).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportPerDeviceEntry
{
  string   sIssuedToComputer;
  string   sHardwareId;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ TSLicenseReportPerDeviceEntry** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ TSLicenseReportPerDeviceEntry** ha queste proprietà.

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di licenza CAL rilasciata. Si tratta di uno dei valori seguenti.

"Licenza CAL TS per dispositivo incorporata"

"TS Per Device CAL"

"TS Internet Connector CAL"

"TS Per User CAL"

"TS o Servizi Desktop remoto per licenza CAL per dispositivo"

"Licenza CAL Per Utente di Servizi Desktop remoto o Servizi Desktop remoto"

"Licenza di sottoscrizione di VDI Standard Suite per dispositivo"

"Licenza di sottoscrizione Premium Suite per dispositivo VDI"

"Licenza CAL Servizi Desktop remoto per dispositivo"

"Licenza CAL Servizi Desktop remoto per utente"

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DATETIME**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data di scadenza della licenza.

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

La versione di Servizi Desktop remoto per cui è stata rilasciata la licenza CAL Per Utente di Servizi Desktop remoto. Si tratta di uno dei valori seguenti.

<dt>

"Windows Server 2012"
</dt> <dd>

Solo i server che Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008 sono supportati con questa licenza.

</dd> <dt>

"Windows Server 7"
</dt> <dd>

Con questa licenza sono supportati solo i server che eseguono Windows Server 2008 R2 o Windows Server 2008.

</dd> <dt>

"Windows Server 2008"
</dt> <dd>

Solo i server che Windows Server 2008 sono supportati con questa licenza.

</dd> </dl>

</dd> <dt>

**ProductVersionID**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore della versione del prodotto per il key pack Servizi Desktop remoto licenza.

<dt>

4
</dt> <dd>

Windows Server 2012

</dd> <dt>

3
</dt> <dd>

Windows Server 2008 R2

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> <dt>

1
</dt> <dd>

Non supportata.

</dd> <dt>

0
</dt> <dd>

Non supportata.

</dd> </dl>

</dd> <dt>

**sHardwareId**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificatore hardware del computer.

</dd> <dt>

**sIssuedToComputer**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer per cui è stata tentata l'emissione della licenza.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FetchReportPerDeviceEntries**](fetchreportperdeviceentries-win32-tslicensereport.md)
</dt> </dl>

 

