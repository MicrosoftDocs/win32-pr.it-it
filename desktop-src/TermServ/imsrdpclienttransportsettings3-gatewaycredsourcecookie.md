---
title: Proprietà GatewayCredSourceCookie di IMsRdpClientTransportSettings3
description: Specifica se l'origine delle credenziali è basata su cookie.
ms.assetid: 039459a3-7a83-444c-a0b4-46ef0dc5ddd0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayCredSourceCookie
- Servizi Desktop remoto proprietà GatewayCredSourceCookie, interfaccia IMsRdpClientTransportSettings3
- Interfaccia IMsRdpClientTransportSettings3 Servizi Desktop remoto, proprietà GatewayCredSourceCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.get_GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.put_GatewayCredSourceCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9547df10ce9f528a4b52c526c970a82d0bd098c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302576"
---
# <a name="imsrdpclienttransportsettings3gatewaycredsourcecookie-property"></a>Proprietà IMsRdpClientTransportSettings3:: GatewayCredSourceCookie

Specifica se l'origine delle credenziali è basata su cookie. Contiene uno se l'origine della credenziale è basata su cookie o zero in caso contrario.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_GatewayCredSourceCookie(
  [in]          ULONG ulProxyCredSourceCookie
);

HRESULT get_GatewayCredSourceCookie(
  [out, retval] ULONG *pulProxyCredSourceCookie
);
```



## <a name="property-value"></a>Valore proprietà

Valore **ULONG** che specifica se l'origine delle credenziali è basata su cookie.

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

 

 





