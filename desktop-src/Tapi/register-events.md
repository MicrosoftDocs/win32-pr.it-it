---
description: Negli esempi di codice seguenti viene illustrata l'implementazione di un semplice gestore eventi, la registrazione dell'interfaccia evento TAPI principale, l'impostazione del filtro eventi e la registrazione per le notifiche di chiamata.
ms.assetid: e7662a26-d7b2-4bff-aa72-e38b58bc15df
title: Registra eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0a554c2e1ea5c226aa4a3c432f3430a30a978e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319872"
---
# <a name="register-events"></a>Registra eventi

Negli esempi di codice seguenti viene illustrata l'implementazione di un semplice gestore eventi, la registrazione dell'interfaccia evento TAPI principale, l'impostazione del filtro eventi e la registrazione per le notifiche di chiamata.

Il gestore eventi illustrato è un esempio anziché un requisito. L'obiettivo principale è garantire che il thread che riceve gli eventi esegue un'elaborazione minima prima di passare il lavoro a un altro thread. Ciò impedisce al gestore eventi di diventare un problema di prestazioni in situazioni di carico elevato degli eventi.

Prima di usare questo esempio di codice, è necessario eseguire le operazioni in [Initialize TAPI](initialize-tapi.md) e [selezionare un indirizzo](select-an-address.md).

> [!Note]  
> Questo esempio non include il controllo degli errori e le versioni appropriate per il codice di produzione.

 

``` syntax
//
// Example 1: Implement a simple event handler.
//
HRESULT STDMETHODCALLTYPE
CTAPIEventNotification::Event(
    TAPI_EVENT  TapiEvent,
    IDispatch * pEvent
    )
{
    // AddRef the event so it does not go away.
    pEvent->AddRef();

    // Post a message to our own UI thread.
    BOOL bMessage;
    bMessage = PostMessage( 
                           ghDlg,
                           WM_PRIVATETAPIEVENT,
                           (WPARAM) TapiEvent,
                           (LPARAM) pEvent
                           );
    // If (bMessage == 0) process the error here. 
    return S_OK;
}
```

``` syntax
//
// Example 2: Register the event interface.
//
long                         gulAdvise;  // Globally declared
IConnectionPointContainer   * pCPC;
IConnectionPoint            * pCP;
IUnknown                    * pUnk;

// Get the connection point container interface pointer from the TAPI object.
hr = gpTapi->QueryInterface(
      IID_IConnectionPointContainer,
      (void **)&pCPC
);
// If ( hr != S_OK O) process the error here. 

// Get the ITTAPIEventNotification interface pointer from the container.
hr = pCPC->FindConnectionPoint(
      IID_ITTAPIEventNotification,
      &pCP
     );
// If ( hr != S_OK O) process the error here. 

pCPC->Release();

// Create a private event notification object.
CTAPIEventNotification* pTapiEventNotification = new CTAPIEventNotification;

hr = pTapiEventNotification->QueryInterface(
      IID_IUnknown,
      (void **)&pUnk
     );
// If ( hr != S_OK O) process the error here. 

// Call the advise method to give TAPI the IUnknown pointer for the event handler.
hr = pCP->Advise(
      pUnk,
      (ULONG *)&gulAdvise
     );
// If ( hr != S_OK O) process the error here. 

pCP->Release();
```

``` syntax
//
// Example 3: Set the event filter.
//
// Assume we are interested only in call-related events.
hr = gpTapi->put_EventFilter(
    TE_CALLNOTIFICATION | TE_CALLSTATE | TE_CALLMEDIA
    );
// If ( hr != S_OK O) process the error here. 
```

``` syntax
//
// Example 4: Register an address with TAPI
// for call notifications. Assume we are interested
// in video and audio calls, and that pAddress
// is a pointer to the ITAddress interface of
// an address that can handle both media types.

long glRegister; // Globally declared

hr = gpTapi->RegisterCallNotifications(
      pAddress,
      VARIANT_TRUE,   // monitor privileges
      VARIANT_TRUE,   // owner privileges
      TAPIMEDIATYPE_AUDIO|TAPIMEDIATYPE_VIDEO,
      gulAdvise,      // As returned by Advise
      &glRegister
      );
// If ( hr != S_OK O) process the error here.
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[**\_evento TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter)
</dt> <dt>

[\_Costanti TAPIMEDIATYPE](tapimediatype--constants.md)
</dt> <dt>

[**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)
</dt> </dl>

 

 



