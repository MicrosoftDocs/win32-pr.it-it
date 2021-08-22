---
title: Win32_TSLicenseReportSummaryEntry classe
description: Fornisce un riepilogo delle licenze client di accesso client per Servizi Desktop remoto installate e rilasciate (Servizi Desktop remoto \ 160; Licenze CAL per utente).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportSummaryEntry classe Servizi Desktop remoto
- Win32_TSLicenseReportSummaryEntry classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportSummaryEntry
- Win32_TSLicenseReportSummaryEntry.ProductVersion
- Win32_TSLicenseReportSummaryEntry.ProductVersionID
- Win32_TSLicenseReportSummaryEntry.TSCALType
- Win32_TSLicenseReportSummaryEntry.InstalledLicenses
- Win32_TSLicenseReportSummaryEntry.IssuedLicenses
- Win32_TSLicenseReportSummaryEntry.TSCALAvailability
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58efc2c70019037219d8eca986fa8afd81e4dc2d06cd638ee24fc59947e3bf3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137800"
---
# <a name="win32_tslicensereportsummaryentry-class"></a>Classe Win32 \_ TSLicenseReportSummaryEntry

Fornisce un riepilogo delle licenze CAL client per Servizi Desktop remoto per utente installate e rilasciate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportSummaryEntry
{
  string ProductVersion;
  uint32 ProductVersionID;
  string TSCALType;
  uint32 InstalledLicenses;
  uint32 IssuedLicenses;
  string TSCALAvailability;
};
```

## <a name="members"></a>Members

La **classe \_ Win32 TSLicenseReportSummaryEntry** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ TSLicenseReportSummaryEntry** ha queste proprietà.

<dl> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di licenze CAL Per Utente di Servizi Desktop remoto installate.

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di licenze CAL Per Utente di Servizi Desktop remoto rilasciate.

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione di Servizi Desktop remoto per cui è stata rilasciata la licenza CAL Per Utente di Servizi Desktop remoto.

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

**TSCALAvailability**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Disponibilità delle licenze CAL Servizi Desktop remoto per utente. Si tratta di uno dei valori seguenti.

<dt>

"Disponibile"
</dt> <dd>

Sono disponibili le licenze CAL Per Utente di Servizi Desktop remoto.

</dd> <dt>

"Limited"
</dt> <dd>

La disponibilità delle licenze CAL Per Utente di Servizi Desktop remoto è limitata.

</dd> <dt>

"None"
</dt> <dd>

Le licenze CAL Per Utente di Servizi Desktop remoto non sono disponibili.

</dd> <dt>

"Not Tracking"
</dt> <dd>

La disponibilità delle licenze CAL Per Utente di Servizi Desktop remoto non viene rilevata.

</dd> </dl>

</dd> <dt>

**TSCALType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di licenze CAL Servizi Desktop remoto per utente. Si tratta di uno dei valori seguenti.

<dt>

"Per dispositivo"
</dt> <dd>

Le licenze CAL Per Utente di Servizi Desktop remoto vengono rilasciate per ogni dispositivo.

</dd> <dt>

"Per utente"
</dt> <dd>

Le licenze CAL Per Utente di Servizi Desktop remoto vengono rilasciate per utente.

</dd> <dt>

"Sconosciuto"
</dt> <dd>

Il tipo di licenze CAL Per Utente di Servizi Desktop remoto è sconosciuto.

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



 

 





