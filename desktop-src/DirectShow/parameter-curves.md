---
description: Curve parametro
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: Curve parametro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c482112c8bd76217f5cbdabdf3cda13b09c3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125016"
---
# <a name="parameter-curves"></a><span data-ttu-id="edebf-103">Curve parametro</span><span class="sxs-lookup"><span data-stu-id="edebf-103">Parameter Curves</span></span>

<span data-ttu-id="edebf-104">I parametri del supporto sono in grado di seguire una curva nel tempo.</span><span class="sxs-lookup"><span data-stu-id="edebf-104">Media parameters are able to follow a curve over time.</span></span> <span data-ttu-id="edebf-105">Ogni curva è descritta da una formula matematica e da due punti finali.</span><span class="sxs-lookup"><span data-stu-id="edebf-105">Each curve is described by a mathematical formula and two end-points.</span></span> <span data-ttu-id="edebf-106">Ogni endpoint è definito da un'ora di riferimento e dal valore della curva in quel momento.</span><span class="sxs-lookup"><span data-stu-id="edebf-106">Each end-point is defined by a reference time and the value of the curve at that time.</span></span> <span data-ttu-id="edebf-107">La formula viene utilizzata per calcolare i valori intermedi tra i punti e determina la forma della curva.</span><span class="sxs-lookup"><span data-stu-id="edebf-107">The formula is used to calculate intermediate values between the points, and determines the shape of the curve.</span></span> <span data-ttu-id="edebf-108">Le curve possibili sono:</span><span class="sxs-lookup"><span data-stu-id="edebf-108">The possible curves are:</span></span>

-   <span data-ttu-id="edebf-109">Saltare</span><span class="sxs-lookup"><span data-stu-id="edebf-109">Jump</span></span>
-   <span data-ttu-id="edebf-110">Lineari</span><span class="sxs-lookup"><span data-stu-id="edebf-110">Linear</span></span>
-   <span data-ttu-id="edebf-111">Square</span><span class="sxs-lookup"><span data-stu-id="edebf-111">Square</span></span>
-   <span data-ttu-id="edebf-112">Quadrato inverso</span><span class="sxs-lookup"><span data-stu-id="edebf-112">Inverse square</span></span>
-   <span data-ttu-id="edebf-113">Seno</span><span class="sxs-lookup"><span data-stu-id="edebf-113">Sine</span></span>

<span data-ttu-id="edebf-114">"Jump" significa passare direttamente al valore finale.</span><span class="sxs-lookup"><span data-stu-id="edebf-114">"Jump" means jump directly to the end value.</span></span> <span data-ttu-id="edebf-115">Le altre curve sono illustrate nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="edebf-115">The other curves are shown in the following diagram.</span></span>

![curve parametro](images/param-curves01.png)

<span data-ttu-id="edebf-117">In matematica, le curve funzionano come segue.</span><span class="sxs-lookup"><span data-stu-id="edebf-117">Mathematically, the curves work as follows.</span></span> <span data-ttu-id="edebf-118">Si supponga che una curva inizi all'ora *t*₀ con il valore *v*₀ e termini al momento *t*₁ con il valore *v*₁.</span><span class="sxs-lookup"><span data-stu-id="edebf-118">Suppose that a curve begins at time *t*₀ with a value of *v*₀, and ends at time *t*₁ with a value of *v*₁.</span></span> <span data-ttu-id="edebf-119">I due punti che definiscono la curva sono (*t*₀, *v*₀) e (*t*₁, *v*₁).</span><span class="sxs-lookup"><span data-stu-id="edebf-119">The two points that define the curve are (*t*₀, *v*₀) and (*t*₁, *v*₁).</span></span>

-   <span data-ttu-id="edebf-120">Consentire a Δ *t* di essere la durata totale della curva, *t*₁ –*t*₀.</span><span class="sxs-lookup"><span data-stu-id="edebf-120">Let Δ *t* be the total duration of the curve, *t*₁–*t*₀.</span></span>
-   <span data-ttu-id="edebf-121">Consentire a Δ *v* di essere l'intervallo tra i valori iniziale e finale, *v*₁ –*v*₀.</span><span class="sxs-lookup"><span data-stu-id="edebf-121">Let Δ *v* be the interval between the starting and ending values, *v*₁–*v*₀.</span></span>
-   <span data-ttu-id="edebf-122">In qualsiasi momento *t* tale che *t*₀ <= *t*  <=  *t*₁, Let Δ *t'*= *t*–*t*₀.</span><span class="sxs-lookup"><span data-stu-id="edebf-122">At any time *t* such that *t*₀ <= *t* <= *t*₁, let Δ *t*' = *t*–*t*₀.</span></span>

![calcolo parametri](images/param-curves02.png)

<span data-ttu-id="edebf-124">Il valore del parametro all'ora *t* è:</span><span class="sxs-lookup"><span data-stu-id="edebf-124">The value of the parameter at time *t* is:</span></span>

<span data-ttu-id="edebf-125">*v* = f (δ *t*'/δ *t* ) \* Δ *v*  +  *v*₀</span><span class="sxs-lookup"><span data-stu-id="edebf-125">*v* = f( Δ *t*' / Δ *t* ) \* Δ *v* + *v*₀</span></span>

<span data-ttu-id="edebf-126">dove f (x) è una funzione determinata dal tipo di curva:</span><span class="sxs-lookup"><span data-stu-id="edebf-126">where f(x) is a function determined by the curve type:</span></span>

-   <span data-ttu-id="edebf-127">Lineare: y = x</span><span class="sxs-lookup"><span data-stu-id="edebf-127">Linear: y = x</span></span>
-   <span data-ttu-id="edebf-128">Quadrato: y = x ^ 2</span><span class="sxs-lookup"><span data-stu-id="edebf-128">Square: y = x^2</span></span>
-   <span data-ttu-id="edebf-129">Quadrato inverso: y = sqrt (x)</span><span class="sxs-lookup"><span data-stu-id="edebf-129">Inverse square: y = sqrt(x)</span></span>
-   <span data-ttu-id="edebf-130">Seno: y = \[ sin (πx-π/2) + 1 \] /2</span><span class="sxs-lookup"><span data-stu-id="edebf-130">Sine: y = \[ sin(πx – π/2) + 1 \] / 2</span></span>

<span data-ttu-id="edebf-131">Osservare che Δ *t'*< δ *t*, quindi il termine δ *t*'/δ *t* è compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="edebf-131">Observe that Δ *t*' < Δ *t*, so the term Δ *t*'/Δ *t* ranges from 0 to 1.</span></span> <span data-ttu-id="edebf-132">F (x), quindi, è compreso tra 0 e 1 e *v* è sempre compreso tra *v*₀ e *v*₁.</span><span class="sxs-lookup"><span data-stu-id="edebf-132">Therefore, f(x) also ranges from 0 to 1, and *v* always falls between *v*₀ and *v*₁.</span></span> <span data-ttu-id="edebf-133">Questo vale se *v*₀ < *v*₁ o viceversa.</span><span class="sxs-lookup"><span data-stu-id="edebf-133">This is true whether *v*₀ < *v*₁ or vice versa.</span></span> <span data-ttu-id="edebf-134">In altre parole, la curva è vincolata dal rettangolo (*t*₀, *v*₀, *t*₁, *v*₁).</span><span class="sxs-lookup"><span data-stu-id="edebf-134">In other words, the curve is bounded by the rectangle (*t*₀, *v*₀, *t*₁, *v*₁).</span></span>

<span data-ttu-id="edebf-135">Per la curva seno, il valore di (πx-π/2) è compreso tra-π/2 e π/2, il che significa che sin (πx-π/2) è compreso tra-1 e 1.</span><span class="sxs-lookup"><span data-stu-id="edebf-135">For the sine curve, the value of (πx – π/2) ranges from –π/2 to π/2, which means that sin(πx – π/2) ranges from –1 to 1.</span></span> <span data-ttu-id="edebf-136">Il risultato viene quindi normalizzato in modo che f (x) rientri nell'intervallo (0-1).</span><span class="sxs-lookup"><span data-stu-id="edebf-136">The result is then normalized so that f(x) falls into the range (0–1).</span></span>

## <a name="related-topics"></a><span data-ttu-id="edebf-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="edebf-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edebf-138">Parametri dei supporti</span><span class="sxs-lookup"><span data-stu-id="edebf-138">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



