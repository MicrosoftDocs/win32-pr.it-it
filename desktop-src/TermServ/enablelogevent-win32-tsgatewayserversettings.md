---
title: Metodo EnableLogEvent della classe Win32_TSGatewayServerSettings
description: Abilita o disabilita la registrazione del tipo di evento specificato.
ms.assetid: e901ef51-2ae2-4123-902a-ac359f3eb959
ms.tgt_platform: multiple
keywords:
- Metodo EnableLogEvent Servizi Desktop remoto
- Metodo EnableLogEvent Servizi Desktop remoto , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Servizi Desktop remoto metodo EnableLogEvent
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableLogEvent
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd70902649f6fadc66308ad35ce165a6d2fdb4654b73e056c3bc38f1850b3e07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871721"
---
# <a name="enablelogevent-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo EnableLogEvent della classe \_ TSGatewayServerSettings Win32

Abilita o disabilita la registrazione del tipo di evento specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 EnableLogEvent(
  [in] string  EventName,
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EventName* \[ Pollici\]
</dt> <dd>

Nome dell'evento. Questo valore deve essere recuperato usando il [**metodo GetLogEventName.**](getlogeventname-win32-tsgatewayserversettings.md)

<dt>

LogChannelDisconnect
</dt> <dd>

L'utente è stato disconnesso dalla risorsa.

</dd> <dt>

LogFailedChannelConnect
</dt> <dd>

L'utente non è riuscito a connettersi alla risorsa.

</dd> <dt>

LogFailureNetworkAccessCheck
</dt> <dd>

Autorizzazione di connessione non riuscita dall'utente.

</dd> <dt>

LogFailureResourceAccessCheck
</dt> <dd>

Autorizzazione delle risorse non riuscita dall'utente.

</dd> <dt>

LogSuccessChannelConnect
</dt> <dd>

L'utente si è connesso alla risorsa.

</dd> <dt>

LogSuccessfulNetworkAccessCheck
</dt> <dd>

L'utente ha superato l'autorizzazione di connessione.

</dd> <dt>

LogSuccessfulResourceAccessCheck
</dt> <dd>

L'utente ha superato correttamente l'autorizzazione della risorsa.

</dd> </dl> </dd> <dt>

*Abilitato* \[ Pollici\]
</dt> <dd>

Specifica se l'evento deve essere abilitato o disabilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

