---
title: Proprietà IMsRdpClientTransportSettings GatewayDefaultUsageMethod
description: Il metodo di utilizzo predefinito Desktop remoto Gateway Desktop remoto.
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- Proprietà GatewayDefaultUsageMethod Servizi Desktop remoto
- Proprietà GatewayDefaultUsageMethod Servizi Desktop remoto, interfaccia IMsRdpClientTransportSettings
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto , proprietà GatewayDefaultUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayDefaultUsageMethod
- IMsRdpClientTransportSettings.get_GatewayDefaultUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6403f319eaa79b9d140a3d75f9dd4f7625eced916ee907755c017d3e58a1767f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607422"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a>Proprietà IMsRdpClientTransportSettings::GatewayDefaultUsageMethod

Il metodo di utilizzo predefinito Desktop remoto Gateway Desktop remoto.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore al metodo di utilizzo predefinito per Gateway Desktop remoto. Restituisce un'unione delle impostazioni utente impostate da [**\_ put GatewayUsageMethod()**](imsrdpclienttransportsettings-gatewayusagemethod.md)e le impostazioni di Criteri di gruppo. Se **\_ gatewayUsageMethod()** non ha impostato alcuna impostazione utente, **get \_ GatewayDefaultUsageMethod()** restituirà il valore predefinito **TSC \_ PROXY MODE \_ \_ DETECT**.

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings è definito come 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





