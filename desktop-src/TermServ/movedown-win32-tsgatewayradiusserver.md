---
title: Metodo MoveDown della classe Win32_TSGatewayRADIUSServer
description: Sposta questo Remote Authentication Dial-In User Service server RADIUS una posizione verso il basso nell'ordine di priorità.
ms.assetid: 1b12d2a0-1463-4bd7-9b92-5df2ba799a8a
ms.tgt_platform: multiple
keywords:
- Metodo MoveDown Servizi Desktop remoto
- Metodo MoveDown Servizi Desktop remoto , Win32_TSGatewayRADIUSServer classe
- Win32_TSGatewayRADIUSServer classe Servizi Desktop remoto , metodo MoveDown
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acee402af28ed62c5f4627972b083d1fd5c3ed7f49b02a058fb4f2562ffbd681
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138167"
---
# <a name="movedown-method-of-the-win32_tsgatewayradiusserver-class"></a>Metodo MoveDown della classe \_ TSGatewayRADIUSServer Win32

Sposta questo Remote Authentication Dial-In User Service server RADIUS una posizione verso il basso nell'ordine di priorità. Questo metodo incrementa la **proprietà Priority** del server RADIUS corrente e decrementa la proprietà **Priority** del server RADIUS che segue il server RADIUS corrente.

## <a name="syntax"></a>Sintassi


```mof
uint32 MoveDown();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

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

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

