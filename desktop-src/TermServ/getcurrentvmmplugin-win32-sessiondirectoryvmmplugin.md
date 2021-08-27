---
title: Metodo GetCurrentVMMPlugin della Win32_SessionDirectoryVMMPlugin classe
description: Ottiene il plug-in con priorità più alta abilitato.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- Metodo GetCurrentVMMPlugin Servizi Desktop remoto
- Metodo GetCurrentVMMPlugin Servizi Desktop remoto , Win32_SessionDirectoryVMMPlugin classe
- Win32_SessionDirectoryVMMPlugin classe Servizi Desktop remoto metodo , GetCurrentVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.GetCurrentVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cc683275581aeb00c654a30e8c5aba7fd920f58248b480fc39caa96c885bb7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080111"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Metodo GetCurrentVMMPlugin della classe \_ Win32 SessionDirectoryVMMPlugin

Ottiene il plug-in con priorità più alta abilitato.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetCurrentVMMPlugin(
  [out] string  sName,
  [out] string  sProvider,
  [out] string  sServiceLocation,
  [out] string  sClassID,
  [out] sint32  Priority,
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sName* \[ Cambio\]
</dt> <dd>

Nome del plug-in.

</dd> <dt>

*sProvider* \[ Cambio\]
</dt> <dd>

Nome del provider del plug-in.

</dd> <dt>

*sServiceLocation* \[ Cambio\]
</dt> <dd>

Percorso del servizio che il plug-in deve contattare.

</dd> <dt>

*sClassID* \[ Cambio\]
</dt> <dd>

Identificatore di classe del plug-in.

</dd> <dt>

*Priorità* \[ Cambio\]
</dt> <dd>

Priorità del plug-in. Maggiore è il valore, maggiore sarà la priorità del plug-in.

</dd> <dt>

*Abilitato* \[ Cambio\]
</dt> <dd>

Indica se il plug-in è abilitato o disabilitato. **True** se il plug-in è abilitato o false in **caso** contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ SessionDirectoryVMMPlugin**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





