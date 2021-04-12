---
title: Interfaccia IWMDRMNetTransmitter
description: L'interfaccia IWMDRMNetTransmitter fornisce i metodi necessari per usare Windows Media DRM per i dispositivi di rete come trasmettitore. Per ottenere un'istanza di questa interfaccia, chiamare IWMDRMProvider CreateObject. Passare IID \_ IWMDRMNetTransmitter come parametro riid.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- Formato Windows Media Interface IWMDRMNetTransmitter
- Interfaccia IWMDRMNetTransmitter-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a56db31bb7c03aa70aa136dcd07a8f41f1d9b84d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338302"
---
# <a name="iwmdrmnettransmitter-interface"></a>Interfaccia IWMDRMNetTransmitter

L'interfaccia **IWMDRMNetTransmitter** fornisce i metodi necessari per usare Windows Media DRM per i dispositivi di rete come trasmettitore.

Per ottenere un'istanza di questa interfaccia, chiamare [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md). Passare **IID \_ IWMDRMNetTransmitter** come parametro *riid* .

## <a name="members"></a>Membri

L'interfaccia **IWMDRMNetTransmitter** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMNetTransmitter** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMDRMNetTransmitter** dispone di questi metodi.



| Metodo                                                                        | Descrizione                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) | Genera un messaggio di risposta di licenza foglia.<br/>                                                       |
| [**GetRootLicenseResponse**](iwmdrmnettransmitter-getrootlicenseresponse.md) | Genera un messaggio di risposta della licenza radice<br/>                                                        |
| [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md)       | Elabora una richiesta di licenza inviata da un DRM di Microsoft Windows Media per i dispositivi di rete Receiver<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> <dt>

[**Interfaccia IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> </dl>

 

