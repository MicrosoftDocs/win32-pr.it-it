---
title: Stub
description: Lo stub, come il proxy, è costituito da una o più parti dell'interfaccia e da un responsabile.
ms.assetid: ed7d5546-2d19-4055-b078-62b39d0317b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109936ae16827dce7779b080902dbca74a8dfc51
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "106320194"
---
# <a name="stub"></a><span data-ttu-id="8e32d-103">Stub</span><span class="sxs-lookup"><span data-stu-id="8e32d-103">Stub</span></span>

<span data-ttu-id="8e32d-104">Lo stub, come il proxy, è costituito da una o più parti dell'interfaccia e da un responsabile.</span><span class="sxs-lookup"><span data-stu-id="8e32d-104">The stub, like the proxy, is made up of one or more interface pieces and a manager.</span></span> <span data-ttu-id="8e32d-105">Ogni stub di interfaccia fornisce codice per l'unmarshalling dei parametri e del codice che chiama una delle interfacce supportate dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8e32d-105">Each interface stub provides code to unmarshal the parameters and code that calls one of the object's supported interfaces.</span></span> <span data-ttu-id="8e32d-106">Ogni stub fornisce anche un'interfaccia per la comunicazione interna.</span><span class="sxs-lookup"><span data-stu-id="8e32d-106">Each stub also provides an interface for internal communication.</span></span> <span data-ttu-id="8e32d-107">Il gestore Stub tiene traccia degli stub di interfaccia disponibili.</span><span class="sxs-lookup"><span data-stu-id="8e32d-107">The stub manager keeps track of the available interface stubs.</span></span>

<span data-ttu-id="8e32d-108">Esistono, tuttavia, le differenze seguenti tra lo stub e il proxy:</span><span class="sxs-lookup"><span data-stu-id="8e32d-108">There are, however, the following differences between the stub and the proxy:</span></span>

-   <span data-ttu-id="8e32d-109">La differenza più importante è che lo stub rappresenta il client nello spazio degli indirizzi dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8e32d-109">The most important difference is that the stub represents the client in the object's address space.</span></span>
-   <span data-ttu-id="8e32d-110">Lo stub non è implementato come oggetto aggregato perché non è necessario che il client venga visualizzato come una singola unità. ogni parte nello stub è un componente separato.</span><span class="sxs-lookup"><span data-stu-id="8e32d-110">The stub is not implemented as an aggregate object because there is no requirement that the client be viewed as a single unit; each piece in the stub is a separate component.</span></span>
-   <span data-ttu-id="8e32d-111">Gli stub di interfaccia sono privati anziché pubblici.</span><span class="sxs-lookup"><span data-stu-id="8e32d-111">The interface stubs are private rather than public.</span></span>
-   <span data-ttu-id="8e32d-112">Gli stub di interfaccia implementano [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), non [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).</span><span class="sxs-lookup"><span data-stu-id="8e32d-112">The interface stubs implement [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), not [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).</span></span>
-   <span data-ttu-id="8e32d-113">Anziché creare il marshalling dei parametri, lo stub li rimuove dal pacchetto dopo che è stato eseguito il marshalling e quindi crea il pacchetto della risposta.</span><span class="sxs-lookup"><span data-stu-id="8e32d-113">Instead of packaging parameters to be marshaled, the stub unpackages them after they have been marshaled and then packages the reply.</span></span>

## <a name="structure-of-the-stub"></a><span data-ttu-id="8e32d-114">Struttura dello stub</span><span class="sxs-lookup"><span data-stu-id="8e32d-114">Structure of the Stub</span></span>

<span data-ttu-id="8e32d-115">Nel diagramma seguente viene illustrata la struttura dello stub.</span><span class="sxs-lookup"><span data-stu-id="8e32d-115">The following diagram shows the structure of the stub.</span></span> <span data-ttu-id="8e32d-116">Ogni stub di interfaccia è connesso a un'interfaccia nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8e32d-116">Each interface stub is connected to an interface on the object.</span></span> <span data-ttu-id="8e32d-117">Il canale invia i messaggi in ingresso allo stub di interfaccia appropriato.</span><span class="sxs-lookup"><span data-stu-id="8e32d-117">The channel dispatches incoming messages to the appropriate interface stub.</span></span> <span data-ttu-id="8e32d-118">Tutti i componenti comunicano con il canale tramite [**Metodo IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), l'interfaccia che fornisce l'accesso alla libreria di runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="8e32d-118">All the components talk to the channel through [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), the interface that provides access to the RPC run-time library.</span></span>

![Screenshot che mostra la struttura dello stub.](images/98714a22-733e-432f-bb90-408bbeecc23f.png)

## <a name="related-topics"></a><span data-ttu-id="8e32d-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8e32d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e32d-121">Channel</span><span class="sxs-lookup"><span data-stu-id="8e32d-121">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="8e32d-122">Comunicazione tra oggetti</span><span class="sxs-lookup"><span data-stu-id="8e32d-122">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="8e32d-123">Dettagli del marshalling</span><span class="sxs-lookup"><span data-stu-id="8e32d-123">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="8e32d-124">RPC Microsoft</span><span class="sxs-lookup"><span data-stu-id="8e32d-124">Microsoft RPC</span></span>](microsoft-rpc.md)
</dt> <dt>

[<span data-ttu-id="8e32d-125">Proxy</span><span class="sxs-lookup"><span data-stu-id="8e32d-125">Proxy</span></span>](proxy.md)
</dt> </dl>

 

 