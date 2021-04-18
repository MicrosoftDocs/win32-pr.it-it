---
description: 'Passaggio 2:'
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: 'Passaggio 2: Dichiarare la classe filter'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ddfe28b7f31238089c331b319621787aef49f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315938"
---
# <a name="step-2-declare-the-filter-class"></a><span data-ttu-id="c5c2d-104">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="c5c2d-104">Step 2.</span></span> <span data-ttu-id="c5c2d-105">Dichiarare la classe filter</span><span class="sxs-lookup"><span data-stu-id="c5c2d-105">Declare the Filter Class</span></span>

<span data-ttu-id="c5c2d-106">Questo è il passaggio 2 dell'esercitazione [scrittura dei filtri di trasformazione](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="c5c2d-106">This is step 2 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="c5c2d-107">Iniziare dichiarando una classe C++ che eredita la classe di base:</span><span class="sxs-lookup"><span data-stu-id="c5c2d-107">Start by declaring a C++ class that inherits the base class:</span></span>


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



<span data-ttu-id="c5c2d-108">A ognuna delle classi di filtro sono associate classi pin.</span><span class="sxs-lookup"><span data-stu-id="c5c2d-108">Each of the filter classes has associated pin classes.</span></span> <span data-ttu-id="c5c2d-109">A seconda delle esigenze specifiche del filtro, potrebbe essere necessario eseguire l'override delle classi pin.</span><span class="sxs-lookup"><span data-stu-id="c5c2d-109">Depending on the specific needs of your filter, you might need to override the pin classes.</span></span> <span data-ttu-id="c5c2d-110">Nel caso di **CTransformFilter**, i pin delegano la maggior parte del lavoro al filtro, quindi probabilmente non è necessario eseguire l'override dei pin.</span><span class="sxs-lookup"><span data-stu-id="c5c2d-110">In the case of **CTransformFilter**, the pins delegate most of their work to the filter, so you probably don't need to override the pins.</span></span>

<span data-ttu-id="c5c2d-111">È necessario generare un CLSID univoco per il filtro.</span><span class="sxs-lookup"><span data-stu-id="c5c2d-111">You must generate a unique CLSID for the filter.</span></span> <span data-ttu-id="c5c2d-112">È possibile utilizzare l'utilità Guidgen o uuidgen. non copiare mai un GUID esistente.</span><span class="sxs-lookup"><span data-stu-id="c5c2d-112">You can use the Guidgen or Uuidgen utility; never copy an existing GUID.</span></span> <span data-ttu-id="c5c2d-113">Esistono diversi modi per dichiarare un CLSID.</span><span class="sxs-lookup"><span data-stu-id="c5c2d-113">There are several ways to declare a CLSID.</span></span> <span data-ttu-id="c5c2d-114">Nell'esempio seguente viene usata la macro **Definisci \_ GUID** :</span><span class="sxs-lookup"><span data-stu-id="c5c2d-114">The following example uses the **DEFINE\_GUID** macro:</span></span>


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



<span data-ttu-id="c5c2d-115">Successivamente, scrivere un metodo del costruttore per il filtro:</span><span class="sxs-lookup"><span data-stu-id="c5c2d-115">Next, write a constructor method for the filter:</span></span>


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



<span data-ttu-id="c5c2d-116">Si noti che uno dei parametri del costruttore [**CTransformFilter**](ctransformfilter-ctransformfilter.md) è il CLSID definito in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c5c2d-116">Notice that one of the parameters to the [**CTransformFilter**](ctransformfilter-ctransformfilter.md) constructor is the CLSID defined earlier.</span></span>

<span data-ttu-id="c5c2d-117">Successivo: [passaggio 3. Supporto della negoziazione del tipo](step-3--support-media-type-negotiation.md)di supporto.</span><span class="sxs-lookup"><span data-stu-id="c5c2d-117">Next: [Step 3. Support Media Type Negotiation](step-3--support-media-type-negotiation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5c2d-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5c2d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5c2d-119">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="c5c2d-119">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



