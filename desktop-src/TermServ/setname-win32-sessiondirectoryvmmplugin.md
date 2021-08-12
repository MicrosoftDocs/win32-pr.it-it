---
title: Metodo SetName della classe Win32_SessionDirectoryVMMPlugin
description: Imposta il nome del plug-in.
ms.assetid: 8af4abca-f147-4027-91fb-4d669b58caa4
ms.tgt_platform: multiple
keywords:
- Metodo SetName Servizi Desktop remoto
- Metodo SetName Servizi Desktop remoto , Win32_SessionDirectoryVMMPlugin classe
- Win32_SessionDirectoryVMMPlugin classe Servizi Desktop remoto , metodo SetName
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetName
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6960d08f39e7ce026a36d1644bebf49aec292a44d900974ebd8481379b00dcf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604640"
---
# <a name="setname-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Metodo SetName della classe \_ Win32 SessionDirectoryVMMPlugin

Imposta il nome del plug-in.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetName(
  [in] string sName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sName* \[ Pollici\]
</dt> <dd>

Nome del plug-in.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto codici di errore del provider WMI,](terminal-services-wmi-provider-error-codes.md) vedere .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ SessionDirectoryVMMPlugin**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





