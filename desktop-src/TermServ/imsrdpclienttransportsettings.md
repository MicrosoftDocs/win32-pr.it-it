---
title: Interfaccia IMsRdpClientTransportSettings
description: Gestisce le impostazioni di trasporto client per il server Gateway Desktop remoto di Desktop remoto. | Interfaccia IMsRdpClientTransportSettings
ms.assetid: d2573727-1dcc-4d4d-af5c-038e9467ba84
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec240d008ef2f9469fb67f4041cfb33c08383079
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321239"
---
# <a name="imsrdpclienttransportsettings-interface"></a>Interfaccia IMsRdpClientTransportSettings

Gestisce le impostazioni di trasporto client per il server Gateway Desktop remoto di Desktop remoto.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpClientTransportSettings** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsRdpClientTransportSettings** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpClientTransportSettings** ha queste proprietà.



| Proprietà                                                                                                          | Tipo di accesso           | Descrizione                                                 |
|:------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [**GatewayCredsSource**](imsrdpclienttransportsettings-gatewaycredssource.md)<br/>                         | Lettura/Scrittura<br/> | Metodo di autenticazione del server Gateway Desktop remoto.<br/>     |
| [**GatewayDefaultUsageMethod**](imsrdpclienttransportsettings-gatewaydefaultusagemethod.md)<br/>           | Sola lettura<br/>  | Metodo di utilizzo predefinito del Gateway Desktop remoto.<br/>             |
| [**GatewayHostname**](imsrdpclienttransportsettings-gatewayhostname.md)<br/>                               | Lettura/Scrittura<br/> | Nome host del server Gateway Desktop remoto.<br/>              |
| [**GatewayIsSupported**](imsrdpclienttransportsettings-gatewayissupported.md)<br/>                         | Sola lettura<br/>  | Indica se Gateway Desktop remoto è supportato.<br/>       |
| [**GatewayProfileUsageMethod**](imsrdpclienttransportsettings-gatewayprofileusagemethod.md)<br/>           | Lettura/Scrittura<br/> | Metodo di utilizzo del profilo Gateway Desktop remoto.<br/>             |
| [**GatewayUsageMethod**](imsrdpclienttransportsettings-gatewayusagemethod.md)<br/>                         | Lettura/Scrittura<br/> | Metodo di utilizzo del server Gateway Desktop remoto.<br/>              |
| [**GatewayUserSelectedCredsSource**](imsrdpclienttransportsettings-gatewayuserselectedcredssource.md)<br/> | Lettura/Scrittura<br/> | Origine della credenziale Gateway Desktop remoto specificata dall'utente.<br/> |



 

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

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Riferimento Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

