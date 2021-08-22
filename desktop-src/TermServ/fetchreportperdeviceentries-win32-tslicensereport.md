---
title: Metodo FetchReportPerDeviceEntries della classe Win32_TSLicenseReport
description: Recupera informazioni sulle licenze di accesso client Servizi Desktop remoto per dispositivo (Servizi Desktop remoto \ 160; Cal cal per dispositivo) dal report.
ms.assetid: 3f632a65-d6e0-4efd-9498-d04a05f9ddec
ms.tgt_platform: multiple
keywords:
- Metodo FetchReportPerDeviceEntries Servizi Desktop remoto
- Metodo FetchReportPerDeviceEntries Servizi Desktop remoto , Win32_TSLicenseReport classe
- Win32_TSLicenseReport classe Servizi Desktop remoto , metodo FetchReportPerDeviceEntries
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
ms.openlocfilehash: bb3a5ef050002da069f7eda56352f204797cac521885248bc7e63dfd77f840f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737561"
---
# <a name="fetchreportperdeviceentries-method-of-the-win32_tslicensereport-class"></a>Metodo FetchReportPerDeviceEntries della classe \_ Win32 TSLicenseReport

Recupera dal report le Servizi Desktop remoto di accesso client per dispositivo (LICENZE CAL Per dispositivo di Servizi Desktop remoto).

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

*StartIndex* \[ Pollici\]
</dt> <dd>

Indice della prima voce del report da recuperare. La prima voce del report ha un indice pari a zero.

</dd> <dt>

*Conteggio* \[ in, out\]
</dt> <dd>

Numero di voci del report da recuperare dall'oggetto report. Il valore zero indica che tutte le voci del report a partire da *StartIndex* devono essere recuperate. In caso di restituzione, contiene il numero di voci nella matrice *ReportPerDeviceEntries.*

</dd> <dt>

*ReportPerDeviceEntries* \[ Cambio\]
</dt> <dd>

Matrice di [**classi Win32 \_ TSLicenseReportPerDeviceEntry**](win32-tslicensereportperdeviceentry.md) che rappresentano le voci di licenza recuperate. Il *parametro Count* contiene il numero di elementi in questa matrice.

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

 

 





