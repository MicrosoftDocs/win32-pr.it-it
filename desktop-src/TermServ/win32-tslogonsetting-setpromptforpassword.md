---
title: Metodo SetPromptForPassword della classe Win32_TSLogonSetting
description: Il metodo SetPromptForPassword imposta la proprietà PromptForPassword.
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetPromptForPassword
- Metodo SetPromptForPassword Servizi Desktop remoto, classe Win32_TSLogonSetting
- Classe Win32_TSLogonSetting Servizi Desktop remoto, metodo SetPromptForPassword
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.SetPromptForPassword
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86dc065a143505ea81bce78d9bf787fae6b0a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301962"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a>Metodo SetPromptForPassword della \_ classe TSLogonSetting Win32

Il metodo **SetPromptForPassword** imposta la proprietà **PromptForPassword** .

## <a name="syntax"></a>Sintassi


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PromptForPassword* \[ in\]
</dt> <dd>

Flag che disabilita o Abilita la proprietà **PromptForPassword** .

<dt>

0
</dt> <dd>

Disabilita la richiesta di conferma della password.

</dd> <dt>

1
</dt> <dd>

Abilita la richiesta di conferma della password.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.

<dl> <dt>

**False** (0)
</dt> <dt>

**True** (1)
</dt> </dl>

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSLogonSetting Win32**](win32-tslogonsetting.md)
</dt> </dl>

 

