---
title: Metodo MoveDown della classe Win32_TSGatewayRADIUSServer
description: Sposta questo server di Remote Authentication Dial-In User Service (RADIUS) una posizione verso il basso nell'ordine di priorità.
ms.assetid: 1b12d2a0-1463-4bd7-9b92-5df2ba799a8a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo MoveDown
- Metodo MoveDown Servizi Desktop remoto, classe Win32_TSGatewayRADIUSServer
- Classe Win32_TSGatewayRADIUSServer Servizi Desktop remoto, metodo MoveDown
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
ms.openlocfilehash: b652eb5e9cfc36f0d41e14d9953b295d35e660be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517698"
---
# <a name="movedown-method-of-the-win32_tsgatewayradiusserver-class"></a>Metodo MoveDown della \_ classe TSGatewayRADIUSServer Win32

Sposta questo server di Remote Authentication Dial-In User Service (RADIUS) una posizione verso il basso nell'ordine di priorità. Questo metodo incrementa la proprietà **Priority** del server RADIUS corrente e decrementa la proprietà **Priority** del server RADIUS che segue il server RADIUS corrente.

## <a name="syntax"></a>Sintassi


```mof
uint32 MoveDown();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

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

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

