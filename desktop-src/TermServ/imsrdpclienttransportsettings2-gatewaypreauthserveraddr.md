---
title: Proprietà GatewayPreAuthServerAddr di IMsRdpClientTransportSettings2
description: Specifica o recupera l'indirizzo Web del server di pre-autenticazione, che viene utilizzato per la funzionalità di password monouso (OTP) di Desktop remoto Gateway.
ms.assetid: 14edad82-ab19-46fe-b878-d34298763c56
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayPreAuthServerAddr
- Servizi Desktop remoto proprietà GatewayPreAuthServerAddr, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewayPreAuthServerAddr
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
ms.openlocfilehash: 95d6fe2f397b0d445a6300d68a89b210debd449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400377"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthserveraddr-property"></a>Proprietà IMsRdpClientTransportSettings2:: GatewayPreAuthServerAddr

Specifica o recupera l'indirizzo Web del server di pre-autenticazione, che viene utilizzato per la funzionalità di password monouso (OTP) di Desktop remoto Gateway.

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

Indirizzo Web del server di pre-autenticazione; ad esempio, l'indirizzo Web del server Microsoft Internet Security and Acceleration (ISA). Specificare l'indirizzo Web utilizzando il formato "https://*hostname*. *NomeDominio*. com/*Websitename*"o" https://*nome host*. *NomeDominio*. com/*Websitename*".

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista con SP1<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                    |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 è definito come 67341688-D606-4C73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





