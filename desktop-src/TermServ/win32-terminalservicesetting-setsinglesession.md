---
title: Metodo SetSingleSession della classe Win32_TerminalServiceSetting
description: Il metodo SetSingleSession imposta la proprietà SingleSession per la classe .
ms.assetid: 67ccfa9d-86a5-4501-9d61-c7f1677ec3d5
ms.tgt_platform: multiple
keywords:
- Metodo SetSingleSession Servizi Desktop remoto
- Metodo SetSingleSession Servizi Desktop remoto , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Servizi Desktop remoto, metodo SetSingleSession
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSingleSession
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93fe070a2c820a1fe098d34c65a00a78b2bb9abecb85dd672ba048a99d7f565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755686"
---
# <a name="setsinglesession-method-of-the-win32_terminalservicesetting-class"></a>Metodo SetSingleSession della classe TerminalServiceSetting Win32 \_

Il **metodo SetSingleSession** imposta la **proprietà SingleSession** per la classe .

## <a name="syntax"></a>Sintassi


```mof
uint32 SetSingleSession(
  [in] uint32 SingleSession
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SingleSession* \[ Pollici\]
</dt> <dd>

Contrassegnare la disabilitazione o l'abilitazione della proprietà **SingleSession,** che determina se gli utenti sono limitati a una o Servizi Desktop remoto sessioni.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Disabilitare la proprietà .

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Abilitare la proprietà .

</dd> </dl> </dd> </dl>

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

 

