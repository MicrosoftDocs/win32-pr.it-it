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
# <a name="registering-for-events"></a><span data-ttu-id="a5c26-103">Registrazione per gli eventi</span><span class="sxs-lookup"><span data-stu-id="a5c26-103">Registering for Events</span></span>

<span data-ttu-id="a5c26-104">Nell'esempio seguente viene usato il metodo Windows Image Acquisition (WIA) 1,0 [**IWiaDevMgr:: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) per eseguire la registrazione per la notifica quando un dispositivo Windows Image Acquisition (WIA) è connesso al sistema.</span><span class="sxs-lookup"><span data-stu-id="a5c26-104">The following example uses the Windows Image Acquisition (WIA) 1.0 [**IWiaDevMgr::RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) method to register for notification when any Windows Image Acquisition (WIA) device is connected to the system.</span></span> <span data-ttu-id="a5c26-105">Le applicazioni possono inoltre utilizzare WIA 1,0 [**IWiaDevMgr:: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) e WIA 1,0 [**IWiaDevMgr:: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) per la registrazione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="a5c26-105">Applications can also use WIA 1.0 [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) and WIA 1.0 [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) to register for events.</span></span> <span data-ttu-id="a5c26-106">Con Windows Vista e versioni successive, è possibile utilizzare i metodi Windows Image Acquisition (WIA) 2,0 [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2:: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)o [**IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) per la registrazione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="a5c26-106">With Windows Vista and later, you can use the Windows Image Acquisition (WIA) 2.0 [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md), or [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) methods to register for events.</span></span>

<span data-ttu-id="a5c26-107">Si presuppone che l'esempio venga preso da un'applicazione registrata come oggetto server out-of-process Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="a5c26-107">It is assumed that the example is taken from an application that is registered as a Component Object Model (COM) out-of-process server object.</span></span>

<span data-ttu-id="a5c26-108">La chiamata a [**IWiaDevMgr:: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (o [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) è la seguente:</span><span class="sxs-lookup"><span data-stu-id="a5c26-108">The call to [**IWiaDevMgr::RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (or [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) is as follows:</span></span>


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



<span data-ttu-id="a5c26-109">Nel codice precedente, **pWiaDevMgr** è un puntatore valido all'interfaccia [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)), il \_ \_ callback dell'evento di registrazione WIA \_ è una costante che specifica che la chiamata deve essere registrata per l'evento anziché annullare la registrazione per l'evento, il \_ dispositivo evento WIA \_ \_ connesso è una costante che specifica che l'applicazione deve essere registrata per ricevere una notifica ogni volta che un dispositivo è connesso al computer dell'utente. **pCLSID** è un puntatore al CLSID registrato dell'applicazione, **bstrName** è il nome dell'applicazione, **bstrDescription** è una descrizione di testo dell'applicazione e **bstrIcon** è il nome di un file di immagine da usare per l'icona per l'applicazione che registra per l'evento.</span><span class="sxs-lookup"><span data-stu-id="a5c26-109">In the previous code, **pWiaDevMgr** is a valid pointer to the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) interface, WIA\_REGISTER\_EVENT\_CALLBACK is a constant that specifies that this call is to register for the event as opposed to unregistering for the event, WIA\_EVENT\_DEVICE\_CONNECTED is a constant that specifies that the application is registering to be notified whenever a device is connected to the user's computer, **pCLSID** is a pointer to the registered CLSID of the application, **bstrName** is the name of the application, **bstrDescription** is a text description of the application, and **bstrIcon** is the name of an image file to be used for the icon for the application registering for the event.</span></span>

<span data-ttu-id="a5c26-110">L'applicazione deve quindi implementare il metodo [**IWiaEventCallback:: ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) , che viene chiamato ogni volta che si verifica un evento per il quale l'applicazione è registrata.</span><span class="sxs-lookup"><span data-stu-id="a5c26-110">The application must then implement the [**IWiaEventCallback::ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) method, which is called whenever an event occurs for which the application is registered.</span></span>

<span data-ttu-id="a5c26-111">Un'applicazione può usare il metodo [**IWiaItem:: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (o [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)) per enumerare le informazioni sugli eventi per cui è registrata.</span><span class="sxs-lookup"><span data-stu-id="a5c26-111">An application can use the [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (or [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)) method to enumerate the information about events for which it is registered.</span></span>

 

 



