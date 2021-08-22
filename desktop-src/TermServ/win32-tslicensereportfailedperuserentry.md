---
title: Win32_TSLicenseReportFailedPerUserEntry classe
description: Fornisce informazioni dettagliate sull'errore Servizi Desktop remoto licenza di accesso client per utente (Servizi Desktop remoto \ 160; Licenza CAL per utente).
ms.assetid: 27d155a4-938e-4bca-8d15-03c44740e506
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportFailedPerUserEntry classe Servizi Desktop remoto
- Win32_TSLicenseReportFailedPerUserEntry classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserEntry
- Win32_TSLicenseReportFailedPerUserEntry.User
- Win32_TSLicenseReportFailedPerUserEntry.TriedIssuanceOn
- Win32_TSLicenseReportFailedPerUserEntry.CALType
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersion
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02d56c1a7e2c715f068d808d45ac6ae3295b16bb7382179ec0e32c93beee096
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119420841"
---
# <a name="win32_tslicensereportfailedperuserentry-class"></a>Classe \_ TSLicenseReportFailedPerUserEntry Win32

Fornisce informazioni dettagliate sulla licenza CAL per Servizi Desktop remoto client per utente di Servizi Desktop remoto per utente.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserEntry
{
  string   User;
  DATETIME TriedIssuanceOn;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ TSLicenseReportFailedPerUserEntry** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ TSLicenseReportFailedPerUserEntry** ha queste proprietà.

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di licenza CAL rilasciata. Questo sarà uno dei valori seguenti.

"Licenza CAL integrata di Servizi terminal per dispositivo"

"TS per dispositivo CAL"

"TS Internet Connector CAL"

"TS per utente CAL"

"TS o SERVIZI Desktop remoto per dispositivo CAL"

"Licenza CAL Per Utente di Servizi Desktop remoto o Servizi Desktop remoto"

"Licenza di sottoscrizione VDI Standard Suite per dispositivo"

"Licenza di sottoscrizione Premium Suite per dispositivo VDI"

"LICENZA CAL per dispositivo di Servizi Desktop remoto"

"LICENZA CAL per utente di Servizi Desktop remoto"

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

La versione di Servizi Desktop remoto per cui è stata rilasciata la licenza CAL Per Utente di Servizi Desktop remoto. Questo sarà uno dei valori seguenti.

<dt>

"Windows Server 2012"
</dt> <dd>

Con questa licenza sono supportati solo i server che eseguono Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008.

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

**TriedIssuanceOn**
</dt> <dd> <dl> <dt>

Tipo di dati: **DATETIME**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data in cui è stato effettuato il tentativo di rilascio della licenza.

</dd> <dt>

**Utente**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome dell'utente a cui è stata tentata l'emissione della licenza.

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

[**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)
</dt> </dl>

 

