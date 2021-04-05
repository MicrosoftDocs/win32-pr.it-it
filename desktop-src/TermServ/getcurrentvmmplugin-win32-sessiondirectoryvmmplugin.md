---
title: Metodo GetCurrentVMMPlugin della classe Win32_SessionDirectoryVMMPlugin
description: Ottiene il plug-in con priorità più elevata attivato.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetCurrentVMMPlugin
- Metodo GetCurrentVMMPlugin Servizi Desktop remoto, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Servizi Desktop remoto, metodo GetCurrentVMMPlugin
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
ms.openlocfilehash: 7162322f4e5e3939309d64e27c93cf8d20da540c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874542"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Metodo GetCurrentVMMPlugin della \_ classe SessionDirectoryVMMPlugin Win32

Ottiene il plug-in con priorità più elevata attivato.

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

*sName* \[ out\]
</dt> <dd>

Nome del plug-in.

</dd> <dt>

*sProvider* \[ out\]
</dt> <dd>

Nome del provider del plug-in.

</dd> <dt>

*sServiceLocation* \[ out\]
</dt> <dd>

Posizione del servizio che il plug-in deve contattare.

</dd> <dt>

*sClassID* \[ out\]
</dt> <dd>

Identificatore di classe del plug-in.

</dd> <dt>

*Priorità* \[ di out\]
</dt> <dd>

Priorità del plug-in. Maggiore è il valore, maggiore è la priorità del plug-in.

</dd> <dt>

*Abilitato* \[ out\]
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

 

 





