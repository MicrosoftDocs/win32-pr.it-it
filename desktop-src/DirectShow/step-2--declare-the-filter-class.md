---
description: Dichiarare una classe C++ che eredita la classe di base scelta nell'ambito della scrittura di un filtro di trasformazione.
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: 'Passaggio 2: Dichiarare la classe Filter'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88be97e47d529ffa22c90e9c8c200160dbd5f261
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410064"
---
# <a name="step-2-declare-the-filter-class"></a><span data-ttu-id="6b219-104">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="6b219-104">Step 2.</span></span> <span data-ttu-id="6b219-105">Dichiarare la classe Filter</span><span class="sxs-lookup"><span data-stu-id="6b219-105">Declare the Filter Class</span></span>

<span data-ttu-id="6b219-106">Questo è il passaggio 2 dell'esercitazione [Scrittura di filtri di trasformazione.](writing-transform-filters.md)</span><span class="sxs-lookup"><span data-stu-id="6b219-106">This is step 2 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="6b219-107">Per iniziare, dichiarare una classe C++ che eredita la classe di base:</span><span class="sxs-lookup"><span data-stu-id="6b219-107">Start by declaring a C++ class that inherits the base class:</span></span>


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



<span data-ttu-id="6b219-108">A ognuna delle classi di filtro sono associate classi pin.</span><span class="sxs-lookup"><span data-stu-id="6b219-108">Each of the filter classes has associated pin classes.</span></span> <span data-ttu-id="6b219-109">A seconda delle esigenze specifiche del filtro, potrebbe essere necessario eseguire l'override delle classi pin.</span><span class="sxs-lookup"><span data-stu-id="6b219-109">Depending on the specific needs of your filter, you might need to override the pin classes.</span></span> <span data-ttu-id="6b219-110">Nel caso di **CTransformFilter,** i segnaposto delegano la maggior parte del lavoro al filtro, quindi probabilmente non è necessario eseguire l'override dei segnaposto.</span><span class="sxs-lookup"><span data-stu-id="6b219-110">In the case of **CTransformFilter**, the pins delegate most of their work to the filter, so you probably don't need to override the pins.</span></span>

<span data-ttu-id="6b219-111">È necessario generare un CLSID univoco per il filtro.</span><span class="sxs-lookup"><span data-stu-id="6b219-111">You must generate a unique CLSID for the filter.</span></span> <span data-ttu-id="6b219-112">È possibile usare l'utilità Guidgen o Uuidgen. non copiare mai un GUID esistente.</span><span class="sxs-lookup"><span data-stu-id="6b219-112">You can use the Guidgen or Uuidgen utility; never copy an existing GUID.</span></span> <span data-ttu-id="6b219-113">Esistono diversi modi per dichiarare un CLSID.</span><span class="sxs-lookup"><span data-stu-id="6b219-113">There are several ways to declare a CLSID.</span></span> <span data-ttu-id="6b219-114">Nell'esempio seguente viene utilizzata la macro **DEFINE \_ GUID:**</span><span class="sxs-lookup"><span data-stu-id="6b219-114">The following example uses the **DEFINE\_GUID** macro:</span></span>


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



<span data-ttu-id="6b219-115">Scrivere quindi un metodo costruttore per il filtro:</span><span class="sxs-lookup"><span data-stu-id="6b219-115">Next, write a constructor method for the filter:</span></span>


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



<span data-ttu-id="6b219-116">Si noti che uno dei parametri per il [**costruttore CTransformFilter**](ctransformfilter-ctransformfilter.md) è il CLSID definito in precedenza.</span><span class="sxs-lookup"><span data-stu-id="6b219-116">Notice that one of the parameters to the [**CTransformFilter**](ctransformfilter-ctransformfilter.md) constructor is the CLSID defined earlier.</span></span>

<span data-ttu-id="6b219-117">Passaggio [successivo: Passaggio 3. Supporto della negoziazione del tipo di supporto](step-3--support-media-type-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="6b219-117">Next: [Step 3. Support Media Type Negotiation](step-3--support-media-type-negotiation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b219-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b219-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b219-119">Scrittura di filtri DirectMostra filtri</span><span class="sxs-lookup"><span data-stu-id="6b219-119">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



