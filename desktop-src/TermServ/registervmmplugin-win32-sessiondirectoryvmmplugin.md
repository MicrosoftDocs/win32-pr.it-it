---
title: Metodo RegisterVMMPlugin della classe Win32_SessionDirectoryVMMPlugin
description: Registra un nuovo plug-in VMM.
ms.assetid: 8fa6109e-6320-4ad1-b313-f100d8383f85
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RegisterVMMPlugin
- Metodo RegisterVMMPlugin Servizi Desktop remoto, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Servizi Desktop remoto, metodo RegisterVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.RegisterVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381be34f9398147b323fa99093479da48adfd480
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400434"
---
# <a name="registervmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Metodo RegisterVMMPlugin della \_ classe SessionDirectoryVMMPlugin Win32

Registra un nuovo plug-in VMM.

## <a name="syntax"></a>Sintassi


```mof
uint32 RegisterVMMPlugin(
  [in] string  sName,
  [in] string  sProvider,
  [in] string  sServiceLocation,
  [in] string  sClassID,
  [in] sint32  Priority = ,
  [in] boolean Enabled = 
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sName* \[ in\]
</dt> <dd>

Nome del plug-in.

</dd> <dt>

*sProvider* \[ in\]
</dt> <dd>

Nome del provider del plug-in.

</dd> <dt>

*sServiceLocation* \[ in\]
</dt> <dd>

Posizione del servizio che il plug-in deve contattare.

</dd> <dt>

*sClassID* \[ in\]
</dt> <dd>

Identificatore di classe del plug-in.

</dd> <dt>

*Priorità* \[ di in\]
</dt> <dd>

Priorità del plug-in. Maggiore è il valore, maggiore è la priorità del plug-in.

</dd> <dt>

*Abilitato* \[ in\]
</dt> <dd>

Indica se il plug-in è abilitato o disabilitato. **True** se il plug-in è abilitato o **false** in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SessionDirectoryVMMPlugin Win32**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





