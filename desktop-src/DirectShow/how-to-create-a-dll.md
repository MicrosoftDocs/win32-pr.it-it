---
description: Come creare una DLL di filtro DirectShow
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Come creare una DLL di filtro DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee964115e040d11ae10562b05899b2895f03d2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303728"
---
# <a name="how-to-create-a-directshow-filter-dll"></a><span data-ttu-id="0c3a9-103">Come creare una DLL di filtro DirectShow</span><span class="sxs-lookup"><span data-stu-id="0c3a9-103">How to Create a DirectShow Filter DLL</span></span>

<span data-ttu-id="0c3a9-104">Questo articolo descrive come implementare un componente come libreria di collegamento dinamico (DLL) in Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0c3a9-104">This article describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.</span></span> <span data-ttu-id="0c3a9-105">Questo articolo è una continuazione di [come implementare IUnknown](how-to-implement-iunknown.md), che descrive come implementare l'interfaccia **IUnknown** derivando il componente dalla classe base [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="0c3a9-105">This article is a continuation from [How to Implement IUnknown](how-to-implement-iunknown.md), which describes how to implement the **IUnknown** interface by deriving your component from the [**CUnknown**](cunknown.md) base class.</span></span>

<span data-ttu-id="0c3a9-106">Questo articolo include le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="0c3a9-106">This article contains the following sections.</span></span>

-   [<span data-ttu-id="0c3a9-107">Class factory e modelli di Factory</span><span class="sxs-lookup"><span data-stu-id="0c3a9-107">Class Factories and Factory Templates</span></span>](class-factories-and-factory-templates.md)
-   [<span data-ttu-id="0c3a9-108">Matrice modello Factory</span><span class="sxs-lookup"><span data-stu-id="0c3a9-108">Factory Template Array</span></span>](factory-template-array.md)
-   [<span data-ttu-id="0c3a9-109">Funzioni DLL</span><span class="sxs-lookup"><span data-stu-id="0c3a9-109">DLL Functions</span></span>](dll-functions.md)

<span data-ttu-id="0c3a9-110">Per la registrazione di un filtro DirectShow (in contrapposizione a un oggetto COM generico) sono necessari alcuni passaggi aggiuntivi che non sono trattati in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="0c3a9-110">Registering a DirectShow filter (as opposed to a generic COM object) requires some additional steps that are not covered in this article.</span></span> <span data-ttu-id="0c3a9-111">Per informazioni sulla registrazione dei filtri, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="0c3a9-111">For information on registering filters, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c3a9-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c3a9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c3a9-113">DirectShow e COM</span><span class="sxs-lookup"><span data-stu-id="0c3a9-113">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



