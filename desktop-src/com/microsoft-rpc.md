---
title: RPC Microsoft
description: RPC Microsoft
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be9d46368ae01aee25815327aafeaf7f44525b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707252"
---
# <a name="microsoft-rpc"></a><span data-ttu-id="56339-103">RPC Microsoft</span><span class="sxs-lookup"><span data-stu-id="56339-103">Microsoft RPC</span></span>

<span data-ttu-id="56339-104">Microsoft RPC è un modello per la programmazione in un ambiente di elaborazione distribuito.</span><span class="sxs-lookup"><span data-stu-id="56339-104">Microsoft RPC is a model for programming in a distributed computing environment.</span></span> <span data-ttu-id="56339-105">L'obiettivo di RPC è fornire la comunicazione trasparente, in modo che il client sembri comunicare direttamente con il server.</span><span class="sxs-lookup"><span data-stu-id="56339-105">The goal of RPC is to provide transparent communication so that the client appears to be directly communicating with the server.</span></span> <span data-ttu-id="56339-106">L'implementazione di RPC di Microsoft è compatibile con la RPC Open Software Foundation (OSF) Distributed Computing Environment (DCE).</span><span class="sxs-lookup"><span data-stu-id="56339-106">Microsoft's implementation of RPC is compatible with the Open Software Foundation (OSF) Distributed Computing Environment (DCE) RPC.</span></span>

<span data-ttu-id="56339-107">È possibile configurare RPC per l'utilizzo di uno o più trasporti, uno o più servizi dei nomi e uno o più server di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="56339-107">You can configure RPC to use one or more transports, one or more name services, and one or more security servers.</span></span> <span data-ttu-id="56339-108">Le interfacce a tali provider sono gestite da RPC.</span><span class="sxs-lookup"><span data-stu-id="56339-108">The interfaces to those providers are handled by RPC.</span></span> <span data-ttu-id="56339-109">Poiché Microsoft RPC è progettato per funzionare con più provider, è possibile scegliere i provider che funzionano meglio per la rete.</span><span class="sxs-lookup"><span data-stu-id="56339-109">Because Microsoft RPC is designed to work with multiple providers, you can choose the providers that work best for your network.</span></span> <span data-ttu-id="56339-110">Il trasporto è responsabile della trasmissione dei dati attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="56339-110">The transport is responsible for transmitting the data across the network.</span></span> <span data-ttu-id="56339-111">Il servizio nome accetta un nome di oggetto, ad esempio un moniker, e ne trova la posizione sulla rete.</span><span class="sxs-lookup"><span data-stu-id="56339-111">The name service takes an object name, such as a moniker, and finds its location on the network.</span></span> <span data-ttu-id="56339-112">Il server di sicurezza offre alle applicazioni la possibilità di negare l'accesso a utenti e/o gruppi specifici.</span><span class="sxs-lookup"><span data-stu-id="56339-112">The security server offers applications the option of denying access to specific users and/or groups.</span></span> <span data-ttu-id="56339-113">Per informazioni più dettagliate sulla sicurezza delle applicazioni, vedere [regole di progettazione dell'interfaccia](interface-design-rules.md) .</span><span class="sxs-lookup"><span data-stu-id="56339-113">See [Interface Design Rules](interface-design-rules.md) for more detailed information about application security.</span></span>

<span data-ttu-id="56339-114">Oltre alle librerie di runtime RPC, Microsoft RPC include il linguaggio di definizione dell'interfaccia (IDL) e il relativo compilatore.</span><span class="sxs-lookup"><span data-stu-id="56339-114">In addition to the RPC run-time libraries, Microsoft RPC includes the Interface Definition Language (IDL) and its compiler.</span></span> <span data-ttu-id="56339-115">Sebbene il file IDL sia una parte standard di RPC, Microsoft lo ha migliorato per estendere le funzionalità per supportare interfacce COM personalizzate.</span><span class="sxs-lookup"><span data-stu-id="56339-115">Although the IDL file is a standard part of RPC, Microsoft has enhanced it to extend its functionality to support custom COM interfaces.</span></span> <span data-ttu-id="56339-116">Il compilatore Microsoft Interface Definition Language (MIDL) utilizza il file IDL che descrive l'interfaccia personalizzata per generare più file descritti in [compilazione e registrazione di una DLL proxy](building-and-registering-a-proxy-dll.md).</span><span class="sxs-lookup"><span data-stu-id="56339-116">The Microsoft Interface Definition Language (MIDL) compiler uses the IDL file that describes your custom interface to generate several files discussed in [Building and Registering a Proxy DLL](building-and-registering-a-proxy-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56339-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="56339-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56339-118">Channel</span><span class="sxs-lookup"><span data-stu-id="56339-118">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="56339-119">Comunicazione tra oggetti</span><span class="sxs-lookup"><span data-stu-id="56339-119">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="56339-120">Dettagli del marshalling</span><span class="sxs-lookup"><span data-stu-id="56339-120">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="56339-121">Proxy</span><span class="sxs-lookup"><span data-stu-id="56339-121">Proxy</span></span>](proxy.md)
</dt> <dt>

[<span data-ttu-id="56339-122">Stub</span><span class="sxs-lookup"><span data-stu-id="56339-122">Stub</span></span>](stub.md)
</dt> </dl>

 

 




