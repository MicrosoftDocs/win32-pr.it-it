---
description: "Nell'esempio seguente viene usato il metodo Windows Image Acquisition (WIA) 1,0 IWiaDevMgr:: RegisterEventCallbackCLSID per eseguire la registrazione per la notifica quando un dispositivo Windows Image Acquisition (WIA) è connesso al sistema."
ms.assetid: 1f2c7bc9-876a-4693-9439-52735e4b9d5f
title: Registrazione per gli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40fe29be23bda4a3094ff8bcf90ae1ca677e858d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129399"
---
# <a name="registering-for-events"></a>Registrazione per gli eventi

Nell'esempio seguente viene usato il metodo Windows Image Acquisition (WIA) 1,0 [**IWiaDevMgr:: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) per eseguire la registrazione per la notifica quando un dispositivo Windows Image Acquisition (WIA) è connesso al sistema. Le applicazioni possono inoltre utilizzare WIA 1,0 [**IWiaDevMgr:: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) e WIA 1,0 [**IWiaDevMgr:: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) per la registrazione degli eventi. Con Windows Vista e versioni successive, è possibile utilizzare i metodi Windows Image Acquisition (WIA) 2,0 [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2:: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)o [**IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) per la registrazione degli eventi.

Si presuppone che l'esempio venga preso da un'applicazione registrata come oggetto server out-of-process Component Object Model (COM).

La chiamata a [**IWiaDevMgr:: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (o [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) è la seguente:


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



Nel codice precedente, **pWiaDevMgr** è un puntatore valido all'interfaccia [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)), il \_ \_ callback dell'evento di registrazione WIA \_ è una costante che specifica che la chiamata deve essere registrata per l'evento anziché annullare la registrazione per l'evento, il \_ dispositivo evento WIA \_ \_ connesso è una costante che specifica che l'applicazione deve essere registrata per ricevere una notifica ogni volta che un dispositivo è connesso al computer dell'utente. **pCLSID** è un puntatore al CLSID registrato dell'applicazione, **bstrName** è il nome dell'applicazione, **bstrDescription** è una descrizione di testo dell'applicazione e **bstrIcon** è il nome di un file di immagine da usare per l'icona per l'applicazione che registra per l'evento.

L'applicazione deve quindi implementare il metodo [**IWiaEventCallback:: ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) , che viene chiamato ogni volta che si verifica un evento per il quale l'applicazione è registrata.

Un'applicazione può usare il metodo [**IWiaItem:: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (o [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)) per enumerare le informazioni sugli eventi per cui è registrata.

 

 



