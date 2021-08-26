---
title: Interfaccia IWMDRMNetReceiver
description: L'interfaccia IWMDRMNetReceiver fornisce i metodi necessari per usare Microsoft Windows Media DRM per dispositivi di rete come ricevitore. Per ottenere un'istanza di questa interfaccia, chiamare IWMDRMProvider CreateObject. Passare \_ IWMDRMNetReceiver IWMDRMNetReceiver come parametro riid.
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- Interfaccia IWMDRMNetReceiver windows Media Format
- Interfaccia IWMDRMNetReceiver windows Media Format , descritta
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cb917d7d229b81a6792461c506b2a6b50aaee2af3bd5f133e44273077924f86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930111"
---
# <a name="iwmdrmnetreceiver-interface"></a>Interfaccia IWMDRMNetReceiver

**L'interfaccia IWMDRMNetReceiver** fornisce i metodi necessari per usare Microsoft Windows Media DRM per dispositivi di rete come ricevitore.

Per ottenere un'istanza di questa interfaccia, chiamare [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md). Passare **\_ IWMDRMNetReceiver IWMDRMNetReceiver** come *parametro riid.*

## <a name="members"></a>Membri

**L'interfaccia IWMDRMNetReceiver** eredita da [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMNetReceiver** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IWMDRMNetReceiver.**



| Metodo                                                                               | Descrizione                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**GetLicenseChallenge**](iwmdrmnetreceiver-getlicensechallenge.md)                 | Genera una richiesta di licenza inviata al trasmettitore quando si richiede contenuto protetto.<br/>                     |
| [**GetRegistrationChallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)       | Genera una richiesta di registrazione inviata al trasmettitore quando il ricevitore esegue la registrazione o la riconvalida.<br/> |
| [**ProcessLicenseResponse**](iwmdrmnetreceiver-processlicenseresponse.md)           | Elabora la risposta di licenza inviata dal trasmettitore in risposta a una richiesta di licenza.<br/>                              |
| [**ProcessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md) | Elabora la risposta di registrazione inviata dal trasmettitore in risposta a una richiesta di registrazione.<br/>                    |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> <dt>

[**Interfaccia IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





