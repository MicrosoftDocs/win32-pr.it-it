---
title: Interfaccia IWMDRMNetTransmitter
description: L'interfaccia IWMDRMNetTransmitter fornisce i metodi necessari per usare Windows DRM multimediale per i dispositivi di rete come trasmettitore. Per ottenere un'istanza di questa interfaccia, chiamare IWMDRMProvider CreateObject. Passare IID \_ IWMDRMNetTransmitter come parametro riid.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- Interfaccia IWMDRMNetTransmitter windows Media Format
- IWMDRMNetTransmitter interface windows Media Format , descritto
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7526ad349403abdb74f1e5684356af1b51b91f99b40e8e26a3b04932d4e5cf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027559"
---
# <a name="iwmdrmnettransmitter-interface"></a>Interfaccia IWMDRMNetTransmitter

**L'interfaccia IWMDRMNetTransmitter** fornisce i metodi necessari per usare Windows DRM multimediale per i dispositivi di rete come trasmettitore.

Per ottenere un'istanza di questa interfaccia, chiamare [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md). Passare **IID \_ IWMDRMNetTransmitter** come *parametro riid.*

## <a name="members"></a>Membri

**L'interfaccia IWMDRMNetTransmitter** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMNetTransmitter** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWMDRMNetTransmitter** include questi metodi.



| Metodo                                                                        | Descrizione                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) | Genera un messaggio di risposta di licenza foglia.<br/>                                                       |
| [**GetRootLicenseResponse**](iwmdrmnettransmitter-getrootlicenseresponse.md) | Genera un messaggio di risposta della licenza radice<br/>                                                        |
| [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md)       | Elabora una richiesta di licenza inviata da un ricevitore di Microsoft Windows Media DRM per dispositivi di rete<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> <dt>

[**Interfaccia IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> </dl>

 

