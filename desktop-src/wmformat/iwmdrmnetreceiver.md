---
title: Interfaccia IWMDRMNetReceiver
description: L'interfaccia IWMDRMNetReceiver fornisce i metodi necessari per utilizzare DRM di Microsoft Windows Media per i dispositivi di rete come ricevitore. Per ottenere un'istanza di questa interfaccia, chiamare IWMDRMProvider CreateObject. Passare IID \_ IWMDRMNetReceiver come parametro riid.
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- Formato Windows Media Interface IWMDRMNetReceiver
- Interfaccia IWMDRMNetReceiver-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a85ae1525a81e97984e29a5dd28763d934dba2b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104398042"
---
# <a name="iwmdrmnetreceiver-interface"></a>Interfaccia IWMDRMNetReceiver

L'interfaccia **IWMDRMNetReceiver** fornisce i metodi necessari per utilizzare DRM di Microsoft Windows Media per i dispositivi di rete come ricevitore.

Per ottenere un'istanza di questa interfaccia, chiamare [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md). Passare **IID \_ IWMDRMNetReceiver** come parametro *riid* .

## <a name="members"></a>Membri

L'interfaccia **IWMDRMNetReceiver** eredita da [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMNetReceiver** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMDRMNetReceiver** dispone di questi metodi.



| Metodo                                                                               | Descrizione                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**GetLicenseChallenge**](iwmdrmnetreceiver-getlicensechallenge.md)                 | Genera un problema di licenza inviato al trasmettitore quando richiede contenuto protetto.<br/>                     |
| [**GetRegistrationChallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)       | Genera una richiesta di registrazione inviata al trasmettitore quando il ricevitore si registra o si riconvalida.<br/> |
| [**ProcessLicenseResponse**](iwmdrmnetreceiver-processlicenseresponse.md)           | Elabora la risposta di licenza inviata dalla trasmittente in risposta a una richiesta di licenza.<br/>                              |
| [**ProcessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md) | Elabora la risposta di registrazione inviata dal trasmettitore in risposta a una richiesta di registrazione.<br/>                    |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> <dt>

[**Interfaccia IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





