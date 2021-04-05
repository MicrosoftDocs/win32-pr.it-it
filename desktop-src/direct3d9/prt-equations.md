---
description: Per comprendere completamente uno shader che implementa PRT, è utile derivare la formula utilizzata dallo shader per calcolare l'uscita.
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: Equazioni PRT (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65559fada82fda7f7eed1c7d05543883a06a19e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124818"
---
# <a name="prt-equations-direct3d-9"></a><span data-ttu-id="aa54f-103">Equazioni PRT (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="aa54f-103">PRT Equations (Direct3D 9)</span></span>

<span data-ttu-id="aa54f-104">Per comprendere completamente uno shader che implementa PRT, è utile derivare la formula utilizzata dallo shader per calcolare l'uscita.</span><span class="sxs-lookup"><span data-stu-id="aa54f-104">To fully understand a shader that implements PRT, it is useful to derive the formula the shader uses to calculate exit radiance.</span></span>

<span data-ttu-id="aa54f-105">Per iniziare, l'equazione seguente è l'equazione generale per calcolare l'uscita radiante risultante dall'illuminazione diretta su un oggetto diffuso con illuminazione distante arbitraria.</span><span class="sxs-lookup"><span data-stu-id="aa54f-105">To start off, the following equation is the general equation to calculate exit radiance resulting from direct lighting on a diffuse object with arbitrary distant lighting.</span></span>

![equazione della luminosità di uscita risultante dall'illuminazione diretta su un oggetto diffuso con illuminazione distante arbitraria](images/prt-theory-eq1.png)

<span data-ttu-id="aa54f-107">dove:</span><span class="sxs-lookup"><span data-stu-id="aa54f-107">where:</span></span>



| <span data-ttu-id="aa54f-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="aa54f-108">Parameter</span></span>     | <span data-ttu-id="aa54f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa54f-109">Description</span></span>                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa54f-110">RP</span><span class="sxs-lookup"><span data-stu-id="aa54f-110">Rₚ</span></span>            | <span data-ttu-id="aa54f-111">Radiance di uscita in corrispondenza del vertice p.</span><span class="sxs-lookup"><span data-stu-id="aa54f-111">The exit radiance at vertex p.</span></span> <span data-ttu-id="aa54f-112">Valutato a ogni vertice sulla rete.</span><span class="sxs-lookup"><span data-stu-id="aa54f-112">Evaluated at every vertex on the mesh.</span></span>                                   |
| <span data-ttu-id="aa54f-113">p<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="aa54f-113">p<sub>d</sub></span></span> | <span data-ttu-id="aa54f-114">Albedo della superficie.</span><span class="sxs-lookup"><span data-stu-id="aa54f-114">The albedo of the surface.</span></span>                                                                              |
| <span data-ttu-id="aa54f-115">pi</span><span class="sxs-lookup"><span data-stu-id="aa54f-115">pi</span></span>            | <span data-ttu-id="aa54f-116">Costante utilizzata come fattore di normalizzazione per la conservazione dell'energia.</span><span class="sxs-lookup"><span data-stu-id="aa54f-116">A constant, used as an energy conservation normalization factor.</span></span>                                        |
| <span data-ttu-id="aa54f-117">L (s)</span><span class="sxs-lookup"><span data-stu-id="aa54f-117">L(s)</span></span>          | <span data-ttu-id="aa54f-118">Ambiente di illuminazione (Radiance di origine).</span><span class="sxs-lookup"><span data-stu-id="aa54f-118">The lighting environment (source radiance).</span></span>                                                             |
| <span data-ttu-id="aa54f-119">₎ VP ₍ s</span><span class="sxs-lookup"><span data-stu-id="aa54f-119">Vₚ₍ₛ₎</span></span>         | <span data-ttu-id="aa54f-120">Funzione di visibilità binaria per il punto p.</span><span class="sxs-lookup"><span data-stu-id="aa54f-120">A binary visibility function for point p.</span></span> <span data-ttu-id="aa54f-121">È 1 se il punto può visualizzare la luce, 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="aa54f-121">It is 1 if the point can see the light, 0 if not.</span></span>             |
| <span data-ttu-id="aa54f-122">HNP ₍ s ₎</span><span class="sxs-lookup"><span data-stu-id="aa54f-122">Hₙₚ₍ₛ₎</span></span>        | <span data-ttu-id="aa54f-123">Termine del coseno dalla legge di Lambert.</span><span class="sxs-lookup"><span data-stu-id="aa54f-123">The cosine term from Lambert's law.</span></span> <span data-ttu-id="aa54f-124">Uguale a Max ((NP · s), 0) dove NP è la normale della superficie al punto p.</span><span class="sxs-lookup"><span data-stu-id="aa54f-124">Equal to max((Nₚ· s), 0) where Nₚ is the surface normal at point p.</span></span> |
| <span data-ttu-id="aa54f-125">s</span><span class="sxs-lookup"><span data-stu-id="aa54f-125">s</span></span>             | <span data-ttu-id="aa54f-126">Variabile che si integra sulla sfera.</span><span class="sxs-lookup"><span data-stu-id="aa54f-126">The variable that integrates over the sphere.</span></span>                                                           |



 

<span data-ttu-id="aa54f-127">Con le funzioni di base sferica, ad esempio le armoniche sferiche, l'equazione seguente si avvicina all'ambiente di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="aa54f-127">Using spherical basis functions, such as spherical harmonics, the following equation approximates the lighting environment.</span></span>

![equazione dell'ambiente di illuminazione](images/prt-theory-eq2.png)

<span data-ttu-id="aa54f-129">dove:</span><span class="sxs-lookup"><span data-stu-id="aa54f-129">where:</span></span>



| <span data-ttu-id="aa54f-130">Parametro</span><span class="sxs-lookup"><span data-stu-id="aa54f-130">Parameter</span></span>        | <span data-ttu-id="aa54f-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa54f-131">Description</span></span>                                              |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="aa54f-132">L (s)</span><span class="sxs-lookup"><span data-stu-id="aa54f-132">L(s)</span></span>             | <span data-ttu-id="aa54f-133">Ambiente di illuminazione (Radiance di origine).</span><span class="sxs-lookup"><span data-stu-id="aa54f-133">The lighting environment (source radiance).</span></span>              |
| <span data-ttu-id="aa54f-134">i</span><span class="sxs-lookup"><span data-stu-id="aa54f-134">i</span></span>                | <span data-ttu-id="aa54f-135">Intero che somma il numero di funzioni di base.</span><span class="sxs-lookup"><span data-stu-id="aa54f-135">An integer that sums over the number of basis functions.</span></span> |
| <span data-ttu-id="aa54f-136">O</span><span class="sxs-lookup"><span data-stu-id="aa54f-136">O</span></span>                | <span data-ttu-id="aa54f-137">Ordine delle armoniche sferiche.</span><span class="sxs-lookup"><span data-stu-id="aa54f-137">The order of spherical harmonics.</span></span>                        |
| <span data-ttu-id="aa54f-138">l<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="aa54f-138">l<sub>i</sub></span></span>    | <span data-ttu-id="aa54f-139">Coefficiente.</span><span class="sxs-lookup"><span data-stu-id="aa54f-139">A coefficient.</span></span>                                           |
| <span data-ttu-id="aa54f-140"><sub>I/o</sub></span><span class="sxs-lookup"><span data-stu-id="aa54f-140">Y<sub>i(s)</sub></span></span> | <span data-ttu-id="aa54f-141">Una funzione di base sulla sfera.</span><span class="sxs-lookup"><span data-stu-id="aa54f-141">Some basis function over the sphere.</span></span>                     |



 

<span data-ttu-id="aa54f-142">La raccolta di questi coefficienti, L', fornisce l'approssimazione ottimale per la funzione L (s) con le funzioni di base Y.</span><span class="sxs-lookup"><span data-stu-id="aa54f-142">The collection of these coefficients, L', provides the optimal approximation for function L(s) with the basis functions Y(s).</span></span> <span data-ttu-id="aa54f-143">La sostituzione e la distribuzione producono la seguente equazione.</span><span class="sxs-lookup"><span data-stu-id="aa54f-143">Substituting and distributing yields the following equation.</span></span>

![equazione della luminosità di uscita dopo la sostituzione di l (s) e della distribuzione](images/prt-theory-eq3.png)

<span data-ttu-id="aa54f-145">L'integrale di Y<sub>i (s)</sub>VP ₍ s ₎ HNP ₍ s ₎ è un coefficiente di trasferimento t<sub>pi</sub> utilizzato dal simulatore per ogni vertice sulla rete.</span><span class="sxs-lookup"><span data-stu-id="aa54f-145">The integral of Y<sub>i(s)</sub>Vₚ₍ₛ₎Hₙₚ₍ₛ₎ is a transfer coefficient t<sub>pi</sub> that the simulator precomputes for every vertex on the mesh.</span></span> <span data-ttu-id="aa54f-146">Se si sostituisce questa operazione, viene restituita l'equazione seguente.</span><span class="sxs-lookup"><span data-stu-id="aa54f-146">Substituting this yields the following equation.</span></span>

![equazione della luminosità di uscita dopo la sostituzione del coefficiente di trasferimento](images/prt-theory-eq4.png)

<span data-ttu-id="aa54f-148">Se si modifica questa notazione Vector, viene restituita l'equazione non compressa seguente per calcolare l'uscita Radiance per ogni canale.</span><span class="sxs-lookup"><span data-stu-id="aa54f-148">Changing this to vector notation yields the following uncompressed equation to calculate exit radiance for each channel.</span></span>

![equazione della luminosità di uscita dopo la modifica alla notazione vettoriale](images/prt-theory-eq5.png)

<span data-ttu-id="aa54f-150">dove:</span><span class="sxs-lookup"><span data-stu-id="aa54f-150">where:</span></span>



| <span data-ttu-id="aa54f-151">Parametro</span><span class="sxs-lookup"><span data-stu-id="aa54f-151">Parameter</span></span>     | <span data-ttu-id="aa54f-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa54f-152">Description</span></span>                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa54f-153">RP</span><span class="sxs-lookup"><span data-stu-id="aa54f-153">Rₚ</span></span>            | <span data-ttu-id="aa54f-154">Radiance di uscita in corrispondenza del vertice p.</span><span class="sxs-lookup"><span data-stu-id="aa54f-154">The exit radiance at vertex p.</span></span>                                                                                                                                                      |
| <span data-ttu-id="aa54f-155">p<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="aa54f-155">p<sub>d</sub></span></span> | <span data-ttu-id="aa54f-156">Albedo della superficie.</span><span class="sxs-lookup"><span data-stu-id="aa54f-156">The albedo of the surface.</span></span>                                                                                                                                                          |
| <span data-ttu-id="aa54f-157">L</span><span class="sxs-lookup"><span data-stu-id="aa54f-157">L'</span></span>            | <span data-ttu-id="aa54f-158">Il vettore di l<sub>i</sub>e rappresenta la proiezione della luminosità di origine nelle funzioni di base armonica sferica.</span><span class="sxs-lookup"><span data-stu-id="aa54f-158">The vector of l<sub>i</sub>, and is the projection of the source radiance into the spherical harmonic basis functions.</span></span> <span data-ttu-id="aa54f-159">Si tratta di un vettore Order ² dei coefficienti armonici sferici.</span><span class="sxs-lookup"><span data-stu-id="aa54f-159">This is an order² vector of spherical harmonic coefficients.</span></span> |
| <span data-ttu-id="aa54f-160">TP</span><span class="sxs-lookup"><span data-stu-id="aa54f-160">Tₚ</span></span>            | <span data-ttu-id="aa54f-161">Vettore di trasferimento Order ² per il vertice p.</span><span class="sxs-lookup"><span data-stu-id="aa54f-161">An order² transfer vector for vertex p.</span></span> <span data-ttu-id="aa54f-162">Il simulatore divide i coefficienti di trasferimento di p.</span><span class="sxs-lookup"><span data-stu-id="aa54f-162">The simulator divides the transfer coefficients by p.</span></span>                                                                                       |



 

<span data-ttu-id="aa54f-163">Entrambi questi vettori sono un vettore di ordine ² di coefficienti sferici sferici, quindi si noti che si tratta semplicemente di un prodotto a virgola.</span><span class="sxs-lookup"><span data-stu-id="aa54f-163">Both of these vectors are an order² vector of spherical harmonic coefficients, so notice that this is simply a dot product.</span></span> <span data-ttu-id="aa54f-164">A seconda dell'ordine, il punto può essere dispendioso, quindi è possibile usare la compressione.</span><span class="sxs-lookup"><span data-stu-id="aa54f-164">Depending on the order, the dot can be expensive so compression can be used.</span></span> <span data-ttu-id="aa54f-165">Un algoritmo denominato AP (Clustered Principal Component Analysis) comprime i dati in modo efficiente.</span><span class="sxs-lookup"><span data-stu-id="aa54f-165">An algorithm called Clustered Principal Component Analysis (CPCA) efficiently compresses the data.</span></span> <span data-ttu-id="aa54f-166">Questo consente l'uso di un'approssimazione armonica sferica di ordine superiore che produce ombre più nitide.</span><span class="sxs-lookup"><span data-stu-id="aa54f-166">This enables the use of a higher-order spherical harmonic approximation which results in sharper shadows.</span></span>

<span data-ttu-id="aa54f-167">AP fornisce l'equazione seguente per approssimare il vettore di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="aa54f-167">CPCA provides the following equation to approximate the transfer vector.</span></span>

![equazione del vettore di trasferimento approssimato](images/prt-theory-eq6.png)

<span data-ttu-id="aa54f-169">dove:</span><span class="sxs-lookup"><span data-stu-id="aa54f-169">where:</span></span>



| <span data-ttu-id="aa54f-170">Parametro</span><span class="sxs-lookup"><span data-stu-id="aa54f-170">Parameter</span></span>      | <span data-ttu-id="aa54f-171">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa54f-171">Description</span></span>                                          |
|----------------|------------------------------------------------------|
| <span data-ttu-id="aa54f-172">TP</span><span class="sxs-lookup"><span data-stu-id="aa54f-172">Tₚ</span></span>             | <span data-ttu-id="aa54f-173">Vettore di trasferimento per il vertice p.</span><span class="sxs-lookup"><span data-stu-id="aa54f-173">The transfer vector for vertex p.</span></span>                    |
| <span data-ttu-id="aa54f-174">MK</span><span class="sxs-lookup"><span data-stu-id="aa54f-174">Mₖ</span></span>             | <span data-ttu-id="aa54f-175">Media per il cluster k.</span><span class="sxs-lookup"><span data-stu-id="aa54f-175">The mean for cluster k.</span></span>                              |
| <span data-ttu-id="aa54f-176">j</span><span class="sxs-lookup"><span data-stu-id="aa54f-176">j</span></span>              | <span data-ttu-id="aa54f-177">Intero che somma il numero di vettori PCA.</span><span class="sxs-lookup"><span data-stu-id="aa54f-177">An integer that sums over the number of PCA vectors.</span></span> |
| <span data-ttu-id="aa54f-178">N</span><span class="sxs-lookup"><span data-stu-id="aa54f-178">N</span></span>              | <span data-ttu-id="aa54f-179">Numero di vettori PCA.</span><span class="sxs-lookup"><span data-stu-id="aa54f-179">The number of PCA vectors.</span></span>                           |
| <span data-ttu-id="aa54f-180">w<sub>PJ</sub></span><span class="sxs-lookup"><span data-stu-id="aa54f-180">w<sub>pj</sub></span></span> | <span data-ttu-id="aa54f-181">Peso PCA JTH per il punto p.</span><span class="sxs-lookup"><span data-stu-id="aa54f-181">The jth PCA weight for point p.</span></span>                      |
| <span data-ttu-id="aa54f-182">B<sub>kJ</sub></span><span class="sxs-lookup"><span data-stu-id="aa54f-182">B<sub>kj</sub></span></span> | <span data-ttu-id="aa54f-183">Vettore di base di JTH PCA per il cluster k.</span><span class="sxs-lookup"><span data-stu-id="aa54f-183">The jth PCA basis vector for cluster k.</span></span>              |



 

<span data-ttu-id="aa54f-184">Un cluster è semplicemente un numero di vertici che condividono lo stesso vettore medio.</span><span class="sxs-lookup"><span data-stu-id="aa54f-184">A cluster is simply some number of vertices that share the same mean vector.</span></span> <span data-ttu-id="aa54f-185">Come ottenere la media del cluster, i pesi PCA, i vettori di base PCA e gli ID cluster per i vertici vengono descritti di seguito.</span><span class="sxs-lookup"><span data-stu-id="aa54f-185">How to get the cluster mean, the PCA weights, the PCA basis vectors, and the cluster ids for the vertices is discussed below.</span></span>

<span data-ttu-id="aa54f-186">La sostituzione di queste due equazioni produce:</span><span class="sxs-lookup"><span data-stu-id="aa54f-186">Substituting these two equations yields:</span></span>

![equazione della luminosità di uscita dopo la sostituzione del vettore di trasferimento](images/prt-theory-eq7.png)

<span data-ttu-id="aa54f-188">La distribuzione del prodotto punto produce quindi l'equazione seguente.</span><span class="sxs-lookup"><span data-stu-id="aa54f-188">Then distributing the dot product yields the following equation.</span></span>

![equazione della luminosità di uscita dopo la distribuzione del prodotto del punto](images/prt-theory-eq8.png)

<span data-ttu-id="aa54f-190">Poiché entrambe (MK · L') e (B<sub>kJ</sub>· L') sono costanti per vertice, l'esempio calcola questi valori con la CPU e li passa come costanti nel vertex shader; Poiché w<sub>PJ</sub> cambia per ogni vertice, l'esempio archivia i dati per vertice nel buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="aa54f-190">Because both (Mₖ· L') and (B<sub>kj</sub>· L') are constant per vertex, the sample calculates these values with the CPU and passes them as constants into the vertex shader; because w<sub>pj</sub> changes for each vertex, the sample stores this per-vertex data in the vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa54f-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa54f-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa54f-192">Trasferimento Radiance pre-calcolato</span><span class="sxs-lookup"><span data-stu-id="aa54f-192">Precomputed Radiance Transfer</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



