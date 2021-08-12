---
title: Metodo IsLogEventEnabled della Win32_TSGatewayServerSettings classe
description: Indica se il tipo di registro eventi specificato è abilitato.
ms.assetid: 4abfc56f-871a-44ef-9998-da88949a0a2d
ms.tgt_platform: multiple
keywords:
- Metodo IsLogEventEnabled Servizi Desktop remoto
- Metodo IsLogEventEnabled Servizi Desktop remoto , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Servizi Desktop remoto , metodo IsLogEventEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsLogEventEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7130578287e313e03caf8b63c2e187f401608ad1cdbd575ae9e6bb6450e1adf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606060"
---
# <a name="islogeventenabled-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo IsLogEventEnabled della classe \_ TSGatewayServerSettings Win32

Indica se il tipo di registro eventi specificato è abilitato.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsLogEventEnabled(
  [in]  string  EventName,
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome evento* \[ Pollici\]
</dt> <dd>

Nome del tipo di registro eventi. Questo valore deve essere recuperato usando il [**metodo GetLogEventName.**](getlogeventname-win32-tsgatewayserversettings.md)

<dt>

LogChannelDisconnect
</dt> <dd>

L'utente si è disconnesso dalla risorsa.

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

L'utente ha superato l'autorizzazione delle risorse.

</dd> </dl> </dd> <dt>

*Abilitato* \[ Cambio\]
</dt> <dd>

Indica se il tipo di registro eventi specificato è abilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco dei codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per Windows di Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

