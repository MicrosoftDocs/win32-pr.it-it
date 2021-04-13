---
title: Metodo DisconnectProtocol della classe Win32_TSGatewayConnection
description: Disconnette tutte le connessioni del protocollo specificato dal server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: 0ca3f478-dfdc-404e-ac17-43b6873b7256
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DisconnectProtocol
- Metodo DisconnectProtocol Servizi Desktop remoto, classe Win32_TSGatewayConnection
- Classe Win32_TSGatewayConnection Servizi Desktop remoto, metodo DisconnectProtocol
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
ms.openlocfilehash: 53a37050cbd622c6fea14b8b4e5dc6a414eaad85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340823"
---
# <a name="disconnectprotocol-method-of-the-win32_tsgatewayconnection-class"></a>Metodo DisconnectProtocol della \_ classe TSGatewayConnection Win32

Disconnette tutte le connessioni del protocollo specificato dal server Gateway Desktop remoto (Gateway Desktop remoto).

## <a name="syntax"></a>Sintassi


```mof
uint32 DisconnectProtocol(
  [in] string ProtocolName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProtocolName* \[ in\]
</dt> <dd>

Nome del protocollo per una connessione specifica. Questo può essere recuperato dalla proprietà **ProtocolName** della classe **Win32 \_ TSGatewayConnection** .

<dt>

TS
</dt> <dd>

Protocollo per il server Gateway Desktop remoto.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> </dl>

 

