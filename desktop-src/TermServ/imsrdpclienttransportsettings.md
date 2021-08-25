---
title: Interfaccia IMsRdpClientTransportSettings
description: Gestisce le impostazioni di trasporto client per il server Desktop remoto Gateway Desktop remoto. | Interfaccia IMsRdpClientTransportSettings
ms.assetid: d2573727-1dcc-4d4d-af5c-038e9467ba84
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto , descritta
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
ms.openlocfilehash: edd2cbcdaba0a4324c4501339e972f8bb967f64716d1688cef7c3c38bb22b5b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771451"
---
# <a name="imsrdpclienttransportsettings-interface"></a>Interfaccia IMsRdpClientTransportSettings

Gestisce le impostazioni di trasporto client per il server Desktop remoto Gateway Desktop remoto.

## <a name="members"></a>Membri

**L'interfaccia IMsRdpClientTransportSettings** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IMsRdpClientTransportSettings** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **IMsRdpClientTransportSettings.**



| Proprietà                                                                                                          | Tipo di accesso           | Descrizione                                                 |
|:------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [**GatewayCredsSource**](imsrdpclienttransportsettings-gatewaycredssource.md)<br/>                         | Lettura/Scrittura<br/> | Metodo di autenticazione del server Gateway Desktop remoto.<br/>     |
| [**GatewayDefaultUsageMethod**](imsrdpclienttransportsettings-gatewaydefaultusagemethod.md)<br/>           | Sola lettura<br/>  | Metodo di utilizzo predefinito di Gateway Desktop remoto.<br/>             |
| [**GatewayHostname**](imsrdpclienttransportsettings-gatewayhostname.md)<br/>                               | Lettura/Scrittura<br/> | Nome host del server Gateway Desktop remoto.<br/>              |
| [**GatewayIsSupported**](imsrdpclienttransportsettings-gatewayissupported.md)<br/>                         | Sola lettura<br/>  | Indica se Gateway Desktop remoto è supportato.<br/>       |
| [**GatewayProfileUsageMethod**](imsrdpclienttransportsettings-gatewayprofileusagemethod.md)<br/>           | Lettura/Scrittura<br/> | Metodo di utilizzo del profilo di Gateway Desktop remoto.<br/>             |
| [**GatewayUsageMethod**](imsrdpclienttransportsettings-gatewayusagemethod.md)<br/>                         | Lettura/Scrittura<br/> | Metodo di utilizzo del server Gateway Desktop remoto.<br/>              |
| [**GatewayUserSelectedCredsSource**](imsrdpclienttransportsettings-gatewayuserselectedcredssource.md)<br/> | Lettura/Scrittura<br/> | Origine delle credenziali di Gateway Desktop remoto specificata dall'utente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IMSRdpClientTransportSettings IID è definito come \_ 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Idispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Connessione Web Desktop remoto riferimento](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

