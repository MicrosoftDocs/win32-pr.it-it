---
title: Implementazione di IClassFactory
description: Implementazione di IClassFactory
ms.assetid: 96466756-c135-4ee5-a48c-f31129878473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b057657508b3060506c15c68308ea6a5332e5099
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399752"
---
# <a name="implementing-iclassfactory"></a><span data-ttu-id="69d7c-103">Implementazione di IClassFactory</span><span class="sxs-lookup"><span data-stu-id="69d7c-103">Implementing IClassFactory</span></span>

<span data-ttu-id="69d7c-104">Quando un client utilizza un CLSID per richiedere la creazione di un'istanza dell'oggetto, il primo passaggio consiste nella creazione di un oggetto classe, un oggetto intermedio che contiene un'implementazione dei metodi dell'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) .</span><span class="sxs-lookup"><span data-stu-id="69d7c-104">When a client uses a CLSID to request the creation of an object instance, the first step is creation of a class object, an intermediate object that contains an implementation of the methods of the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface.</span></span> <span data-ttu-id="69d7c-105">Sebbene COM fornisca diverse funzioni di creazione di istanze, il primo passaggio nell'implementazione di queste funzioni è la creazione di un oggetto classe.</span><span class="sxs-lookup"><span data-stu-id="69d7c-105">While COM provides several instance creation functions, the first step in the implementation of these functions is the creation of a class object.</span></span>

<span data-ttu-id="69d7c-106">Di conseguenza, tutti i server devono implementare i metodi dell'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , che contiene due metodi:</span><span class="sxs-lookup"><span data-stu-id="69d7c-106">As a result, all servers must implement the methods of the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface, which contains two methods:</span></span>

-   <span data-ttu-id="69d7c-107">[**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance).</span><span class="sxs-lookup"><span data-stu-id="69d7c-107">[**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance).</span></span> <span data-ttu-id="69d7c-108">Questo metodo deve creare un'istanza non inizializzata dell'oggetto e restituire un puntatore a un'interfaccia richiesta nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="69d7c-108">This method must create an uninitialized instance of the object and return a pointer to a requested interface on the object.</span></span>
-   <span data-ttu-id="69d7c-109">[**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver).</span><span class="sxs-lookup"><span data-stu-id="69d7c-109">[**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver).</span></span> <span data-ttu-id="69d7c-110">Questo metodo incrementa il conteggio dei riferimenti nell'oggetto classe per garantire che il server rimanga in memoria e non venga arrestato prima che il client sia pronto per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="69d7c-110">This method just increments the reference count on the class object to ensure that the server stays in memory and does not shut down before the client is ready for it to do so.</span></span>

<span data-ttu-id="69d7c-111">Per consentire a un server di essere responsabile della propria licenza, COM definisce [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), che eredita la definizione da [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="69d7c-111">To enable a server to be responsible for its own licensing, COM defines [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), which inherits its definition from [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="69d7c-112">Pertanto, un server che implementa **IClassFactory2** deve, per definizione, implementare i metodi di **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="69d7c-112">Thus, a server implementing **IClassFactory2** must, by definition, implement the methods of **IClassFactory**.</span></span>

<span data-ttu-id="69d7c-113">COM fornisce anche funzioni di supporto per l'implementazione di server out-of-process.</span><span class="sxs-lookup"><span data-stu-id="69d7c-113">COM also provides helper functions for implementing out-of-process servers.</span></span> <span data-ttu-id="69d7c-114">Per ulteriori informazioni, vedere [Helper di implementazione del server out-of-process](out-of-process-server-implementation-helpers.md).</span><span class="sxs-lookup"><span data-stu-id="69d7c-114">For more information, see [Out-of-Process Server Implementation Helpers](out-of-process-server-implementation-helpers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="69d7c-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69d7c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69d7c-116">Responsabilità server COM</span><span class="sxs-lookup"><span data-stu-id="69d7c-116">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> <dt>

[<span data-ttu-id="69d7c-117">Licenze e IClassFactory2</span><span class="sxs-lookup"><span data-stu-id="69d7c-117">Licensing and IClassFactory2</span></span>](licensing-and-iclassfactory2.md)
</dt> </dl>

 

 