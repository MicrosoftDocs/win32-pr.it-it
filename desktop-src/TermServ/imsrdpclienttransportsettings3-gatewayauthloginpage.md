---
title: Proprietà GatewayAuthLoginPage di IMsRdpClientTransportSettings3
description: Indirizzo della pagina Web di accesso da usare per autenticare un utente.
ms.assetid: d7a5e0d8-353e-416d-a9e0-11ef5072f9ff
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayAuthLoginPage
- Servizi Desktop remoto proprietà GatewayAuthLoginPage, interfaccia IMsRdpClientTransportSettings3
- Interfaccia IMsRdpClientTransportSettings3 Servizi Desktop remoto, proprietà GatewayAuthLoginPage
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.get_GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.put_GatewayAuthLoginPage
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5be535dea0a89f1cf6e7c238029e53f38f58b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121378"
---
# <a name="imsrdpclienttransportsettings3gatewayauthloginpage-property"></a>Proprietà IMsRdpClientTransportSettings3:: GatewayAuthLoginPage

Indirizzo della pagina Web di accesso da usare per autenticare un utente.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_GatewayAuthLoginPage(
  [in]          BSTR bstrProxyAuthLoginPage
);

HRESULT get_GatewayAuthLoginPage(
  [out, retval] BSTR *pbstrProxyAuthLoginPage
);
```



## <a name="property-value"></a>Valore proprietà

Nuovo indirizzo della pagina Web di accesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





