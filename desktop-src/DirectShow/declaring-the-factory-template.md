---
description: Dichiarazione del modello Factory
ms.assetid: 3060c167-ea23-4061-b32a-16e750f55e6f
title: Dichiarazione del modello Factory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3168f16b6281417846f13b7a17141282053c4705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123693"
---
# <a name="declaring-the-factory-template"></a><span data-ttu-id="d4dc9-103">Dichiarazione del modello Factory</span><span class="sxs-lookup"><span data-stu-id="d4dc9-103">Declaring the Factory Template</span></span>

<span data-ttu-id="d4dc9-104">Il passaggio successivo consiste nel dichiarare il modello factory per il filtro.</span><span class="sxs-lookup"><span data-stu-id="d4dc9-104">The next step is to declare the factory template for your filter.</span></span> <span data-ttu-id="d4dc9-105">Un modello di Factory è una classe C++ che contiene informazioni per la class factory.</span><span class="sxs-lookup"><span data-stu-id="d4dc9-105">A factory template is a C++ class that contains information for the class factory.</span></span> <span data-ttu-id="d4dc9-106">Nella DLL dichiarare una matrice globale di oggetti [**CFactoryTemplate**](cfactorytemplate.md) , uno per ogni filtro o componente COM della dll.</span><span class="sxs-lookup"><span data-stu-id="d4dc9-106">In your DLL, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) objects, one for each filter or COM component in your DLL.</span></span> <span data-ttu-id="d4dc9-107">La matrice deve essere denominata *g \_ templates*.</span><span class="sxs-lookup"><span data-stu-id="d4dc9-107">The array must be named *g\_Templates*.</span></span> <span data-ttu-id="d4dc9-108">Per ulteriori informazioni sui modelli Factory, vedere [How to create an DirectShow Filter DLL](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="d4dc9-108">For more information about factory templates, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="d4dc9-109">Il membro del **\_ \_ filtro pAMovieSetup m** del modello Factory è un puntatore alla struttura [**del \_ filtro AMOVIESETUP**](amoviesetup-filter.md) descritta in precedenza.</span><span class="sxs-lookup"><span data-stu-id="d4dc9-109">The **m\_pAMovieSetup\_Filter** member of the factory template is a pointer to the [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure described previously.</span></span> <span data-ttu-id="d4dc9-110">L'esempio seguente illustra un modello Factory, usando la struttura specificata nell'esempio precedente:</span><span class="sxs-lookup"><span data-stu-id="d4dc9-110">The following example shows a factory template, using the structure given in the previous example:</span></span>


```C++
CFactoryTemplate g_Templates[] = {
    {
        g_wszName,                      // Name.
        &CLSID_SomeFilter,              // CLSID.
        CSomeFilter::CreateInstance,    // Creation function.
        NULL,
        &sudFilterReg                   // Pointer to filter information.
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);
```



<span data-ttu-id="d4dc9-111">Se non è stata dichiarata alcuna informazione sul filtro, il **\_ \_ filtro m PAMoveSetup** può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="d4dc9-111">If you did not declare any filter information, **m\_pAMoveSetup\_Filter** can be **NULL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4dc9-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d4dc9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4dc9-113">Come registrare i filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="d4dc9-113">How to Register DirectShow Filters</span></span>](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



