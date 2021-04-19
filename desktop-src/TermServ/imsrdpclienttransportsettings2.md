---
title: Interfaccia IMsRdpClientTransportSettings2
description: Gestisce le impostazioni di trasporto client per il server Gateway Desktop remoto di Desktop remoto. | Interfaccia IMsRdpClientTransportSettings2
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f2f4887c6a4f55f3b9c97c389e9afd702d2ffab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321324"
---
# <a name="imsrdpclienttransportsettings2-interface"></a>Interfaccia IMsRdpClientTransportSettings2

Gestisce le impostazioni di trasporto client per il server Gateway Desktop remoto di Desktop remoto.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpClientTransportSettings2** eredita da [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md). **IMsRdpClientTransportSettings2** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpClientTransportSettings2** ha queste proprietà.



| Proprietà                                                                                                    | Tipo di accesso           | Descrizione                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [**GatewayCredSharing**](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | Lettura/Scrittura<br/> | Indica se la funzionalità Single Sign-On per Gateway Desktop remoto è abilitata.<br/>                |
| [**GatewayDomain**](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | Lettura/Scrittura<br/> | Nome di dominio fornito da un utente per la connessione al server Gateway Desktop remoto.<br/>              |
| [**GatewayEncryptedOtpCookie**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | Lettura/Scrittura<br/> | Cookie OTP crittografato.<br/>                                                              |
| [**GatewayEncryptedOtpCookieSize**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | Lettura/Scrittura<br/> | Dimensione, in byte, del cookie OTP crittografato.<br/>                                       |
| [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | Sola scrittura<br/> | Password fornita da un utente per la connessione al server Gateway Desktop remoto.<br/>                 |
| [**GatewayPreAuthRequirement**](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | Lettura/Scrittura<br/> | Indica se la funzionalità di password monouso di Gateway Desktop remoto (OTP) è abilitata.<br/>           |
| [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | Lettura/Scrittura<br/> | Indirizzo Web del server di pre-autenticazione.<br/>                                      |
| [**GatewaySupportUrl**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | Lettura/Scrittura<br/> | Indirizzo Web del sito che fornisce supporto tecnico per il server Gateway Desktop remoto.<br/> |
| [**GatewayUsername**](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | Lettura/Scrittura<br/> | Nome utente fornito da un utente per la connessione al server Gateway Desktop remoto.<br/>                |



 

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
</dt> </dl>

 

 





