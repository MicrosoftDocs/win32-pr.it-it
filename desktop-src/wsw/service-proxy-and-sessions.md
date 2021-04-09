---
title: Proxy e sessioni del servizio
description: Il proxy del servizio ha comportamenti speciali per i binding di canale di sessione e non basati sulla sessione.
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- Servizi Web per proxy e sessioni del servizio per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8477a8cd03579e1d8cbfe4509f89890af8482
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047615"
---
# <a name="service-proxy-and-sessions"></a><span data-ttu-id="34857-106">Proxy e sessioni del servizio</span><span class="sxs-lookup"><span data-stu-id="34857-106">Service Proxy and Sessions</span></span>

<span data-ttu-id="34857-107">Il [proxy del servizio](service-proxy.md) ha comportamenti speciali per i binding di canale di sessione e non basati sulla sessione.</span><span class="sxs-lookup"><span data-stu-id="34857-107">The [service proxy](service-proxy.md) has special behaviors for session and non-session-based channel bindings.</span></span> <span data-ttu-id="34857-108">Il proxy del servizio fornisce la semantica basata sulla sessione se l'associazione di canale sottostante è basata sulla sessione.</span><span class="sxs-lookup"><span data-stu-id="34857-108">The service proxy provides session based semantics if the underlying channel binding is session based.</span></span> <span data-ttu-id="34857-109">In questo caso viene usato un solo canale per le chiamate di servizio.</span><span class="sxs-lookup"><span data-stu-id="34857-109">In this case a single channel is used to service calls.</span></span> <span data-ttu-id="34857-110">Tuttavia, se l'associazione di canale non è basata sulla sessione, il proxy del servizio crea un canale separato per ogni chiamata.</span><span class="sxs-lookup"><span data-stu-id="34857-110">However, if the channel binding is not session based, the service proxy creates a separate channel for each call.</span></span> <span data-ttu-id="34857-111">Si noti, tuttavia, che i canali non basati sulla sessione sono in pool e potrebbero essere riutilizzati.</span><span class="sxs-lookup"><span data-stu-id="34857-111">Note, though, that non-session-based channels are pooled and maybe reused.</span></span> <span data-ttu-id="34857-112">Quando si riutilizza un canale, il proxy del servizio mantiene il canale aperto se il canale sottostante non ha avuto errori o la chiamata su un canale ha causato l'errore del proxy del servizio nel canale.</span><span class="sxs-lookup"><span data-stu-id="34857-112">In reusing a channel, the service proxy keeps the channel open if the underlying channel has not faulted or the call on a channel has resulted in the service proxy's faulting the channel.</span></span> <span data-ttu-id="34857-113">Si noti che.</span><span class="sxs-lookup"><span data-stu-id="34857-113">Note that.</span></span> <span data-ttu-id="34857-114">tranne che in caso di errore, dopo l'apertura di un canale viene mantenuto aperto finché il proxy del servizio è aperto e chiuso solo quando il proxy del servizio viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="34857-114">except in the event of a fault, once a channel is opened it is kept open as long as the service proxy is open and is closed only when the service proxy is closed.</span></span>


<span data-ttu-id="34857-115">Se l'associazione di canale è basata sulla sessione e in caso di errori del canale sottostante, la macchina a Stati del proxy del servizio passerà allo stato di [**\_ \_ \_ \_ errore del proxy del servizio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .</span><span class="sxs-lookup"><span data-stu-id="34857-115">If the channel binding is session based and if the underlying channel faults, the service proxy state machine will transition into the [**WS\_SERVICE\_PROXY\_STATE\_FAULTED**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) state.</span></span> <span data-ttu-id="34857-116">Nel caso di un'associazione di canale non basata sulla sessione, un errore nel canale sottostante non determina la transizione del proxy allo stato **di \_ \_ \_ \_ errore del proxy del servizio WS** .</span><span class="sxs-lookup"><span data-stu-id="34857-116">In the case of non-session based channel binding, a fault in the underlying channel does not cause the proxy to transition into **WS\_SERVICE\_PROXY\_STATE\_FAULTED** state.</span></span>

<span data-ttu-id="34857-117">Per ulteriori informazioni sul proxy del servizio e sulla relativa relazione con lo stato, vedere l'argomento relativo al [proxy del servizio](service-proxy.md) .</span><span class="sxs-lookup"><span data-stu-id="34857-117">For more information on the service proxy and its relation to state, see the [Service Proxy](service-proxy.md) topic.</span></span> <span data-ttu-id="34857-118">Per esempi di diverse associazioni di canale, vedere gli esempi seguenti:</span><span class="sxs-lookup"><span data-stu-id="34857-118">For examples of different channel bindings see the following examples:</span></span>

-   <span data-ttu-id="34857-119">binding di canale non di sessione, [HttpCalculatorClientExample](httpcalculatorclientexample.md)</span><span class="sxs-lookup"><span data-stu-id="34857-119">non-session channel binding, [HttpCalculatorClientExample](httpcalculatorclientexample.md)</span></span>
-   <span data-ttu-id="34857-120">associazione di canale basata sulla sessione, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)</span><span class="sxs-lookup"><span data-stu-id="34857-120">session-based channel binding, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)</span></span>

 

 




