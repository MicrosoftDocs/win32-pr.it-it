---
title: Metodo SetAllowDwm della classe Win32_TSClientSetting
description: Imposta la proprietà AllowDwm.
ms.assetid: c70d3dc9-c109-4d77-be50-20a0352282d6
ms.tgt_platform: multiple
keywords:
- Metodo SetAllowDwm Servizi Desktop remoto
- Metodo SetAllowDwm Servizi Desktop remoto , Win32_TSClientSetting classe
- Win32_TSClientSetting classe Servizi Desktop remoto, metodo SetAllowDwm
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetAllowDwm
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e48373859e59464986aab85bf00d16a76a066bad12e3e38bf7b07275257016
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009031"
---
# <a name="setallowdwm-method-of-the-win32_tsclientsetting-class"></a>Metodo SetAllowDwm della classe \_ Win32 TSClientSetting

Imposta la **proprietà AllowDwm.**

## <a name="syntax"></a>Sintassi


```mof
uint32 SetAllowDwm(
  [in] uint32 AllowDwm
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AllowDwm* \[ Pollici\]
</dt> <dd>

Nuovo valore **della proprietà AllowDwm.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto di questi valori,](terminal-services-wmi-provider-error-codes.md) fare riferimento Servizi Desktop remoto di errore del provider WMI. Il metodo restituisce un errore se le impostazioni di connessione dell'utente vengono sostituite dal server.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                               |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

 





