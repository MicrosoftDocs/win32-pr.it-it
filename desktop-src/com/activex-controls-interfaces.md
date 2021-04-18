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
# <a name="activex-controls-interfaces"></a>Interfacce di controlli ActiveX

Oltre ad altri meccanismi per la comunicazione tra il controllo e il client, la tecnologia dei controlli ActiveX specifica le interfacce [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) e [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) per la comunicazione del controllo client. È disponibile anche l'interfaccia [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) per i contenitori di controlli semplici.

Queste tre interfacce sono, tuttavia, specifiche dei controlli e non sono in genere utili all'esterno del contesto dei controlli. Queste interfacce sono definite come segue.

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

Alcuni controlli, come una casella di gruppo, sono semplicemente un semplice contenitore di altri controlli. In questi casi, il controllo semplice, denominato frame semplice, non deve implementare tutti i requisiti del contenitore. Può delegare la maggior parte delle chiamate di interfaccia dai controlli contenuti al contenitore che gestisce il frame semplice. Oltre alle chiamate di interfaccia, il frame semplice deve anche gestire i messaggi di Windows che potenzialmente provengono da controlli al suo interno. Per questo motivo, un contenitore fornisce [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) per consentire a tali controlli frame semplici di passare messaggi al contenitore. [**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) elabora innanzitutto il messaggio; [**Postmessagefilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) viene chiamato dopo che il frame semplice ha elaborato il messaggio stesso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli ActiveX](activex-controls.md)
</dt> </dl>

 

 




