---
title: Interfacce di controlli ActiveX
description: Interfacce di controlli ActiveX
ms.assetid: c4ca5696-c461-4d65-b2a8-c689c056dac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd7c4e0b726e9f330910bd468c237c72462fa21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298019"
---
# <a name="activex-controls-interfaces"></a><span data-ttu-id="e99fb-103">Interfacce di controlli ActiveX</span><span class="sxs-lookup"><span data-stu-id="e99fb-103">ActiveX Controls Interfaces</span></span>

<span data-ttu-id="e99fb-104">Oltre ad altri meccanismi per la comunicazione tra il controllo e il client, la tecnologia dei controlli ActiveX specifica le interfacce [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) e [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) per la comunicazione del controllo client.</span><span class="sxs-lookup"><span data-stu-id="e99fb-104">In addition to other mechanisms for communicating between the control and its client, ActiveX controls technology specifies the [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) and [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interfaces for client-control communication.</span></span> <span data-ttu-id="e99fb-105">È disponibile anche l'interfaccia [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) per i contenitori di controlli semplici.</span><span class="sxs-lookup"><span data-stu-id="e99fb-105">There is also the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface for simple control containers.</span></span>

<span data-ttu-id="e99fb-106">Queste tre interfacce sono, tuttavia, specifiche dei controlli e non sono in genere utili all'esterno del contesto dei controlli.</span><span class="sxs-lookup"><span data-stu-id="e99fb-106">These three interfaces are, however, specific to controls and are not generally useful outside the context of controls.</span></span> <span data-ttu-id="e99fb-107">Queste interfacce sono definite come segue.</span><span class="sxs-lookup"><span data-stu-id="e99fb-107">These interfaces are defined as follows.</span></span>

``` syntax
interface IOleControl : IUnknown 
  { 
    HRESULT GetControlInfo([out] CONTROLINFO *pCI); 
    HRESULT OnMnemonic([in] LPMSG pMsg); 
    HRESULT OnAmbientPropertyChange([in] DISPID dispID); 
    HRESULT FreezeEvents([in] BOOL bFreeze); 
  } 
 
interface IOleControlSite : IUnknown 
  { 
    HRESULT OnControlInfoChanged(void); 
    HRESULT LockInPlaceActive([in] BOOL fLock); 
    HRESULT GetExtendedControl([out] IDispatch **ppDisp); 
    HRESULT TransformCoords([in-out] POINTL *pptlHimetric, [in-out] POINTF *pptfContainer, [in] DWORD dwFlags); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg, [in] DWORD grfModifiers); 
    HRESULT OnFocus([in] BOOL fGotFocus); 
    HRESULT ShowPropertyFrame(void); 
  } 
 
interface ISimpleFrameSite : IUnknown 
  { 
    HRESULT PreMessageFilter([in] HWND hWnd, [in] UINT msg, [in] WPARAM wp, [in] LPARAM lp, 
        [out] LRESULT *plResult, [out] DWORD *pdwCookie); 
    HRESULT PostMessageFilter([in] HWND hWnd, [in] UINT msg, [in] WPARAM wp, [in] LPARAM lp, 
        [out] LRESULT *plResult, [in] DWORD dwCookie); 
  } 
 
```

<span data-ttu-id="e99fb-108">Alcuni controlli, come una casella di gruppo, sono semplicemente un semplice contenitore di altri controlli.</span><span class="sxs-lookup"><span data-stu-id="e99fb-108">Some controls, like a group box, are merely a simple container of other controls.</span></span> <span data-ttu-id="e99fb-109">In questi casi, il controllo semplice, denominato frame semplice, non deve implementare tutti i requisiti del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e99fb-109">In such cases, the simple control, called a simple frame, doesn't have to implement all the container requirements.</span></span> <span data-ttu-id="e99fb-110">Può delegare la maggior parte delle chiamate di interfaccia dai controlli contenuti al contenitore che gestisce il frame semplice.</span><span class="sxs-lookup"><span data-stu-id="e99fb-110">It can delegate most of the interface calls from its contained controls to the container that manages the simple frame.</span></span> <span data-ttu-id="e99fb-111">Oltre alle chiamate di interfaccia, il frame semplice deve anche gestire i messaggi di Windows che potenzialmente provengono da controlli al suo interno.</span><span class="sxs-lookup"><span data-stu-id="e99fb-111">Besides interface calls, the simple frame also has to deal with Windows messages that potentially come from controls within it.</span></span> <span data-ttu-id="e99fb-112">Per questo motivo, un contenitore fornisce [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) per consentire a tali controlli frame semplici di passare messaggi al contenitore.</span><span class="sxs-lookup"><span data-stu-id="e99fb-112">For this reason, a container supplies [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) to allow such simple frame controls to pass messages up to the container.</span></span> <span data-ttu-id="e99fb-113">[**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) elabora innanzitutto il messaggio; [**Postmessagefilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) viene chiamato dopo che il frame semplice ha elaborato il messaggio stesso.</span><span class="sxs-lookup"><span data-stu-id="e99fb-113">[**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) processes the message first; [**PostMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) is called after the simple frame has processed the message itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e99fb-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e99fb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e99fb-115">Controlli ActiveX</span><span class="sxs-lookup"><span data-stu-id="e99fb-115">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




