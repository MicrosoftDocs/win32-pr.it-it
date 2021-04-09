---
title: Metodo DisconnectUser della classe Win32_TSGatewayConnection (Tsgauthenticationengine. h)
description: Disconnette tutte le connessioni dell'utente specificato dal server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: 3c5d66b6-c1f0-4a91-bf93-be886d8e2391
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DisconnectUser
- Metodo DisconnectUser Servizi Desktop remoto, classe Win32_TSGatewayConnection
- Classe Win32_TSGatewayConnection Servizi Desktop remoto, metodo DisconnectUser
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectUser
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e223a2de36ad6c2a6fcabc446fe88cad27dc5da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742151"
---
# <a name="disconnectuser-method-of-the-win32_tsgatewayconnection-class"></a>Metodo DisconnectUser della \_ classe TSGatewayConnection Win32

Disconnette tutte le connessioni dell'utente specificato dal server Gateway Desktop remoto (Gateway Desktop remoto).

## <a name="syntax"></a>Sintassi


```mof
uint32 DisconnectUser(
  [in] string UserName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome utente* \[ in\]
</dt> <dd>

Nome utente, nel formato * domain * **\\** _username_ , le cui connessioni devono essere disconnesse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                            |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                       |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Tsgauthenticationengine. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl>             |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> </dl>

 

