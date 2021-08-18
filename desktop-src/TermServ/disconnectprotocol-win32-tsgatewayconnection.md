---
title: Metodo DisconnectProtocol della Win32_TSGatewayConnection classe
description: Disconnette tutte le connessioni del protocollo specificato dal server Desktop remoto Gateway Desktop remoto.
ms.assetid: 0ca3f478-dfdc-404e-ac17-43b6873b7256
ms.tgt_platform: multiple
keywords:
- Metodo DisconnectProtocol Servizi Desktop remoto
- Metodo DisconnectProtocol Servizi Desktop remoto , Win32_TSGatewayConnection classe
- Win32_TSGatewayConnection classe Servizi Desktop remoto , metodo DisconnectProtocol
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectProtocol
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c3c987a07dddfee5814cc32fbab8e77e2b7af5d6e55768965294cfeadaf5fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118856246"
---
# <a name="disconnectprotocol-method-of-the-win32_tsgatewayconnection-class"></a>Metodo DisconnectProtocol della classe \_ TSGatewayConnection Win32

Disconnette tutte le connessioni del protocollo specificato dal server Desktop remoto Gateway Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 DisconnectProtocol(
  [in] string ProtocolName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProtocolName* \[ Pollici\]
</dt> <dd>

Nome del protocollo per una connessione specifica. Può essere recuperato dalla **proprietà ProtocolName** della **classe \_ Win32 TSGatewayConnection.**

<dt>

"TS"
</dt> <dd>

Protocollo per il server Gateway Desktop remoto.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco dei codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**Connessione \_ TSGateway Win32**](win32-tsgatewayconnection.md)
</dt> </dl>

 

