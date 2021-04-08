---
title: Quando usare la tabella dell'interfaccia globale
description: Quando usare la tabella dell'interfaccia globale
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89bbd7437b65c85abe89e8d647cbd73555c2d6a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047405"
---
# <a name="when-to-use-the-global-interface-table"></a><span data-ttu-id="1b8e9-103">Quando usare la tabella dell'interfaccia globale</span><span class="sxs-lookup"><span data-stu-id="1b8e9-103">When to Use the Global Interface Table</span></span>

<span data-ttu-id="1b8e9-104">Se si esegue l'unmarshalling di un puntatore di interfaccia più volte tra gli Apartment in un processo, è possibile usare l'interfaccia [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) .</span><span class="sxs-lookup"><span data-stu-id="1b8e9-104">If you are unmarshaling an interface pointer multiple times between apartments in a process, you might use the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="1b8e9-105">Con altre tecniche, è necessario eseguire il marshalling ogni volta.</span><span class="sxs-lookup"><span data-stu-id="1b8e9-105">With other techniques, you would have to remarshal each time.</span></span>

> [!Note]  
> <span data-ttu-id="1b8e9-106">Se viene eseguito l'unmarshalling del puntatore a interfaccia solo una volta, è possibile usare la funzione [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) .</span><span class="sxs-lookup"><span data-stu-id="1b8e9-106">If the interface pointer is unmarshaled only once, you may want to use the [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) function.</span></span> <span data-ttu-id="1b8e9-107">Può anche essere usato per passare un puntatore di interfaccia da un thread a un altro thread nello stesso processo.</span><span class="sxs-lookup"><span data-stu-id="1b8e9-107">It can also be used to pass an interface pointer from one thread to another thread in the same process.</span></span>

 

<span data-ttu-id="1b8e9-108">L'interfaccia [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) rende anche un altro problema più difficile in precedenza per il programmatore.</span><span class="sxs-lookup"><span data-stu-id="1b8e9-108">The [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface also makes another previously difficult problem simpler for the programmer.</span></span> <span data-ttu-id="1b8e9-109">Questo problema si verifica quando si applicano le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b8e9-109">This problem occurs when the following conditions apply:</span></span>

-   <span data-ttu-id="1b8e9-110">Un oggetto agile in-process aggrega il gestore di marshalling a thread libero.</span><span class="sxs-lookup"><span data-stu-id="1b8e9-110">An in-process agile object aggregates the free-threaded marshaler.</span></span>
-   <span data-ttu-id="1b8e9-111">Questo stesso oggetto Agile include anche i puntatori di interfaccia (come variabili membro) per gli altri oggetti che non sono agile e non aggregano il gestore di marshalling a thread libero.</span><span class="sxs-lookup"><span data-stu-id="1b8e9-111">This same agile object also holds (as member variables) interface pointers to other objects that are not agile and do not aggregate the free-threaded marshaler.</span></span>

<span data-ttu-id="1b8e9-112">In questa situazione, se l'oggetto esterno viene sottoposto a marshalling in un altro Apartment e l'applicazione chiama su di esso e l'oggetto tenta di chiamare su uno dei puntatori a interfaccia della variabile membro che non sono a thread libero o che sono proxy di oggetti in altri Apartment, potrebbe ottenere risultati non corretti o il thread RPC di errore \_ e un \_ \_ thread errato.</span><span class="sxs-lookup"><span data-stu-id="1b8e9-112">In this situation, if the outer object gets marshaled to another apartment and the application calls on it, and the object tries to call on any of its member variable interface pointers that are not free-threaded or are proxies to objects in other apartments, it might get incorrect results or the error RPC\_E\_WRONG\_THREAD.</span></span> <span data-ttu-id="1b8e9-113">Questo errore si verifica perché l'interfaccia interna è progettata per essere richiamabile solo dall'Apartment in cui è stata prima archiviata nella variabile membro.</span><span class="sxs-lookup"><span data-stu-id="1b8e9-113">This error occurs because the inner interface is designed to be callable only from the apartment in which it was first stored in the member variable.</span></span>

<span data-ttu-id="1b8e9-114">Per risolvere questo problema, è necessario che l'oggetto esterno che aggrega il gestore di marshalling a thread libero chiami [**IGlobalInterfaceTable:: RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) sull'interfaccia interna e memorizzi il cookie risultante nella variabile membro, anziché archiviare il puntatore di interfaccia effettivo.</span><span class="sxs-lookup"><span data-stu-id="1b8e9-114">To solve this problem, the outer object aggregating the free-threaded marshaler should call [**IGlobalInterfaceTable::RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) on the inner interface and store the resulting cookie in its member variable, instead of storing the actual interface pointer.</span></span> <span data-ttu-id="1b8e9-115">Quando l'oggetto esterno desidera chiamare sul puntatore a interfaccia di un oggetto interno, deve chiamare [**IGlobalInterfaceTable:: GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), utilizzare il puntatore di interfaccia restituito e quindi rilasciarlo.</span><span class="sxs-lookup"><span data-stu-id="1b8e9-115">When the outer object wants to call on an inner object's interface pointer, it should call [**IGlobalInterfaceTable::GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), use the returned interface pointer, and then release it.</span></span> <span data-ttu-id="1b8e9-116">Quando l'oggetto esterno viene rimosso, è necessario chiamare [**IGlobalInterfaceTable:: RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) per rimuovere l'interfaccia dalla tabella dell'interfaccia globale.</span><span class="sxs-lookup"><span data-stu-id="1b8e9-116">When the outer object goes away, it should call [**IGlobalInterfaceTable::RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) to remove the interface from the global interface table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b8e9-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1b8e9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b8e9-118">Creazione della tabella dell'interfaccia globale</span><span class="sxs-lookup"><span data-stu-id="1b8e9-118">Creating the Global Interface Table</span></span>](creating-the-global-interface-table.md)
</dt> </dl>

 

 