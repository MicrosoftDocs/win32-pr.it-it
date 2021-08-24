---
title: Metodo FetchReportFailedPerUserSummaryEntries della Win32_TSLicenseReport classe
description: Recupera informazioni di riepilogo delle licenze di accesso client per Servizi Desktop remoto per utente (Servizi Desktop remoto \ 160; Cal cal per utente) dal report.
ms.assetid: dc9c4a36-b2a8-407e-b902-ee9d51227909
ms.tgt_platform: multiple
keywords:
- Metodo FetchReportFailedPerUserSummaryEntries Servizi Desktop remoto
- Metodo FetchReportFailedPerUserSummaryEntries Servizi Desktop remoto , Win32_TSLicenseReport classe
- Win32_TSLicenseReport classe Servizi Desktop remoto , metodo FetchReportFailedPerUserSummaryEntries
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
ms.openlocfilehash: cc42cb36ad0d203389dd115eb6bf02b1135982f1c490a0f669e19d2f64e937ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737551"
---
# <a name="fetchreportfailedperusersummaryentries-method-of-the-win32_tslicensereport-class"></a>Metodo FetchReportFailedPerUserSummaryEntries della classe \_ Win32 TSLicenseReport

Recupera dal report le informazioni di riepilogo Servizi Desktop remoto licenze CAL client per utente per utente.

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

*StartIndex* \[ Pollici\]
</dt> <dd>

Indice della prima voce del report da recuperare. La prima voce del report ha un indice pari a zero.

</dd> <dt>

*Conteggio* \[ in, out\]
</dt> <dd>

Numero di voci del report da recuperare dall'oggetto report. Il valore zero indica che tutte le voci del report a partire da *StartIndex* devono essere recuperate. In caso di restituzione, contiene il numero di voci nella matrice *ReportFailedPerUserSummaryEntries.*

</dd> <dt>

*ReportFailedPerUserSummaryEntries* \[ Cambio\]
</dt> <dd>

Matrice di [**classi Win32 \_ TSLicenseReportFailedPerUserSummaryEntry**](win32-tslicensereportfailedperusersummaryentry.md) che rappresentano le voci di licenza recuperate. Il *parametro Count* contiene il numero di elementi in questa matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

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

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> </dl>

 

 





