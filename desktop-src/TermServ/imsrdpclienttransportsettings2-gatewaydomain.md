---
title: Proprietà GatewayDomain di IMsRdpClientTransportSettings2
description: Specifica o Recupera il nome di dominio di un utente fornito al server gateway di Desktop remoto (Gateway Desktop remoto).
ms.assetid: 792ff7c6-afeb-4a2a-86b4-7722513a08e0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayDomain
- Servizi Desktop remoto proprietà GatewayDomain, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewayDomain
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayDomain
- IMsRdpClientTransportSettings2.get_GatewayDomain
- IMsRdpClientTransportSettings2.put_GatewayDomain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088780fbbaa4ab86fc416a3e9aa353920cc25e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400378"
---
# <a name="imsrdpclienttransportsettings2gatewaydomain-property"></a>Proprietà IMsRdpClientTransportSettings2:: GatewayDomain

Specifica o Recupera il nome di dominio di un utente fornito al server gateway di Desktop remoto (Gateway Desktop remoto).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_GatewayDomain(
  [in]  BSTR proxyDomain
);

HRESULT get_GatewayDomain(
  [out] BSTR *pProxyDomain
);
```



## <a name="property-value"></a>Valore proprietà

Nome di dominio fornito per la connessione al server Gateway Desktop remoto.

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

 

 





