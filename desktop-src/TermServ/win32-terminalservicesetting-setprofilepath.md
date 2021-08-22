---
title: Metodo SetProfilePath della classe Win32_TerminalServiceSetting
description: Il metodo SetProfilePath imposta la proprietà ProfilePath per la classe.
ms.assetid: a0dfe6a4-929c-45ec-bd31-7e0ffb6ce5de
ms.tgt_platform: multiple
keywords:
- Metodo SetProfilePath Servizi Desktop remoto
- Metodo SetProfilePath Servizi Desktop remoto , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Servizi Desktop remoto metodo SetProfilePath
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetProfilePath
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fafbd3c4556899ad2602f0b7ca1897a7aff4a4db98e4773ea56d2405b9423f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514331"
---
# <a name="setprofilepath-method-of-the-win32_terminalservicesetting-class"></a>Metodo SetProfilePath della classe TerminalServiceSetting Win32 \_

Il **metodo SetProfilePath** imposta la **proprietà ProfilePath** per la classe.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetProfilePath(
  [in] string ProfilePath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProfilePath* \[ Pollici\]
</dt> <dd>

Nuovo valore per la **proprietà ProfilePath,** che specifica il percorso del profilo per il computer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce Success in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori.

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

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

