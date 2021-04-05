---
title: Interfaccia IMsRdpClientTransportSettings3
description: Definisce proprietà aggiuntive per il server Gateway Desktop remoto di Desktop remoto. | Interfaccia IMsRdpClientTransportSettings3
ms.assetid: c0bdfe23-9a26-4feb-b9b7-e52f04f23aa1
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientTransportSettings3 Servizi Desktop remoto
- Interfaccia IMsRdpClientTransportSettings3 Servizi Desktop remoto, descritta
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
ms.openlocfilehash: e7498db4b39a4ad0e89761cbec439895e4e9a152
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886105"
---
# <a name="imsrdpclienttransportsettings3-interface"></a>Interfaccia IMsRdpClientTransportSettings3

Definisce proprietà aggiuntive per il server Gateway Desktop remoto di Desktop remoto.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpClientTransportSettings3** eredita da [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md). **IMsRdpClientTransportSettings3** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpClientTransportSettings3** ha queste proprietà.



| Proprietà                                                                                                           | Tipo di accesso           | Descrizione                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GatewayAuthCookieServerAddr**](imsrdpclienttransportsettings3-gatewayauthcookieserveraddr.md)<br/>       | Lettura/Scrittura<br/> | Indirizzo del server per l'autenticazione basata su cookie.<br/>                                                                                       |
| [**GatewayAuthLoginPage**](imsrdpclienttransportsettings3-gatewayauthloginpage.md)<br/>                     | Lettura/Scrittura<br/> | Indirizzo della pagina Web di accesso da usare per autenticare un utente.<br/>                                                                           |
| [**GatewayCredSourceCookie**](imsrdpclienttransportsettings3-gatewaycredsourcecookie.md)<br/>               | Lettura/Scrittura<br/> | Specifica se l'origine delle credenziali è basata su cookie.<br/>                                                                                       |
| [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/>         | Lettura/Scrittura<br/> | Cookie di autenticazione crittografato.<br/>                                                                                                      |
| [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)<br/> | Lettura/Scrittura<br/> | Dimensione, in caratteri, della proprietà [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) .<br/> |



 

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

 

 





