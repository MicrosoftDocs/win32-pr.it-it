---
title: Metodo di scadenza della classe Win32_TSSessionSetting
description: Imposta il tempo massimo allocato al tipo di limite di sessione specificato.
ms.assetid: 55194197-ffb6-49ae-827a-478ced867ab0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo di scadenza
- Servizi Desktop remoto del metodo di scadenza, classe Win32_TSSessionSetting
- Classe Win32_TSSessionSetting Servizi Desktop remoto, metodo di scadenza
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.TimeLimit
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4016c28de50d31338d9bc6ec50ef1497c7a561da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517397"
---
# <a name="timelimit-method-of-the-win32_tssessionsetting-class"></a>Metodo di scadenza della \_ classe Win32 TSSessionSetting

Imposta il tempo massimo allocato al tipo di limite di sessione specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 TimeLimit(
  [in] string SessionLimitType,
  [in] uint32 ValueLimit
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SessionLimitType* \[ in\]
</dt> <dd>

Specifica il tipo di proprietà del limite di sessione che il metodo sta impostando.

<dt>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**


</dt> <dd>

Il metodo sta impostando la proprietà **ActiveSessionLimit** .

</dd> <dt>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**


</dt> <dd>

Il metodo sta impostando la proprietà **DisconnectedSessionLimit** .

</dd> <dt>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**


</dt> <dd>

Il metodo sta impostando la proprietà **IdleSessionLimit** .

</dd> </dl> </dd> <dt>

*ValueLimit* \[ in\]
</dt> <dd>

Il nuovo tempo massimo, in millisecondi, per la proprietà specificata dal parametro *SessionLimitType* . Il valore zero indica che non esiste alcun limite di sessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.

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

[**\_TSSessionSetting Win32**](win32-tssessionsetting.md)
</dt> </dl>

 

