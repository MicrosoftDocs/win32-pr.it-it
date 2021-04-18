---
title: Proprietà GatewayDefaultUsageMethod di IMsRdpClientTransportSettings
description: Metodo di utilizzo predefinito per Desktop remoto Gateway (Gateway Desktop remoto).
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayDefaultUsageMethod
- Servizi Desktop remoto proprietà GatewayDefaultUsageMethod, interfaccia IMsRdpClientTransportSettings
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto, proprietà GatewayDefaultUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayDefaultUsageMethod
- IMsRdpClientTransportSettings.get_GatewayDefaultUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8417da30f9a692e6e233174a33f4b03682a5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301219"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a>Proprietà IMsRdpClientTransportSettings:: GatewayDefaultUsageMethod

Metodo di utilizzo predefinito per Desktop remoto Gateway (Gateway Desktop remoto).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore al metodo di utilizzo predefinito per Gateway Desktop remoto. Restituisce un'Unione delle impostazioni utente impostate mediante [**put \_ GatewayUsageMethod ()**](imsrdpclienttransportsettings-gatewayusagemethod.md)e le impostazioni di criteri di gruppo. Se non sono state impostate impostazioni utente mediante **put \_ GatewayUsageMethod ()**, **get \_ GatewayDefaultUsageMethod ()** restituirà il valore predefinito **della \_ modalità proxy TSC \_ \_ Detect**.

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

 

 





