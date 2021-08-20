---
title: Metodo GenerateReport della classe Win32_TSLicenseReport (Gpmgmt.h)
description: GenerateReport non è più disponibile per l'uso a Windows Server 2012.
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- Metodo GenerateReport Servizi Desktop remoto
- Metodo GenerateReport Servizi Desktop remoto , Win32_TSLicenseReport classe
- Win32_TSLicenseReport classe Servizi Desktop remoto , metodo GenerateReport
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a619da8130187a4ab5d39de390315dd99b3ee7a171005a4cf66e7bb5677ae87c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130780"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a>Metodo GenerateReport della classe \_ TSLicenseReport Win32

\[**GenerateReport** non è più disponibile per l'uso a Windows Server 2012. Usare invece [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]

Questo metodo non è supportato.

**Windows Server 2008 R2 e Windows Server 2008:** Genera un report corrente sull'utilizzo delle licenze per utente nel server Desktop remoto licenze.

## <a name="syntax"></a>Sintassi


```mof
uint32 GenerateReport(
  [in]  uint32 ScopeType,
  [in]  string ScopeValue,
  [out] string FileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ScopeType* \[ Pollici\]
</dt> <dd>

Ambito del report sull'utilizzo delle licenze. Può avere i valori seguenti.

<dt>

1
</dt> <dd>

Il report verrà generato per l'intero dominio.

</dd> <dt>

2
</dt> <dd>

Il report verrà generato per l'unità organizzativa specificata nel *parametro ScopeValue.*

</dd> <dt>

3
</dt> <dd>

Il report verrà generato per tutti i domini attendibili.

</dd> </dl> </dd> <dt>

*ScopeValue* \[ Pollici\]
</dt> <dd>

Se il *parametro ScopeType* è 2, *ScopeType* specifica l'unità organizzativa per cui verrà generato il report. È necessario specificare *ScopeValue* usando il formato **OU=**_OUName1_*_,OU=_*_OUName2_*_..._*.

</dd> <dt>

*FileName* \[ Cambio\]
</dt> <dd>

Nome file del report generato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **WBEM \_ E NOT \_ \_ SUPPORTED**.

**Windows Server 2008 R2 e Windows Server 2008:** Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Si tratta di un metodo statico.

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                                 |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                         |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| Intestazione<br/>                   | <dl> <dt>Gpmgmt.h</dt> </dl>       |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> </dl>

 

