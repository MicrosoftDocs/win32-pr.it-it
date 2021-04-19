---
title: Proxy
description: Un proxy risiede nello spazio degli indirizzi del processo chiamante e funge da surrogato per l'oggetto remoto.
ms.assetid: 6c82f655-ac46-4ed9-992b-0387b324a8f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11257dd060f51bef118a4afc0cc35acf995c111
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "106320187"
---
# <a name="proxy"></a><span data-ttu-id="c73fe-103">Proxy</span><span class="sxs-lookup"><span data-stu-id="c73fe-103">Proxy</span></span>

<span data-ttu-id="c73fe-104">Un proxy risiede nello spazio degli indirizzi del processo chiamante e funge da surrogato per l'oggetto remoto.</span><span class="sxs-lookup"><span data-stu-id="c73fe-104">A proxy resides in the address space of the calling process and acts as a surrogate for the remote object.</span></span> <span data-ttu-id="c73fe-105">Dal punto di vista dell'oggetto chiamante, il proxy è l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c73fe-105">From the perspective of the calling object, the proxy is the object.</span></span> <span data-ttu-id="c73fe-106">In genere, il ruolo del proxy consiste nel creare un pacchetto dei parametri di interfaccia per le chiamate ai metodi nelle interfacce degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="c73fe-106">Typically, the proxy's role is to package the interface parameters for calls to methods in its object interfaces.</span></span> <span data-ttu-id="c73fe-107">Il proxy inserisce i parametri in un buffer dei messaggi e passa il buffer sul canale, che gestisce il trasporto tra i processi.</span><span class="sxs-lookup"><span data-stu-id="c73fe-107">The proxy packages the parameters into a message buffer and passes the buffer onto the channel, which handles the transport between processes.</span></span> <span data-ttu-id="c73fe-108">Il proxy viene implementato come oggetto aggregato o composito.</span><span class="sxs-lookup"><span data-stu-id="c73fe-108">The proxy is implemented as an aggregate, or composite, object.</span></span> <span data-ttu-id="c73fe-109">Contiene una parte di gestione fornita dal sistema denominata Proxy Manager e uno o più componenti specifici dell'interfaccia chiamati proxy di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c73fe-109">It contains a system-provided, manager piece called the proxy manager and one or more interface-specific components called interface proxies.</span></span> <span data-ttu-id="c73fe-110">Il numero di proxy di interfaccia è uguale al numero di interfacce oggetto esposte a quel particolare client.</span><span class="sxs-lookup"><span data-stu-id="c73fe-110">The number of interface proxies equals the number of object interfaces that have been exposed to that particular client.</span></span> <span data-ttu-id="c73fe-111">Per il client che rispetta il modello a oggetti del componente, il proxy sembra essere l'oggetto reale.</span><span class="sxs-lookup"><span data-stu-id="c73fe-111">To the client complying with the component object model, the proxy appears to be the real object.</span></span>

> [!Note]  
> <span data-ttu-id="c73fe-112">Con il marshalling personalizzato, il proxy può essere implementato in modo analogo o può comunicare direttamente con l'oggetto senza usare uno stub.</span><span class="sxs-lookup"><span data-stu-id="c73fe-112">With custom marshaling, the proxy can be implemented similarly or it can communicate directly with the object without using a stub.</span></span>

 

<span data-ttu-id="c73fe-113">Ogni proxy di interfaccia è un oggetto Component che implementa il codice di marshalling per una delle interfacce dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c73fe-113">Each interface proxy is a component object that implements the marshaling code for one of the object's interfaces.</span></span> <span data-ttu-id="c73fe-114">Il proxy rappresenta l'oggetto per il quale viene fornito il codice di marshalling.</span><span class="sxs-lookup"><span data-stu-id="c73fe-114">The proxy represents the object for which it provides marshaling code.</span></span> <span data-ttu-id="c73fe-115">Ogni proxy implementa anche l'interfaccia [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) .</span><span class="sxs-lookup"><span data-stu-id="c73fe-115">Each proxy also implements the [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) interface.</span></span> <span data-ttu-id="c73fe-116">Sebbene l'interfaccia oggetto rappresentata dal proxy sia pubblica, l'implementazione di **IRpcProxyBuffer** è privata e viene utilizzata internamente all'interno del proxy.</span><span class="sxs-lookup"><span data-stu-id="c73fe-116">Although the object interface represented by the proxy is public, the **IRpcProxyBuffer** implementation is private and is used internally within the proxy.</span></span> <span data-ttu-id="c73fe-117">Gestione proxy tiene traccia dei proxy di interfaccia e contiene anche l'implementazione pubblica dell'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) di controllo per l'aggregazione.</span><span class="sxs-lookup"><span data-stu-id="c73fe-117">The proxy manager keeps track of the interface proxies and also contains the public implementation of the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface for the aggregate.</span></span> <span data-ttu-id="c73fe-118">Ogni proxy di interfaccia può esistere in una DLL separata che viene caricata quando l'interfaccia supportata viene materializzata nel client.</span><span class="sxs-lookup"><span data-stu-id="c73fe-118">Each interface proxy can exist in a separate DLL that is loaded when the interface it supports is materialized to the client.</span></span>

## <a name="structure-of-the-proxy"></a><span data-ttu-id="c73fe-119">Struttura del proxy</span><span class="sxs-lookup"><span data-stu-id="c73fe-119">Structure of the Proxy</span></span>

<span data-ttu-id="c73fe-120">Il diagramma seguente illustra la struttura di un proxy che supporta il marshalling standard di parametri appartenenti a due interfacce: IA1 e IA2.</span><span class="sxs-lookup"><span data-stu-id="c73fe-120">The following diagram shows the structure of a proxy that supports the standard marshaling of parameters belonging to two interfaces: IA1 and IA2.</span></span> <span data-ttu-id="c73fe-121">Ogni proxy di interfaccia implementa [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) per la comunicazione interna tra le parti aggregate.</span><span class="sxs-lookup"><span data-stu-id="c73fe-121">Each interface proxy implements [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) for internal communication between the aggregate pieces.</span></span> <span data-ttu-id="c73fe-122">Quando il proxy è pronto a passare i parametri di cui è stato effettuato il marshalling attraverso il limite del processo, chiama i metodi nell'interfaccia [**Metodo IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) , implementata dal canale.</span><span class="sxs-lookup"><span data-stu-id="c73fe-122">When the proxy is ready to pass its marshaled parameters across the process boundary, it calls methods in the [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) interface, which is implemented by the channel.</span></span> <span data-ttu-id="c73fe-123">Il canale, a sua volta, trasmette la chiamata alla libreria di runtime RPC per poter raggiungere la destinazione nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c73fe-123">The channel in turn forwards the call to the RPC run-time library so that it can reach its destination in the object.</span></span>

![Diagramma che mostra la struttura del proxy.](images/4432d8d3-dfab-4635-90f8-408aecf70134.png)

## <a name="related-topics"></a><span data-ttu-id="c73fe-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c73fe-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c73fe-126">Channel</span><span class="sxs-lookup"><span data-stu-id="c73fe-126">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="c73fe-127">Comunicazione tra oggetti</span><span class="sxs-lookup"><span data-stu-id="c73fe-127">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="c73fe-128">Dettagli del marshalling</span><span class="sxs-lookup"><span data-stu-id="c73fe-128">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="c73fe-129">RPC Microsoft</span><span class="sxs-lookup"><span data-stu-id="c73fe-129">Microsoft RPC</span></span>](microsoft-rpc.md)
</dt> <dt>

[<span data-ttu-id="c73fe-130">Stub</span><span class="sxs-lookup"><span data-stu-id="c73fe-130">Stub</span></span>](stub.md)
</dt> </dl>

 

 