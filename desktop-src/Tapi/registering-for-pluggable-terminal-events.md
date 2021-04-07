---
description: Il processo di registrazione dell'evento viene eseguito quando il terminale viene selezionato da un flusso.
ms.assetid: 03854b38-4dba-480e-b931-34299d04c551
title: Registrazione per eventi Terminal collegabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42bf75cfd0d7e6bd4d8a2520335c374cce28c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885826"
---
# <a name="registering-for-pluggable-terminal-events"></a><span data-ttu-id="aadfe-103">Registrazione per eventi Terminal collegabili</span><span class="sxs-lookup"><span data-stu-id="aadfe-103">Registering for Pluggable Terminal Events</span></span>

<span data-ttu-id="aadfe-104">Il processo di registrazione dell'evento viene eseguito quando il terminale viene selezionato da un flusso.</span><span class="sxs-lookup"><span data-stu-id="aadfe-104">The event registration process take place when the terminal is selected by a stream.</span></span> <span data-ttu-id="aadfe-105">Nell'implementazione dell'applicazione terminal del metodo [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) , è possibile usare l'interfaccia [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) del terminale collegato al flusso e chiamare **QueryInterface** per trovare [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).</span><span class="sxs-lookup"><span data-stu-id="aadfe-105">In the terminal application's implementation of the [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) method, we can use the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface of the terminal that was attached to the stream, and call **QueryInterface** to find [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).</span></span>

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

<span data-ttu-id="aadfe-106">Se la chiamata **QueryInterface** ha esito positivo, è possibile chiamare il metodo [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) .</span><span class="sxs-lookup"><span data-stu-id="aadfe-106">If the **QueryInterface** call succeeds, we can call the [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) method.</span></span> <span data-ttu-id="aadfe-107">A questo scopo, è necessario creare un oggetto che implementi l'interfaccia [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) .</span><span class="sxs-lookup"><span data-stu-id="aadfe-107">For this purpose, we should create an object that implements the [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) interface.</span></span> <span data-ttu-id="aadfe-108">Questa interfaccia viene passata come parametro del metodo **RegisterSink** .</span><span class="sxs-lookup"><span data-stu-id="aadfe-108">We pass this interface as a parameter of the **RegisterSink** method.</span></span>

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

<span data-ttu-id="aadfe-109">Il terminale che implementa la chiamata [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) archivia l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="aadfe-109">The terminal that implements the [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) call will store the interface.</span></span> <span data-ttu-id="aadfe-110">Il puntatore verrà usato quando il terminale genererà un evento.</span><span class="sxs-lookup"><span data-stu-id="aadfe-110">The pointer will be used when the terminal will fire an event.</span></span>

<span data-ttu-id="aadfe-111">Il sink di evento può essere annullato tramite [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).</span><span class="sxs-lookup"><span data-stu-id="aadfe-111">The event sink can be unregistered using [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).</span></span>

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
