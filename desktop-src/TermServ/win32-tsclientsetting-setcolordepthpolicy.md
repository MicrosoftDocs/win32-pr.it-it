---
title: Metodo SetColorDepthPolicy della classe Win32_TSClientSetting
description: Il metodo SetColorDepthPolicy imposta la proprietà ColorDepthPolicy per la classe.
ms.assetid: 7a8c2b51-5f7a-4188-aae0-0b2d47d043bd
ms.tgt_platform: multiple
keywords:
- Metodo SetColorDepthPolicy Servizi Desktop remoto
- Metodo SetColorDepthPolicy Servizi Desktop remoto , Win32_TSClientSetting classe
- Win32_TSClientSetting classe Servizi Desktop remoto, metodo SetColorDepthPolicy
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepthPolicy
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ecb53500a65c997ace21865492a0a473c2799bd38a3876c4676aaea4120610
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999841"
---
# <a name="setcolordepthpolicy-method-of-the-win32_tsclientsetting-class"></a>Metodo SetColorDepthPolicy della classe \_ Win32 TSClientSetting

Il **metodo SetColorDepthPolicy** imposta la **proprietà ColorDepthPolicy** per la classe.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetColorDepthPolicy(
  [in] uint32 ColorDepthPolicy
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ColorDepthPolicy* \[ Pollici\]
</dt> <dd>

Flag che disabilita o abilita la **proprietà SetColorDepthPolicy,** che specifica se eseguire l'override dell'impostazione di colore massima dell'utente.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Abilitare la proprietà .

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Disabilitare la proprietà .

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce Success in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto codici di errore del provider WMI,](terminal-services-wmi-provider-error-codes.md) vedere . Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

## <a name="remarks"></a>Commenti

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

