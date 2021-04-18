---
description: Le tecniche forniscono il muscolo di rendering. Una tecnica incapsula lo stato dell'effetto che determina uno stile di rendering. Una tecnica è costituita da uno o più passaggi.
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: Tecniche e passaggi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3a68ac40db16b3e6819adf6fcd1f8a6f790325
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304374"
---
# <a name="techniques-and-passes-direct3d-9"></a><span data-ttu-id="e0f39-105">Tecniche e passaggi (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e0f39-105">Techniques and Passes (Direct3D 9)</span></span>

<span data-ttu-id="e0f39-106">Le tecniche forniscono il muscolo di rendering.</span><span class="sxs-lookup"><span data-stu-id="e0f39-106">Techniques provide the rendering muscle.</span></span> <span data-ttu-id="e0f39-107">Una tecnica incapsula lo stato dell'effetto che determina uno stile di rendering.</span><span class="sxs-lookup"><span data-stu-id="e0f39-107">A technique encapsulates the effect state that determines a rendering style.</span></span> <span data-ttu-id="e0f39-108">Una tecnica è costituita da uno o più passaggi.</span><span class="sxs-lookup"><span data-stu-id="e0f39-108">A technique is made up of one or more passes.</span></span>

## <a name="techniques"></a><span data-ttu-id="e0f39-109">Tecniche</span><span class="sxs-lookup"><span data-stu-id="e0f39-109">Techniques</span></span>

<span data-ttu-id="e0f39-110">La sintassi per la chiamata di una tecnica è la seguente:</span><span class="sxs-lookup"><span data-stu-id="e0f39-110">The syntax for calling a technique is as follows:</span></span>


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



<span data-ttu-id="e0f39-111">Dove:</span><span class="sxs-lookup"><span data-stu-id="e0f39-111">Where:</span></span>

-   <span data-ttu-id="e0f39-112">ID è un nome univoco facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e0f39-112">id is an optional unique name.</span></span>
-   <span data-ttu-id="e0f39-113">l'annotazione è zero o più parti facoltative delle informazioni specifiche dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e0f39-113">annotation is zero or more optional pieces of user-specific information.</span></span> <span data-ttu-id="e0f39-114">Vedere [aggiungere informazioni ai parametri di effetto con le \_ annotazioni](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="e0f39-114">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>
-   <span data-ttu-id="e0f39-115">i pass (es) sono pari a zero o più sessioni.</span><span class="sxs-lookup"><span data-stu-id="e0f39-115">pass(es) is zero or more passes.</span></span> <span data-ttu-id="e0f39-116">Ogni sessione contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="e0f39-116">Each pass contains state assignments.</span></span> <span data-ttu-id="e0f39-117">Vedere qui di seguito.</span><span class="sxs-lookup"><span data-stu-id="e0f39-117">See below.</span></span>

## <a name="passes"></a><span data-ttu-id="e0f39-118">Passa</span><span class="sxs-lookup"><span data-stu-id="e0f39-118">Passes</span></span>

<span data-ttu-id="e0f39-119">Un passaggio contiene le assegnazioni di stato necessarie per il rendering.</span><span class="sxs-lookup"><span data-stu-id="e0f39-119">A pass contains the state assignments required to render.</span></span>


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



<span data-ttu-id="e0f39-120">Dove:</span><span class="sxs-lookup"><span data-stu-id="e0f39-120">Where:</span></span>

-   <span data-ttu-id="e0f39-121">ID è un nome univoco facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e0f39-121">id is an optional unique name.</span></span>
-   <span data-ttu-id="e0f39-122">l'annotazione è una o più informazioni facoltative specifiche dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e0f39-122">annotation is one or more optional piece of user-specific information.</span></span> <span data-ttu-id="e0f39-123">Vedere [aggiungere informazioni ai parametri di effetto con le \_ annotazioni](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="e0f39-123">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>
-   <span data-ttu-id="e0f39-124">assegnazione/i assegna zero o più valori di stato oppure valuta una o più espressioni.</span><span class="sxs-lookup"><span data-stu-id="e0f39-124">assignment(s) assigns zero or more state values, or evaluates one or more expressions.</span></span> <span data-ttu-id="e0f39-125">Vedere [gli Stati degli effetti (Direct3D 9)](effect-states.md) ed [espressioni (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="e0f39-125">See [Effect States (Direct3D 9)](effect-states.md) and [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="e0f39-126">Passa Ignora tutto tranne l'ultima assegnazione in un set di assegnazioni ripetute allo stesso stato.</span><span class="sxs-lookup"><span data-stu-id="e0f39-126">Passes ignore all but the last assignment in a set of repeated assignments to the same state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0f39-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0f39-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0f39-128">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="e0f39-128">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



