---
title: Classe Win32_TSLicenseReportSummaryEntry
description: Fornisce un riepilogo delle licenze di accesso client (RDS \ 160) installate e rilasciate Servizi Desktop remoto per utente. Licenze CAL per utente).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLicenseReportSummaryEntry Servizi Desktop remoto
- Classe Win32_TSLicenseReportSummaryEntry Servizi Desktop remoto, descritta
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
ms.openlocfilehash: f34482e9c6199ef6586024d43d586421a54071ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301057"
---
# <a name="win32_tslicensereportsummaryentry-class"></a>Win32 \_ TSLicenseReportSummaryEntry (classe)

Fornisce un riepilogo delle licenze di accesso client (RDS per utente) installate e riServizi Desktop remoto lasciate per ogni utente.

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

La classe **Win32 \_ TSLicenseReportSummaryEntry** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSLicenseReportSummaryEntry** dispone di queste proprietà.

<dl> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di licenze CAL per utente di Servizi Desktop remoto installate.

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di licenze CAL per utente per ogni utente rilasciate.

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione di Servizi Desktop remoto per cui è stata rilasciata la licenza CAL per utente.

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

**TSCALAvailability**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Disponibilità delle licenze CAL per utente per utente. Si tratta di uno dei valori seguenti.

<dt>

Disponibile
</dt> <dd>

Le licenze CAL per utente per utente sono disponibili.

</dd> <dt>

Limitato
</dt> <dd>

La disponibilità delle licenze CAL per utente per utente è limitata.

</dd> <dt>

"None"
</dt> <dd>

Le licenze CAL per utente per utente non sono disponibili.

</dd> <dt>

"Non rilevamento"
</dt> <dd>

Non è stata rilevata la disponibilità delle licenze CAL per utente per utente.

</dd> </dl>

</dd> <dt>

**TSCALType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di licenze CAL per utente per utente. Si tratta di uno dei valori seguenti.

<dt>

"Per dispositivo"
</dt> <dd>

Le licenze CAL per utente per utente vengono rilasciate per ogni dispositivo.

</dd> <dt>

"Per utente"
</dt> <dd>

Le licenze CAL per utente per utente vengono rilasciate per utente.

</dd> <dt>

Sconosciuto
</dt> <dd>

Il tipo di licenze CAL per utente per utente è sconosciuto.

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



 

 





