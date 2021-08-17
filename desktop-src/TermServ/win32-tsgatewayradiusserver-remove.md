---
title: Metodo Remove della classe Win32_TSGatewayRADIUSServer
description: Rimuove il server REMOTE AUTHENTICATION DIAL-IN USER SERVICE (RADIUS) corrente.
ms.assetid: 915f6d38-ba6a-4994-8bb9-bfddb9aa6ff8
ms.tgt_platform: multiple
keywords:
- Metodo Remove Servizi Desktop remoto
- Metodo Remove Servizi Desktop remoto , Win32_TSGatewayRADIUSServer interface
- Win32_TSGatewayRADIUSServer interfaccia Servizi Desktop remoto , metodo Remove
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Remove
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446a9ea6a9f2bdb4fada3fed38952988c0284b5bc4055503784c232255586407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126575"
---
# <a name="remove-method-of-the-win32_tsgatewayradiusserver-class"></a>Metodo Remove della classe \_ Win32 TSGatewayRADIUSServer

Rimuove il server REMOTE AUTHENTICATION DIAL-IN USER SERVICE (RADIUS) corrente.

## <a name="syntax"></a>Sintassi


```mof
uint32 Remove();
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

 

