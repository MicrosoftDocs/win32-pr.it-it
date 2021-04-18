---
title: Proprietà GatewayUserName di IMsRdpClientTransportSettings2
description: Specifica o Recupera il nome utente fornito al server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: eb5ed12f-e650-4abb-be20-bd5fae44e604
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayUserName
- Servizi Desktop remoto proprietà GatewayUserName, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewayUserName
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayUserName
- IMsRdpClientTransportSettings2.get_GatewayUserName
- IMsRdpClientTransportSettings2.put_GatewayUserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48244c49c942c917c58bfc2790b423981f17fe98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301215"
---
# <a name="imsrdpclienttransportsettings2gatewayusername-property"></a>Proprietà IMsRdpClientTransportSettings2:: GatewayUserName

Specifica o Recupera il nome utente fornito al server Gateway Desktop remoto (Gateway Desktop remoto).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_GatewayUserName(
  [in]  BSTR proxyUserName
);

HRESULT get_GatewayUserName(
  [out] BSTR *pProxyUserName
);
```



## <a name="property-value"></a>Valore proprietà

Nome utente fornito per la connessione al server Gateway Desktop remoto.

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

 

 





