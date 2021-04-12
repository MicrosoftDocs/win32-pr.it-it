---
title: Contenimento/delega
description: Il meccanismo più comune per il riutilizzo degli oggetti in COM è il contenimento/delega.
ms.assetid: 56396c11-889a-4f28-8fa7-9e48c805c501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d26e0c1d1e48596cb9acef740405c797f6f0f46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332356"
---
# <a name="containmentdelegation"></a><span data-ttu-id="fc2e5-103">Contenimento/delega</span><span class="sxs-lookup"><span data-stu-id="fc2e5-103">Containment/Delegation</span></span>

<span data-ttu-id="fc2e5-104">Il meccanismo più comune per il riutilizzo degli oggetti in COM è il *contenimento/delega*.</span><span class="sxs-lookup"><span data-stu-id="fc2e5-104">The most common mechanism for object reuse in COM is *containment/delegation*.</span></span> <span data-ttu-id="fc2e5-105">Questo tipo di riutilizzo è un concetto familiare presente nella maggior parte dei sistemi e dei linguaggi orientati agli oggetti.</span><span class="sxs-lookup"><span data-stu-id="fc2e5-105">This type of reuse is a familiar concept found in most object-oriented languages and systems.</span></span> <span data-ttu-id="fc2e5-106">L'oggetto esterno, che deve usare l'oggetto interno, funge da client oggetto per l'oggetto interno.</span><span class="sxs-lookup"><span data-stu-id="fc2e5-106">The outer object, which needs to make use of the inner object, acts as an object client to the inner object.</span></span> <span data-ttu-id="fc2e5-107">L'oggetto esterno "contiene" l'oggetto interno e quando l'oggetto esterno richiede i servizi dell'oggetto interno, l'oggetto esterno delega in modo esplicito l'implementazione ai metodi dell'oggetto interno.</span><span class="sxs-lookup"><span data-stu-id="fc2e5-107">The outer object "contains" the inner object, and when the outer object requires the services of the inner object, the outer object explicitly delegates implementation to the inner object's methods.</span></span> <span data-ttu-id="fc2e5-108">Ciò significa che l'oggetto esterno usa i servizi dell'oggetto interno per implementare se stesso.</span><span class="sxs-lookup"><span data-stu-id="fc2e5-108">That is, the outer object uses the inner object's services to implement itself.</span></span>

<span data-ttu-id="fc2e5-109">Non è necessario che gli oggetti esterni e interni supportino le stesse interfacce, sebbene sia certamente ragionevole contenere un oggetto che implementi un'interfaccia non eseguita dall'oggetto esterno e implementi i metodi dell'oggetto esterno semplicemente come le chiamate ai metodi corrispondenti nell'oggetto interno.</span><span class="sxs-lookup"><span data-stu-id="fc2e5-109">It is not necessary for the outer and inner objects to support the same interfaces, although it certainly is reasonable to contain an object that implements an interface that the outer object does not and implement the methods of the outer object simply as calls to the corresponding methods in the inner object.</span></span> <span data-ttu-id="fc2e5-110">Quando la complessità degli oggetti esterni e interni è notevolmente diversa, tuttavia, l'oggetto esterno può implementare alcuni dei metodi delle relative interfacce delegando le chiamate ai metodi di interfaccia implementati nell'oggetto interno.</span><span class="sxs-lookup"><span data-stu-id="fc2e5-110">When the complexity of the outer and inner objects differs greatly, however, the outer object may implement some of the methods of its interfaces by delegating calls to interface methods implemented in the inner object.</span></span>

<span data-ttu-id="fc2e5-111">È semplice implementare il contenimento per un oggetto esterno.</span><span class="sxs-lookup"><span data-stu-id="fc2e5-111">It is simple to implement containment for an outer object.</span></span> <span data-ttu-id="fc2e5-112">L'oggetto esterno crea gli oggetti interni che devono usare come qualsiasi altro client.</span><span class="sxs-lookup"><span data-stu-id="fc2e5-112">The outer object creates the inner objects it needs to use as any other client would.</span></span> <span data-ttu-id="fc2e5-113">Non si tratta di una novità: il processo è simile a un oggetto C++ che a sua volta contiene un oggetto stringa C++ che usa per eseguire determinate funzioni stringa, anche se l'oggetto esterno non è considerato un oggetto stringa in un proprio diritto.</span><span class="sxs-lookup"><span data-stu-id="fc2e5-113">This is nothing new—the process is like a C++ object that itself contains a C++ string object that it uses to perform certain string functions, even if the outer object is not considered a string object in its own right.</span></span> <span data-ttu-id="fc2e5-114">Quindi, usando il relativo puntatore all'oggetto interno, una chiamata a un metodo nell'oggetto esterno genera una chiamata a un metodo dell'oggetto interno.</span><span class="sxs-lookup"><span data-stu-id="fc2e5-114">Then, using its pointer to the inner object, a call to a method in the outer object generates a call to an inner object method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc2e5-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc2e5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc2e5-116">Aggregazione</span><span class="sxs-lookup"><span data-stu-id="fc2e5-116">Aggregation</span></span>](aggregation.md)
</dt> </dl>

 

 




