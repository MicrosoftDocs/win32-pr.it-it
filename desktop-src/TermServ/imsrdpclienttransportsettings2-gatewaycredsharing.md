---
title: Proprietà IMsRdpClientTransportSettings2 GatewayCredSharing
description: Specifica o recupera l'impostazione per indicare se la funzionalità di condivisione delle credenziali Desktop remoto Gateway desktop remoto è abilitata.
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- Proprietà GatewayCredSharing Servizi Desktop remoto
- Proprietà GatewayCredSharing Servizi Desktop remoto, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto , proprietà GatewayCredSharing
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
ms.openlocfilehash: d6d489678006e842a6da82f5d2f9489f84a9a20fd70bfe8f18018aaa6d412c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974651"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a>Proprietà IMsRdpClientTransportSettings2::GatewayCredSharing

Specifica o recupera l'impostazione per indicare se la funzionalità di condivisione delle credenziali Desktop remoto Gateway desktop remoto è abilitata. Quando la funzionalità è abilitata, il controllo Desktop remoto ActiveX tenta di usare le stesse credenziali per l'autenticazione al server Host sessione Desktop remoto (Host sessione Desktop remoto) e al server Gateway Desktop remoto.

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

Se impostato su uno, la condivisione delle credenziali è abilitata. Se impostato su zero, la condivisione delle credenziali è disabilitata.

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

Questa proprietà viene usata dal controllo ActiveX per implementare una singola richiesta di condivisione delle credenziali tra il server Host sessione Desktop remoto e il server Gateway Desktop remoto. La condivisione delle credenziali non supporta la condivisione delle password basata sul [**Web con GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) [**o ClearTextPassword.**](imstscnonscriptable-cleartextpassword.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista con SP1<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                    |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 è definito come 67341688-D606-4c73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





