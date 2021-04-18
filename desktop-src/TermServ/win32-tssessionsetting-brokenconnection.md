---
title: Metodo BrokenConnection della classe Win32_TSSessionSetting (Wtsprotocol. h)
description: Imposta la proprietà BrokenConnectionAction, ovvero l'azione eseguita dal server in caso di raggiungimento del limite di tempo della sessione o di interruzione della connessione.
ms.assetid: 2422e314-9e1c-4bed-a958-eedd2daeca66
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo BrokenConnection
- Metodo BrokenConnection Servizi Desktop remoto, classe Win32_TSSessionSetting
- Classe Win32_TSSessionSetting Servizi Desktop remoto, metodo BrokenConnection
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.BrokenConnection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90b3f6bada75812b37df014cedadfb4e7ff2e83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301501"
---
# <a name="brokenconnection-method-of-the-win32_tssessionsetting-class"></a>Metodo BrokenConnection della \_ classe TSSessionSetting Win32

Imposta la proprietà **BrokenConnectionAction** , ovvero l'azione eseguita dal server in caso di raggiungimento del limite di tempo della sessione o di interruzione della connessione.

## <a name="syntax"></a>Sintassi


```mof
uint32 BrokenConnection(
  [in] uint32 BrokenConnectionAction
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*BrokenConnectionAction* \[ in\]
</dt> <dd>

Azione da eseguire.

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnetti** (0)


</dt> <dd>

L'utente è disconnesso dalla sessione.

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Termina** (1)


</dt> <dd>

La sessione viene eliminata definitivamente dal server.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se l'impostazione è sotto Criteri di gruppo controllo.

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>Wtsprotocol. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSSessionSetting Win32**](win32-tssessionsetting.md)
</dt> </dl>

 

