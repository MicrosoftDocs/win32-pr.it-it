---
title: Classe Win32_TSLicenseReportFailedPerUserEntry
description: Fornisce informazioni dettagliate sulla licenza di accesso client Servizi Desktop remoto per utente non riuscita (RDS \ 160; CAL per utente).
ms.assetid: 27d155a4-938e-4bca-8d15-03c44740e506
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLicenseReportFailedPerUserEntry Servizi Desktop remoto
- Classe Win32_TSLicenseReportFailedPerUserEntry Servizi Desktop remoto, descritta
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
ms.openlocfilehash: 18098ce0510a39f6083edcf688a18c10a3e20278
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400270"
---
# <a name="win32_tslicensereportfailedperuserentry-class"></a>Win32 \_ TSLicenseReportFailedPerUserEntry (classe)

Fornisce informazioni dettagliate sulla licenza CAL per utente Servizi Desktop remoto per utente non riuscita.

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

La classe **Win32 \_ TSLicenseReportFailedPerUserEntry** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSLicenseReportFailedPerUserEntry** dispone di queste proprietà.

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di licenza CAL rilasciata. Si tratta di uno dei valori seguenti.

"Licenze CAL per dispositivo predefinite"

"Licenze CAL per dispositivo"

"CAL Internet Connector CAL"

"Licenza CAL per utente di servizi Terminal"

Licenza CAL per dispositivo di Servizi terminal o RDS

Licenza CAL per utente di Servizi terminal o RDS

"Licenza abbonamento VDI Standard Suite per dispositivo"

"Licenza di sottoscrizione di VDI Premium Suite per dispositivo"

"RDS per dispositivo CAL"

"CAL per utente per utente"

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione di Servizi Desktop remoto per cui è stata rilasciata la licenza CAL per utente. Si tratta di uno dei valori seguenti.

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

Con questa licenza sono supportati solo i server che eseguono Windows Server 2008.

</dd> </dl>

</dd> <dt>

**ProductVersionID**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore della versione del prodotto per il Key Pack di Servizi Desktop remoto License.

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

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data in cui è stato effettuato il tentativo di rilascio della licenza.

</dd> <dt>

**Utente**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome dell'utente a cui è stato effettuato il tentativo di rilascio della licenza.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)
</dt> </dl>

 

