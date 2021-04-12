---
title: Proprietà GatewayPreAuthRequirement di IMsRdpClientTransportSettings2
description: Specifica o recupera l'impostazione per verificare se la funzionalità di password monouso (OTP) del Gateway Desktop remoto (Gateway Desktop remoto) è abilitata.
ms.assetid: cc8f7ebb-16ba-45ed-ba66-de4a339946d0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayPreAuthRequirement
- Servizi Desktop remoto proprietà GatewayPreAuthRequirement, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewayPreAuthRequirement
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.get_GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.put_GatewayPreAuthRequirement
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058ca92237a4f9729f526030f5f8a836ce1c739c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518940"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthrequirement-property"></a>Proprietà IMsRdpClientTransportSettings2:: GatewayPreAuthRequirement

Specifica o recupera l'impostazione per verificare se la funzionalità di password monouso (OTP) del Gateway Desktop remoto (Gateway Desktop remoto) è abilitata.

Quando OTP è abilitato, **GatewayPreAuthRequirement** tenta di eseguire una query sul cookie OTP dall'archivio dei cookie Internet usando la proprietà [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) . In caso di esito positivo, **GatewayPreAuthRequirement** invia il cookie OTP al server del firewall, ad esempio Microsoft Internet Security and Acceleration \[ ISA \] Server, per la pre-autenticazione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_GatewayPreAuthRequirement(
  [in]  ULONG ulProxyPreAuthRequirement
);

HRESULT get_GatewayPreAuthRequirement(
  [out] ULONG *pulProxyPreAuthRequirement
);
```



## <a name="property-value"></a>Valore proprietà

Se impostato su 1, la funzionalità OTP è abilitata. Se è impostato su 0, la funzionalità OTP è disabilitata.

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

 

 





