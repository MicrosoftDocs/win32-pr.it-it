---
description: Metodi di callback asincroni
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Metodi di callback asincroni
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0064873a5b026b6910597ebc9911f56f00584b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305520"
---
# <a name="asynchronous-callback-methods"></a><span data-ttu-id="5eb3d-103">Metodi di callback asincroni</span><span class="sxs-lookup"><span data-stu-id="5eb3d-103">Asynchronous Callback Methods</span></span>

<span data-ttu-id="5eb3d-104">Media Foundation offre un modo coerente per implementare metodi asincroni, usando un'interfaccia di callback.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-104">Media Foundation provides a consistent way to implement asynchronous methods, using a callback interface.</span></span>

<span data-ttu-id="5eb3d-105">In questa sezione viene descritto come implementare l'interfaccia di callback e come scrivere metodi asincroni che utilizzano questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-105">This section describes how to implement the callback interface and how to write asynchronous methods that use this interface.</span></span> <span data-ttu-id="5eb3d-106">Contiene gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-106">It contains the following topics.</span></span>



| <span data-ttu-id="5eb3d-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="5eb3d-107">Topic</span></span>                                                                                | <span data-ttu-id="5eb3d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5eb3d-108">Description</span></span>                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5eb3d-109">Chiamata di metodi asincroni</span><span class="sxs-lookup"><span data-stu-id="5eb3d-109">Calling Asynchronous Methods</span></span>](calling-asynchronous-methods.md)                     | <span data-ttu-id="5eb3d-110">Come chiamare metodi asincroni in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-110">How to call asynchronous methods in Media Foundation.</span></span>                                               |
| [<span data-ttu-id="5eb3d-111">Implementazione del callback asincrono</span><span class="sxs-lookup"><span data-stu-id="5eb3d-111">Implementing the Asynchronous Callback</span></span>](implementing-the-asynchronous-callback.md) | <span data-ttu-id="5eb3d-112">Come implementare il metodo di callback nell'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="5eb3d-112">How to implement the callback method in the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> |
| [<span data-ttu-id="5eb3d-113">Supporto di più callback</span><span class="sxs-lookup"><span data-stu-id="5eb3d-113">Supporting Multiple Callbacks</span></span>](supporting-multiple-callbacks.md)                   | <span data-ttu-id="5eb3d-114">Come supportare più callback all'interno della stessa classe C++.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-114">How to support multiple callbacks within the same C++ class.</span></span>                                        |
| [<span data-ttu-id="5eb3d-115">Code di lavoro</span><span class="sxs-lookup"><span data-stu-id="5eb3d-115">Work Queues</span></span>](work-queues.md)                                                       | <span data-ttu-id="5eb3d-116">Le code di lavoro rappresentano un modo efficiente per eseguire operazioni asincrone su un altro thread.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-116">Work queues provide an efficient way to perform asynchronous operations on another thread.</span></span>          |
| [<span data-ttu-id="5eb3d-117">Scrittura di un metodo asincrono</span><span class="sxs-lookup"><span data-stu-id="5eb3d-117">Writing an Asynchronous Method</span></span>](writing-an-asynchronous-method.md)                 | <span data-ttu-id="5eb3d-118">Come implementare metodi asincroni in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-118">How to implement asynchronous methods in Media Foundation.</span></span>                                          |
| [<span data-ttu-id="5eb3d-119">Oggetti risultato asincrono personalizzati</span><span class="sxs-lookup"><span data-stu-id="5eb3d-119">Custom Asynchronous Result Objects</span></span>](custom-asynchronous-result-objects.md)         | <span data-ttu-id="5eb3d-120">Come fornire un'implementazione personalizzata dell'interfaccia [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="5eb3d-120">How to provide a custom implementation of the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="5eb3d-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5eb3d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eb3d-122">**Interfaccia IMFAsyncCallback**</span><span class="sxs-lookup"><span data-stu-id="5eb3d-122">**IMFAsyncCallback Interface**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[<span data-ttu-id="5eb3d-123">**Interfaccia IMFAsyncResult**</span><span class="sxs-lookup"><span data-stu-id="5eb3d-123">**IMFAsyncResult Interface**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[<span data-ttu-id="5eb3d-124">API della piattaforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5eb3d-124">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



