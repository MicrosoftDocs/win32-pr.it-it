---
title: Proprietà GatewayCredSharing di IMsRdpClientTransportSettings2
description: Specifica o recupera l'impostazione per verificare se la funzionalità di condivisione delle credenziali del gateway di Desktop remoto (Gateway Desktop remoto) è abilitata.
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayCredSharing
- Servizi Desktop remoto proprietà GatewayCredSharing, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewayCredSharing
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayCredSharing
- IMsRdpClientTransportSettings2.get_GatewayCredSharing
- IMsRdpClientTransportSettings2.put_GatewayCredSharing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329e425631b674e050f246c4105115bd4326be3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475628"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a>Proprietà IMsRdpClientTransportSettings2:: GatewayCredSharing

Specifica o recupera l'impostazione per verificare se la funzionalità di condivisione delle credenziali del gateway di Desktop remoto (Gateway Desktop remoto) è abilitata. Quando la funzionalità è abilitata, il controllo ActiveX Desktop remoto tenta di utilizzare le stesse credenziali per l'autenticazione al server di host sessione Desktop remoto (host sessione Desktop remoto) e al server Gateway Desktop remoto.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_GatewayCredSharing(
  [in]  ULONG ulProxyCredSharing
);

HRESULT get_GatewayCredSharing(
  [out] ULONG *pulProxyCredSharing
);
```



## <a name="property-value"></a>Valore proprietà

Se impostato su uno, la condivisione delle credenziali è abilitata. Se è impostato su zero, la condivisione delle credenziali è disabilitata.

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="remarks"></a>Commenti

Questa proprietà viene utilizzata dal controllo ActiveX per implementare una singola richiesta di condivisione delle credenziali tra il server Host sessione Desktop remoto e il server Gateway Desktop remoto. La condivisione delle credenziali non supporta la condivisione delle password basata sul Web con [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) o [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md).

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

 

 





