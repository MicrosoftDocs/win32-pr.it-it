---
title: Proprietà IMsRdpClientTransportSettings2 GatewayPreAuthServerAddr
description: Specifica o recupera l'indirizzo Web del server di pre-autenticazione, usato per la funzionalità OTP (One-Time Password) di Gateway Desktop remoto ( Gateway Desktop remoto).
ms.assetid: 14edad82-ab19-46fe-b878-d34298763c56
ms.tgt_platform: multiple
keywords:
- Proprietà GatewayPreAuthServerAddr Servizi Desktop remoto
- Proprietà GatewayPreAuthServerAddr Servizi Desktop remoto, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto proprietà , GatewayPreAuthServerAddr
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.get_GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.put_GatewayPreAuthServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89fa3df8431f829c0dd85cd3a448965e98b4e6d5e6285ae75d18c76257ddbb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000911"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthserveraddr-property"></a>Proprietà IMsRdpClientTransportSettings2::GatewayPreAuthServerAddr

Specifica o recupera l'indirizzo Web del server di pre-autenticazione, usato per la funzionalità OTP (One-Time Password) di Gateway Desktop remoto ( Gateway Desktop remoto).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_GatewayPreAuthServerAddr(
  [in]  BSTR bstrProxyPreAuthServerAddr
);

HRESULT get_GatewayPreAuthServerAddr(
  [out] BSTR *pbstrProxyPreAuthServerAddr
);
```



## <a name="property-value"></a>Valore proprietà

Indirizzo Web del server di pre-autenticazione. ad esempio l'indirizzo Web del server Microsoft Internet Security and Acceleration (ISA). Specificare l'indirizzo Web usando il formato "https://*HostName*. *DomainName*.com/*WebsiteName*" o "https://*HostName*. *DomainName*.com/*WebsiteName*".

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista con SP1<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                    |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 è definito come 67341688-D606-4c73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





