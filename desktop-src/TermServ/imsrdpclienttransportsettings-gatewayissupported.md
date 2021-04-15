---
title: Proprietà GatewayIsSupported di IMsRdpClientTransportSettings
description: Specifica se Desktop remoto Gateway Desktop remoto è supportato.
ms.assetid: 31edd35b-251d-404d-bec8-e082bb2427b3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayIsSupported
- Servizi Desktop remoto proprietà GatewayIsSupported, interfaccia IMsRdpClientTransportSettings
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto, proprietà GatewayIsSupported
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayIsSupported
- IMsRdpClientTransportSettings.get_GatewayIsSupported
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de79033c2ab9bae73aae4213e72a54590170a184
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400237"
---
# <a name="imsrdpclienttransportsettingsgatewayissupported-property"></a>Proprietà IMsRdpClientTransportSettings:: GatewayIsSupported

Specifica se Desktop remoto Gateway Desktop remoto è supportato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_GatewayIsSupported(
  [out] BOOL *pfProxyIsSupported
);
```



## <a name="property-value"></a>Valore proprietà

Specifica se Gateway Desktop remoto è supportato.

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

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

 

 





