---
title: Proprietà GatewaySupportUrl di IMsRdpClientTransportSettings2
description: Specifica o recupera l'indirizzo Web del sito che fornisce supporto tecnico per il server Gateway Desktop remoto di Desktop remoto.
ms.assetid: e9c0f5ec-1b2f-4e09-8169-4316fd394443
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewaySupportUrl
- Servizi Desktop remoto proprietà GatewaySupportUrl, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewaySupportUrl
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewaySupportUrl
- IMsRdpClientTransportSettings2.get_GatewaySupportUrl
- IMsRdpClientTransportSettings2.put_GatewaySupportUrl
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4212dd03d5fb217753e14c2869973bda87476367
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400376"
---
# <a name="imsrdpclienttransportsettings2gatewaysupporturl-property"></a>Proprietà IMsRdpClientTransportSettings2:: GatewaySupportUrl

Specifica o recupera l'indirizzo Web del sito che fornisce supporto tecnico per il server Gateway Desktop remoto di Desktop remoto.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_GatewaySupportUrl(
  [in]  BSTR bstrProxySupportUrl
);

HRESULT get_GatewaySupportUrl(
  [out] BSTR *pbstrProxySupportUrl
);
```



## <a name="property-value"></a>Valore proprietà

Specifica o recupera l'indirizzo Web del sito che fornisce supporto tecnico per il server Gateway Desktop remoto.

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

 

 





