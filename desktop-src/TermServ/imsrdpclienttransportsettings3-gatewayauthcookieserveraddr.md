---
title: Proprietà IMsRdpClientTransportSettings3 GatewayAuthCookieServerAddr
description: Indirizzo del server per l'autenticazione basata su cookie.
ms.assetid: e00480cd-2133-42ff-8447-6c4234b56bf9
ms.tgt_platform: multiple
keywords:
- Proprietà GatewayAuthCookieServerAddr Servizi Desktop remoto
- Proprietà GatewayAuthCookieServerAddr Servizi Desktop remoto , interfaccia IMsRdpClientTransportSettings3
- Interfaccia IMsRdpClientTransportSettings3 Servizi Desktop remoto proprietà , GatewayAuthCookieServerAddr
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.get_GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.put_GatewayAuthCookieServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 330a1ddb15d548988c23f8140ce848f7f68be5d1deb17fc51bd88eed23b9eec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000921"
---
# <a name="imsrdpclienttransportsettings3gatewayauthcookieserveraddr-property"></a>Proprietà IMsRdpClientTransportSettings3::GatewayAuthCookieServerAddr

Indirizzo del server per l'autenticazione basata su cookie.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_GatewayAuthCookieServerAddr(
  [in]          BSTR bstrProxyAuthCookieServerAddr
);

HRESULT get_GatewayAuthCookieServerAddr(
  [out, retval] BSTR *pbstrProxyAuthCookieServerAddr
);
```



## <a name="property-value"></a>Valore proprietà

Nuovo indirizzo del server per l'autenticazione basata su cookie.

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

 

 





