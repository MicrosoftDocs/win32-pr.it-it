---
title: Interfaccia IMsRdpClientTransportSettings3
description: Definisce proprietà aggiuntive per il server Desktop remoto Gateway Desktop remoto. | Interfaccia IMsRdpClientTransportSettings3
ms.assetid: c0bdfe23-9a26-4feb-b9b7-e52f04f23aa1
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientTransportSettings3 Servizi Desktop remoto
- Interfaccia IMsRdpClientTransportSettings3 Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a7680e27b0d67c9273e4f47da4725c0acab6d173c560bb5b288a30a96931d7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606926"
---
# <a name="imsrdpclienttransportsettings3-interface"></a>Interfaccia IMsRdpClientTransportSettings3

Definisce proprietà aggiuntive per il server Desktop remoto Gateway Desktop remoto.

## <a name="members"></a>Membri

**L'interfaccia IMsRdpClientTransportSettings3** eredita da [**IMsRdpClientTransportSettings2.**](imsrdpclienttransportsettings2.md) **IMsRdpClientTransportSettings3** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Queste **proprietà sono disponibili nell'interfaccia IMsRdpClientTransportSettings3.**



| Proprietà                                                                                                           | Tipo di accesso           | Descrizione                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GatewayAuthCookieServerAddr**](imsrdpclienttransportsettings3-gatewayauthcookieserveraddr.md)<br/>       | Lettura/Scrittura<br/> | Indirizzo del server per l'autenticazione basata su cookie.<br/>                                                                                       |
| [**GatewayAuthLoginPage**](imsrdpclienttransportsettings3-gatewayauthloginpage.md)<br/>                     | Lettura/Scrittura<br/> | Indirizzo della pagina Web di accesso da usare per autenticare un utente.<br/>                                                                           |
| [**GatewayCredSourceCookie**](imsrdpclienttransportsettings3-gatewaycredsourcecookie.md)<br/>               | Lettura/Scrittura<br/> | Specifica se l'origine delle credenziali è basata su cookie.<br/>                                                                                       |
| [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/>         | Lettura/Scrittura<br/> | Cookie di autenticazione crittografato.<br/>                                                                                                      |
| [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)<br/> | Lettura/Scrittura<br/> | Dimensione, in caratteri, della [**proprietà GatewayEncryptedAuthCookie.**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                              |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                    |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings3 è definito come 3D5B21AC-748D-41DE-8F30-E15169586BD4<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





