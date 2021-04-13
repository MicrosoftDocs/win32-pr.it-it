---
title: Metodo RemoteControl della classe Win32_TSRemoteControlSetting
description: Il metodo RemoteControl imposta la proprietà LevelOfControl.
ms.assetid: 341f4f8d-17be-4482-834a-b771e041cfec
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoteControl
- Metodo RemoteControl Servizi Desktop remoto, classe Win32_TSRemoteControlSetting
- Classe Win32_TSRemoteControlSetting Servizi Desktop remoto, metodo RemoteControl
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
ms.openlocfilehash: 9476269c2f619b7ea46bc6546f106d7ccd2a486e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340632"
---
# <a name="remotecontrol-method-of-the-win32_tsremotecontrolsetting-class"></a>Metodo RemoteControl della \_ classe TSRemoteControlSetting Win32

Il metodo **RemoteControl** imposta la proprietà **LevelOfControl** .

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoteControl(
  [in] uint32 LevelOfControl
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LevelOfControl* \[ in\]
</dt> <dd>

Nuovo valore per la proprietà **LevelOfControl** , che specifica se la sessione verrà visualizzata solo dall'utente remoto oppure visualizzata e controllata tramite una tastiera e un mouse. Per altre informazioni, vedere la sezione Osservazioni. Sono supportati i valori seguenti.

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disabilita** (0)


</dt> <dd>

Il controllo remoto è disabilitato.

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)


</dt> <dd>

L'utente del controllo remoto dispone del controllo completo della sessione dell'utente, con l'autorizzazione dell'utente.

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)


</dt> <dd>

L'utente del controllo remoto ha il controllo completo della sessione dell'utente. l'autorizzazione dell'utente non è obbligatoria.

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)


</dt> <dd>

L'utente del controllo remoto può visualizzare la sessione in modalità remota con l'autorizzazione dell'utente. l'utente remoto non è in grado di controllare attivamente la sessione.

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)


</dt> <dd>

L'utente del controllo remoto può visualizzare la sessione in modalità remota, ma non controlla attivamente la sessione. l'autorizzazione dell'utente non è obbligatoria.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.

## <a name="remarks"></a>Commenti

Il controllo completo di una sessione significa che l'utente remoto può controllare attivamente la sessione dell'utente con una tastiera e un mouse.

Quando un utente tenta di stabilire una connessione di controllo remoto, il sistema Visualizza un messaggio nel client remoto, richiedendo l'autorizzazione per visualizzare o partecipare attivamente alla sessione remota.

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

[**\_TSRemoteControlSetting Win32**](win32-tsremotecontrolsetting.md)
</dt> </dl>

 

