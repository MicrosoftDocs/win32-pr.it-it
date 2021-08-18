---
title: Metodo RemoteControl della classe Win32_TSRemoteControlSetting
description: Il metodo RemoteControl imposta la proprietà LevelOfControl.
ms.assetid: 341f4f8d-17be-4482-834a-b771e041cfec
ms.tgt_platform: multiple
keywords:
- Metodo RemoteControl Servizi Desktop remoto
- Metodo RemoteControl Servizi Desktop remoto , Win32_TSRemoteControlSetting classe
- Win32_TSRemoteControlSetting classe Servizi Desktop remoto , metodo RemoteControl
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting.RemoteControl
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73de3f92171f688a9c0dc611552a061a3f2de7bf573fa41dab8606395eafe228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769421"
---
# <a name="remotecontrol-method-of-the-win32_tsremotecontrolsetting-class"></a>Metodo RemoteControl della classe \_ Win32 TSRemoteControlSetting

Il **metodo RemoteControl** imposta la **proprietà LevelOfControl.**

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoteControl(
  [in] uint32 LevelOfControl
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LevelOfControl* \[ Pollici\]
</dt> <dd>

Nuovo valore per la **proprietà LevelOfControl,** che specifica se la sessione verrà visualizzata solo dall'utente remoto o visualizzata e controllata tramite tastiera e mouse. Per altre informazioni, vedere la sezione Osservazioni. Sono supportati i valori seguenti.

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disabilita** (0)


</dt> <dd>

Il controllo remoto è disabilitato.

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)


</dt> <dd>

L'utente del controllo remoto ha il controllo completo della sessione dell'utente, con l'autorizzazione dell'utente.

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)


</dt> <dd>

L'utente del controllo remoto ha il controllo completo della sessione dell'utente. L'autorizzazione dell'utente non è necessaria.

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)


</dt> <dd>

L'utente del controllo remoto può visualizzare la sessione in modalità remota, con l'autorizzazione dell'utente. l'utente remoto non può controllare attivamente la sessione.

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)


</dt> <dd>

L'utente del controllo remoto può visualizzare la sessione in modalità remota, ma non controllare attivamente la sessione. L'autorizzazione dell'utente non è necessaria.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto codici di errore del provider WMI,](terminal-services-wmi-provider-error-codes.md) vedere . Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

## <a name="remarks"></a>Commenti

Il controllo completo di una sessione significa che l'utente remoto può controllare attivamente la sessione dell'utente con una tastiera e un mouse.

Quando un utente tenta di stabilire una connessione di controllo remoto, il sistema visualizza un messaggio al client remoto, richiedendo l'autorizzazione per visualizzare o partecipare attivamente alla sessione remota.

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

[**Win32 \_ TSRemoteControlSetting**](win32-tsremotecontrolsetting.md)
</dt> </dl>

 

