---
title: Metodo FetchReportFailedPerUserEntries della classe Win32_TSLicenseReport
description: Recupera i dettagli delle licenze di accesso client non riuscite Servizi Desktop remoto per utente (RDS \ 160; Licenze CAL per utente) dal report.
ms.assetid: 2c16723c-1755-4ec1-a6db-55d769f8b6fd
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo FetchReportFailedPerUserEntries
- Metodo FetchReportFailedPerUserEntries Servizi Desktop remoto, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Servizi Desktop remoto, metodo FetchReportFailedPerUserEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 159f980944c70dbad4c6948a614d0c9964a5f0cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518844"
---
# <a name="fetchreportfailedperuserentries-method-of-the-win32_tslicensereport-class"></a>Metodo FetchReportFailedPerUserEntries della \_ classe TSLicenseReport Win32

Recupera i dettagli relativi alle licenze CAL per utente non riuscite Servizi Desktop remoto per utente dal report.

## <a name="syntax"></a>Sintassi


```mof
uint32 FetchReportFailedPerUserEntries(
  [in]      uint32                                  StartIndex,
  [in, out] uint32                                  Count,
  [out]     Win32_TSLicenseReportFailedPerUserEntry ReportFailedPerUserEntries[]
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

Numero di voci del report da recuperare dall'oggetto report. Un valore pari a zero indica che devono essere recuperate tutte le voci del report a partire da *startIndex* . Nell'output restituito è contenuto il numero di voci nella matrice *ReportFailedPerUserEntries* .

</dd> <dt>

*ReportFailedPerUserEntries* \[ out\]
</dt> <dd>

Matrice di classi [**\_ TSLicenseReportFailedPerUserEntry Win32**](win32-tslicensereportfailedperuserentry.md) che rappresentano le voci di licenza recuperate. Il parametro *count* contiene il numero di elementi in questa matrice.

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

 

 





