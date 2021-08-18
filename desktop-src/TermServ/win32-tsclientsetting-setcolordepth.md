---
title: Metodo SetColorDepth della Win32_TSClientSetting classe
description: Il metodo SetColorDepth imposta la proprietà ColorDepth per la classe.
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- Metodo SetColorDepth Servizi Desktop remoto
- Metodo SetColorDepth Servizi Desktop remoto , Win32_TSClientSetting classe
- Win32_TSClientSetting classe Servizi Desktop remoto metodo SetColorDepth
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepth
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2c7f31ef04fdfb9dcbfee5e1ca3dcec1386a7dbd0c20824b00bdfe41ac6d48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999861"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a>Metodo SetColorDepth della classe \_ Win32 TSClientSetting

Il **metodo SetColorDepth** imposta la **proprietà ColorDepth** per la classe.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ColorDepth* \[ Pollici\]
</dt> <dd>

Nuovo valore per la **proprietà ColorDepth.**

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

8 bit per pixel

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

15 bit per pixel

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

16 bit per pixel

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

24 bit per pixel

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5**


</dt> <dd>

32 bit per pixel

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce Success in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto codici di errore del provider WMI,](terminal-services-wmi-provider-error-codes.md) vedere . Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

