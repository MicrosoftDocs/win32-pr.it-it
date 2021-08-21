---
title: Metodo MoveUp della classe Win32_TSGatewayRADIUSServer
description: Sposta questo Remote Authentication Dial-In User Service server RADIUS di una posizione verso l'alto nell'ordine di priorità.
ms.assetid: 060bb90d-72c0-4364-a44f-c6368434b174
ms.tgt_platform: multiple
keywords:
- Metodo MoveUp Servizi Desktop remoto
- Metodo MoveUp Servizi Desktop remoto , Win32_TSGatewayRADIUSServer classe
- Win32_TSGatewayRADIUSServer classe Servizi Desktop remoto , metodo MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2850c587a9e610fd1e2b935f9a5d8ca0cb60f5b17054249db082dd67c656ee5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118350657"
---
# <a name="moveup-method-of-the-win32_tsgatewayradiusserver-class"></a>Metodo MoveUp della classe \_ Win32 TSGatewayRADIUSServer

Sposta questo Remote Authentication Dial-In User Service server RADIUS di una posizione verso l'alto nell'ordine di priorità. Questo metodo decrementa la **proprietà Priority** del server RADIUS corrente e incrementa la proprietà **Priority** del server RADIUS che precede il server RADIUS corrente.

## <a name="syntax"></a>Sintassi


```mof
uint32 MoveUp();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

