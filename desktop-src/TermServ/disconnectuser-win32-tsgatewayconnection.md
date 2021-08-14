---
title: Metodo DisconnectUser della classe Win32_TSGatewayConnection (Tsgauthenticationengine.h)
description: Disconnette tutte le connessioni dell'utente specificato dal server Desktop remoto Gateway Desktop remoto.
ms.assetid: 3c5d66b6-c1f0-4a91-bf93-be886d8e2391
ms.tgt_platform: multiple
keywords:
- Metodo DisconnectUser Servizi Desktop remoto
- Metodo DisconnectUser Servizi Desktop remoto , Win32_TSGatewayConnection classe
- Win32_TSGatewayConnection classe Servizi Desktop remoto , metodo DisconnectUser
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
ms.openlocfilehash: 8d31c7c89d285aed576024c551b07766a7387938762d60c252dec43e491037e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130996"
---
# <a name="disconnectuser-method-of-the-win32_tsgatewayconnection-class"></a>Metodo DisconnectUser della classe \_ TSGatewayConnection Win32

Disconnette tutte le connessioni dell'utente specificato dal server Desktop remoto Gateway Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 DisconnectUser(
  [in] string UserName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UserName* \[ Pollici\]
</dt> <dd>

Nome utente, in formato *Domain* **\\** _UserName,_ le cui connessioni devono essere disconnesse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                            |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                       |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Tsgauthenticationengine.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl>             |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> </dl>

 

