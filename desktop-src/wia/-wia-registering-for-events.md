---
description: Nell'esempio seguente viene usato il metodo IWiaDevMgr::RegisterEventCallbackCLSID di Windows Image Acquisition (WIA) 1.0 per registrarsi per la notifica quando un dispositivo WIA (Windows Image Acquisition) è connesso al sistema.
ms.assetid: 1f2c7bc9-876a-4693-9439-52735e4b9d5f
title: Registrazione per gli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7a72614533ccc7c2f72bb4f2cf105107cc88ef8030cf306d31d6d9ffa5b4d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965550"
---
# <a name="registering-for-events"></a>Registrazione per gli eventi

L'esempio seguente usa il metodo [**IWiaDevMgr::RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) di Windows Image Acquisition (WIA) 1.0 per registrarsi per la notifica quando un dispositivo WIA (Windows Image Acquisition) è connesso al sistema. Le applicazioni possono anche usare WIA 1.0 [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) e WIA 1.0 [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) per la registrazione per gli eventi. Con Windows Vista e versioni successive, è possibile usare i metodi Windows [**IWiaDevMgr2::RegisterEventCallbackCLSID,**](-wia-iwiadevmgr2-registereventcallbackclsid.md) [**IWiaDevMgr2::RegisterEventCallbackMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)o [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) per la registrazione per gli eventi.

Si presuppone che l'esempio sia tratto da un'applicazione registrata come oggetto server out-of-process Component Object Model (COM).

La chiamata a [**IWiaDevMgr::RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (o [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) è la seguente:


```
    pWiaDevMgr->RegisterEventCallbackCLSID( WIA_REGISTER_EVENT_CALLBACK,
                                            NULL,
                                            WIA_EVENT_DEVICE_CONNECTED,
                                            pCLSID,
                                            bstrName,
                                            bstrDescription,
                                            bstrIcon
                                            );
```



Nel codice **precedente, pWiaDevMgr** è un puntatore valido all'interfaccia [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (o [**IWiaDevMgr2),**](-wia-iwiadevmgr2.md)WIA REGISTER EVENT CALLBACK è una costante che specifica che questa chiamata deve essere registrata per l'evento anziché annullare la registrazione per l'evento, WIA EVENT DEVICE CONNECTED è una costante che specifica che l'applicazione si sta registrando per ricevere una notifica ogni volta che un dispositivo è connesso al \_ computer \_ \_ \_ \_ \_ dell'utente, **pCLSID**    è un puntatore al CLSID registrato dell'applicazione, bstrName è il nome dell'applicazione, bstrDescription è una descrizione testuale dell'applicazione e bstrIcon è il nome di un file di immagine da usare per l'icona per l'applicazione che esegue la registrazione per l'evento.

L'applicazione deve quindi implementare il metodo [**IWiaEventCallback::ImageEventCallback,**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) che viene chiamato ogni volta che si verifica un evento per cui è registrata l'applicazione.

Un'applicazione può usare il metodo [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (o [**IWiaItem2::EnumRegisterEventInfo)**](-wia-iwiaitem2-enumregistereventinfo.md)per enumerare le informazioni sugli eventi per cui è registrata.

 

 



