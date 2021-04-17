---
title: Metodo GenerateReportEx della classe Win32_TSLicenseReport
description: Genera un report sull'utilizzo delle licenze corrente per le licenze per utente e per dispositivo.
ms.assetid: c454e0c5-ca1c-41c7-86b2-1e52c414aeb5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GenerateReportEx
- Metodo GenerateReportEx Servizi Desktop remoto, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Servizi Desktop remoto, metodo GenerateReportEx
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReportEx
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893e6e29d1e4716560b0f0f6b41e6109c89e2f5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400323"
---
# <a name="generatereportex-method-of-the-win32_tslicensereport-class"></a>Metodo GenerateReportEx della \_ classe TSLicenseReport Win32

Genera un report sull'utilizzo delle licenze corrente per le licenze per utente e per dispositivo.

## <a name="syntax"></a>Sintassi


```mof
uint32 GenerateReportEx(
  [out] string FileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome file* \[ out\]
</dt> <dd>

Nome file del report generato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Si tratta di un metodo statico.

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

