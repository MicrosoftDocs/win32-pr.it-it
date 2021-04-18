---
title: Metodo FetchReportPerDeviceEntries della classe Win32_TSLicenseReport
description: Recupera le informazioni sulle licenze di accesso client per dispositivo Servizi Desktop remoto emesse (RDS \ 160; Per dispositivo CAL) dal report.
ms.assetid: 3f632a65-d6e0-4efd-9498-d04a05f9ddec
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo FetchReportPerDeviceEntries
- Metodo FetchReportPerDeviceEntries Servizi Desktop remoto, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Servizi Desktop remoto, metodo FetchReportPerDeviceEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportPerDeviceEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce77fce941dd0a24fb6ee17e0aeb67b4e78bdae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302477"
---
# <a name="fetchreportperdeviceentries-method-of-the-win32_tslicensereport-class"></a>Metodo FetchReportPerDeviceEntries della \_ classe TSLicenseReport Win32

Recupera le informazioni sulle licenze di accesso client per dispositivo di Servizi Desktop remoto emesse dal report.

## <a name="syntax"></a>Sintassi


```mof
uint32 FetchReportPerDeviceEntries(
  [in]      uint32                              StartIndex,
  [in, out] uint32                              Count,
  [out]     Win32_TSLicenseReportPerDeviceEntry ReportPerDeviceEntries[]
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

Numero di voci del report da recuperare dall'oggetto report. Un valore pari a zero indica che devono essere recuperate tutte le voci del report a partire da *startIndex* . Nell'output restituito è contenuto il numero di voci nella matrice *ReportPerDeviceEntries* .

</dd> <dt>

*ReportPerDeviceEntries* \[ out\]
</dt> <dd>

Matrice di classi [**\_ TSLicenseReportPerDeviceEntry Win32**](win32-tslicensereportperdeviceentry.md) che rappresentano le voci di licenza recuperate. Il parametro *count* contiene il numero di elementi in questa matrice.

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

 

 





