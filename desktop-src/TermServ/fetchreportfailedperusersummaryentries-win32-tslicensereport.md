---
title: Metodo FetchReportFailedPerUserSummaryEntries della classe Win32_TSLicenseReport
description: Recupera le informazioni di riepilogo di Servizi Desktop remoto non riuscite per licenze client Access (RDS \ 160; Licenze CAL per utente) dal report.
ms.assetid: dc9c4a36-b2a8-407e-b902-ee9d51227909
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo FetchReportFailedPerUserSummaryEntries
- Metodo FetchReportFailedPerUserSummaryEntries Servizi Desktop remoto, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Servizi Desktop remoto, metodo FetchReportFailedPerUserSummaryEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219c2c854e04dabf8b5bfe0b5b70a07bbc3c57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302478"
---
# <a name="fetchreportfailedperusersummaryentries-method-of-the-win32_tslicensereport-class"></a>Metodo FetchReportFailedPerUserSummaryEntries della \_ classe TSLicenseReport Win32

Recupera le informazioni di riepilogo di Servizi Desktop remoto non riuscite per licenze CAL per utente per utente dal report.

## <a name="syntax"></a>Sintassi


```mof
uint32 FetchReportFailedPerUserSummaryEntries(
  [in]      uint32                                         StartIndex,
  [in, out] uint32                                         Count,
  [out]     Win32_TSLicenseReportFailedPerUserSummaryEntry ReportFailedPerUserSummaryEntries[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StartIndex* \[ in\]
</dt> <dd>

Indice della prima voce del report da recuperare. La prima voce del report ha un indice pari a zero.

</dd> <dt>

*Numero* \[ di in uscita\]
</dt> <dd>

Numero di voci del report da recuperare dall'oggetto report. Un valore pari a zero indica che devono essere recuperate tutte le voci del report a partire da *startIndex* . Nell'output restituito è contenuto il numero di voci nella matrice *ReportFailedPerUserSummaryEntries* .

</dd> <dt>

*ReportFailedPerUserSummaryEntries* \[ out\]
</dt> <dd>

Matrice di classi [**\_ TSLicenseReportFailedPerUserSummaryEntry Win32**](win32-tslicensereportfailedperusersummaryentry.md) che rappresentano le voci di licenza recuperate. Il parametro *count* contiene il numero di elementi in questa matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

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

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> </dl>

 

 





