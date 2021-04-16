---
title: Proprietà GatewayPassword di IMsRdpClientTransportSettings2
description: Specifica la password fornita da un utente per la connessione al server Gateway Desktop remoto di Desktop remoto.
ms.assetid: f29078e5-49ab-45a0-8d79-4b57d7c35e3a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayPassword
- Servizi Desktop remoto proprietà GatewayPassword, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewayPassword
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPassword
- IMsRdpClientTransportSettings2.put_GatewayPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d532f28023b7ff0eb3b8571e3875d0b63606535
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517487"
---
# <a name="imsrdpclienttransportsettings2gatewaypassword-property"></a>Proprietà IMsRdpClientTransportSettings2:: GatewayPassword

Specifica la password fornita da un utente per la connessione al server Gateway Desktop remoto di Desktop remoto.

Questa proprietà è di sola scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_GatewayPassword(
  [in] BSTR proxyPassword
);
```



## <a name="property-value"></a>Valore proprietà

Password fornita da un utente per la connessione al server Gateway Desktop remoto.

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

 

 





