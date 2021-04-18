---
description: Creazione di oggetti Timeline
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: Creazione di oggetti Timeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929fffb6a953e198b6e7ed9b17250d45e84f7932
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303782"
---
# <a name="creating-timeline-objects"></a><span data-ttu-id="5b7a5-103">Creazione di oggetti Timeline</span><span class="sxs-lookup"><span data-stu-id="5b7a5-103">Creating Timeline Objects</span></span>

<span data-ttu-id="5b7a5-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="5b7a5-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="5b7a5-105">Il codice di esempio presentato in questo articolo inizia con una sequenza temporale vuota, ma gli stessi passaggi si applicano se si carica un progetto esistente e si desidera aggiungervi oggetti.</span><span class="sxs-lookup"><span data-stu-id="5b7a5-105">The sample code presented in this article starts with an empty timeline, but the same steps apply if you load an existing project and want to add objects to it.</span></span>

<span data-ttu-id="5b7a5-106">Per creare qualsiasi tipo di oggetto nella sequenza temporale, chiamare il metodo [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="5b7a5-106">To create any type of object in the timeline, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="5b7a5-107">Il codice seguente, ad esempio, consente di creare un nuovo gruppo:</span><span class="sxs-lookup"><span data-stu-id="5b7a5-107">For example, the following code creates a new group:</span></span>


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



<span data-ttu-id="5b7a5-108">Il secondo parametro è un membro dell'enumerazione [**di \_ \_ tipo principale della sequenza temporale**](timeline-major-type.md) .</span><span class="sxs-lookup"><span data-stu-id="5b7a5-108">The second parameter is a member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumeration.</span></span> <span data-ttu-id="5b7a5-109">Specifica il tipo di oggetto sequenza temporale da creare, ad esempio un gruppo o una traccia.</span><span class="sxs-lookup"><span data-stu-id="5b7a5-109">It specifies the type of timeline object to create, such as a group or a track.</span></span>

<span data-ttu-id="5b7a5-110">Il metodo **CreateEmptyNode** crea l'oggetto e restituisce un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5b7a5-110">The **CreateEmptyNode** method creates the object and returns a pointer to the object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span> <span data-ttu-id="5b7a5-111">Incrementa inoltre il conteggio dei riferimenti sull'interfaccia **IAMTimelineObj** , pertanto è necessario rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="5b7a5-111">It also increments the reference count on the **IAMTimelineObj** interface, so you must release the interface when you finish using it.</span></span> <span data-ttu-id="5b7a5-112">Non chiamare la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="5b7a5-112">Do not call the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span> <span data-ttu-id="5b7a5-113">Usare invece sempre **CreateEmptyNode** per creare un oggetto sequenza temporale, perché Inizializza il nuovo oggetto per l'uso in una sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="5b7a5-113">Instead, always use **CreateEmptyNode** to create a timeline object, because it initializes the new object for use in a timeline.</span></span>

<span data-ttu-id="5b7a5-114">L'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) è un'interfaccia generica.</span><span class="sxs-lookup"><span data-stu-id="5b7a5-114">The [**IAMTimelineObj**](iamtimelineobj.md) interface is a generic interface.</span></span> <span data-ttu-id="5b7a5-115">Fornisce metodi comuni a tutti i tipi di oggetto sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="5b7a5-115">It provides methods that are common to all types of timeline object.</span></span> <span data-ttu-id="5b7a5-116">Ogni tipo di oggetto espone anche altre interfacce.</span><span class="sxs-lookup"><span data-stu-id="5b7a5-116">Each type of object exposes other interfaces as well.</span></span> <span data-ttu-id="5b7a5-117">Ad esempio, i gruppi espongono l'interfaccia [**IAMTimelineGroup**](iamtimelinegroup.md) , tra gli altri.</span><span class="sxs-lookup"><span data-stu-id="5b7a5-117">For example, groups expose the [**IAMTimelineGroup**](iamtimelinegroup.md) interface, among others.</span></span> <span data-ttu-id="5b7a5-118">È possibile ottenere i puntatori alle altre interfacce chiamando **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="5b7a5-118">You can obtain pointers to the other interfaces by calling **QueryInterface**.</span></span>

<span data-ttu-id="5b7a5-119">Dopo aver creato un oggetto, non fa ancora parte della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="5b7a5-119">After you create an object, it is not yet a part of the timeline.</span></span> <span data-ttu-id="5b7a5-120">Il metodo per aggiungere un oggetto alla sequenza temporale dipende dal tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="5b7a5-120">The method to add an object to the timeline depends on the object type.</span></span> <span data-ttu-id="5b7a5-121">Nella sezione seguente viene descritto come aggiungere gruppi, composizioni e tracce alla sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="5b7a5-121">The following section describes how to add groups, compositions, and tracks to the timeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b7a5-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5b7a5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b7a5-123">Creazione di una sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="5b7a5-123">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 
