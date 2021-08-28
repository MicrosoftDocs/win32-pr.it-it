---
title: Metodo SetPromptForPassword della classe Win32_TSLogonSetting
description: Il metodo SetPromptForPassword imposta la proprietà PromptForPassword.
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- Metodo SetPromptForPassword Servizi Desktop remoto
- Metodo SetPromptForPassword Servizi Desktop remoto , Win32_TSLogonSetting classe
- Win32_TSLogonSetting classe Servizi Desktop remoto, metodo SetPromptForPassword
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
ms.openlocfilehash: 90ea5202b0cfdfb624a05240deb042a88a8c73c8ea994cd810e1d9680ac0ddc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769521"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a>Metodo SetPromptForPassword della classe \_ Win32 TSLogonSetting

Il **metodo SetPromptForPassword** imposta la **proprietà PromptForPassword.**

## <a name="syntax"></a>Sintassi


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PromptForPassword* \[ Pollici\]
</dt> <dd>

Contrassegnare la disabilitazione o l'abilitazione **della proprietà PromptForPassword.**

<dt>

0
</dt> <dd>

Disabilita la richiesta della password.

</dd> <dt>

1
</dt> <dd>

Abilita la richiesta della password.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce Success in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori. Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

<dl> <dt>

**FALSE** (0)
</dt> <dt>

**TRUE** (1)
</dt> </dl>

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

[**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md)
</dt> </dl>

 

