---
description: Controllo di grafici filtro con C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Controllo di grafici filtro con C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce6d78875c6b0d5f028ea89dfbd2b061285f1c1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401259"
---
# <a name="controlling-filter-graphs-using-c"></a><span data-ttu-id="068c7-103">Controllo di grafici filtro con C</span><span class="sxs-lookup"><span data-stu-id="068c7-103">Controlling Filter Graphs Using C</span></span>

<span data-ttu-id="068c7-104">Se si sta scrivendo un'applicazione DirectShow in C (anziché in C++), è necessario usare un puntatore vtable per chiamare i metodi.</span><span class="sxs-lookup"><span data-stu-id="068c7-104">If you are writing a DirectShow application in C (rather than C++), you must use a vtable pointer to call methods.</span></span> <span data-ttu-id="068c7-105">Nell'esempio seguente viene illustrato come chiamare il metodo **IUnknown:: QueryInterface** da un'applicazione scritta in C:</span><span class="sxs-lookup"><span data-stu-id="068c7-105">The following example illustrates how to call the **IUnknown::QueryInterface** method from an application written in C:</span></span>


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="068c7-106">Di seguito viene illustrata la chiamata equivalente in C++:</span><span class="sxs-lookup"><span data-stu-id="068c7-106">The following shows the equivalent call in C++:</span></span>


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="068c7-107">In C, le interfacce COM sono definite come strutture.</span><span class="sxs-lookup"><span data-stu-id="068c7-107">In C, COM interfaces are defined as structures.</span></span> <span data-ttu-id="068c7-108">Il membro **lpVtbl** è un puntatore a una tabella di metodi di interfaccia (vtable).</span><span class="sxs-lookup"><span data-stu-id="068c7-108">The **lpVtbl** member is a pointer to a table of interface methods (the vtable).</span></span> <span data-ttu-id="068c7-109">Tutti i metodi accettano un parametro aggiuntivo, ovvero un puntatore all'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="068c7-109">All methods take an additional parameter, which is a pointer to the interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="068c7-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="068c7-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="068c7-111">Appendici</span><span class="sxs-lookup"><span data-stu-id="068c7-111">Appendixes</span></span>](appendixes.md)
</dt> </dl>

 

 



