---
description: Il tipo di dati del sensore primario per i sensori di luce di ambiente è illuminato in Lux (lumen per metro quadrato). I principi descritti in questo argomento si basano sull'assunzione di valori Lux come input e sulla reazione a tali dati in un programma.
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: Informazioni e interpretazione dei valori Lux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8012f983eeac29cc07b18ac2d27918d2df6ed52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057870"
---
# <a name="understanding-and-interpreting-lux-values"></a><span data-ttu-id="c4933-104">Informazioni e interpretazione dei valori Lux</span><span class="sxs-lookup"><span data-stu-id="c4933-104">Understanding and Interpreting Lux Values</span></span>

<span data-ttu-id="c4933-105">Il tipo di dati del sensore primario per i sensori di luce di ambiente è illuminato in Lux (lumen per metro quadrato).</span><span class="sxs-lookup"><span data-stu-id="c4933-105">The primary sensor data type for ambient light sensors is illuminance in lux (lumens per square meter).</span></span> <span data-ttu-id="c4933-106">I principi descritti in questo argomento si basano sull'assunzione di valori Lux come input e sulla reazione a tali dati in un programma.</span><span class="sxs-lookup"><span data-stu-id="c4933-106">The principles outlined in this topic are based on taking lux values as input and reacting to that data in a program.</span></span>

<span data-ttu-id="c4933-107">Le letture Lux sono direttamente proporzionali all'energia per ogni metro quadrato assorbita al secondo.</span><span class="sxs-lookup"><span data-stu-id="c4933-107">Lux readings are directly proportional to the energy per square meter that is absorbed per second.</span></span> <span data-ttu-id="c4933-108">La percezione umana dei livelli di luce non è così semplice.</span><span class="sxs-lookup"><span data-stu-id="c4933-108">Human perception of light levels is not so straightforward.</span></span> <span data-ttu-id="c4933-109">La percezione umana della luce è complessa perché i nostri occhi sono costantemente regolabili e altri processi biologici influiscono sulla nostra percezione.</span><span class="sxs-lookup"><span data-stu-id="c4933-109">Human perception of light is complicated because our eyes are constantly adjusting and other biological processes are affecting our perception.</span></span> <span data-ttu-id="c4933-110">Tuttavia, è possibile pensare a questa percezione da una prospettiva semplificata creando diversi intervalli di interesse con soglie note superiori e inferiori.</span><span class="sxs-lookup"><span data-stu-id="c4933-110">However, we can think of this perception from a simplified perspective by creating several ranges of interest with known upper and lower thresholds.</span></span>

<span data-ttu-id="c4933-111">Il set di dati di esempio seguente rappresenta le soglie approssimative per le condizioni di illuminazione comuni e il passaggio di illuminazione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="c4933-111">The following example data set represents rough thresholds for common lighting conditions, and the corresponding lighting step.</span></span> <span data-ttu-id="c4933-112">In questo caso, ogni passaggio di illuminazione rappresenta una modifica nell'ambiente di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="c4933-112">Here, each lighting step represents a change in lighting environment.</span></span>

> [!Note]  
> <span data-ttu-id="c4933-113">Questo set di dati è a illustrazione e potrebbe non essere completamente accurato per tutti gli utenti o le situazioni.</span><span class="sxs-lookup"><span data-stu-id="c4933-113">This data set is for illustration and may not be completely accurate for all users or situations.</span></span>

 



| <span data-ttu-id="c4933-114">Condizione di illuminazione</span><span class="sxs-lookup"><span data-stu-id="c4933-114">Lighting condition</span></span> | <span data-ttu-id="c4933-115">Da (LUX)</span><span class="sxs-lookup"><span data-stu-id="c4933-115">From (lux)</span></span> | <span data-ttu-id="c4933-116">A (LUX)</span><span class="sxs-lookup"><span data-stu-id="c4933-116">To (lux)</span></span> | <span data-ttu-id="c4933-117">Valore medio (LUX)</span><span class="sxs-lookup"><span data-stu-id="c4933-117">Mean value (lux)</span></span> | <span data-ttu-id="c4933-118">Passaggio di illuminazione</span><span class="sxs-lookup"><span data-stu-id="c4933-118">Lighting step</span></span> |
|--------------------|------------|----------|------------------|---------------|
| <span data-ttu-id="c4933-119">Pitch nero</span><span class="sxs-lookup"><span data-stu-id="c4933-119">Pitch Black</span></span>        | <span data-ttu-id="c4933-120">0</span><span class="sxs-lookup"><span data-stu-id="c4933-120">0</span></span>          | <span data-ttu-id="c4933-121">10</span><span class="sxs-lookup"><span data-stu-id="c4933-121">10</span></span>       | <span data-ttu-id="c4933-122">5</span><span class="sxs-lookup"><span data-stu-id="c4933-122">5</span></span>                | <span data-ttu-id="c4933-123">1</span><span class="sxs-lookup"><span data-stu-id="c4933-123">1</span></span>             |
| <span data-ttu-id="c4933-124">Molto scuro</span><span class="sxs-lookup"><span data-stu-id="c4933-124">Very Dark</span></span>          | <span data-ttu-id="c4933-125">11</span><span class="sxs-lookup"><span data-stu-id="c4933-125">11</span></span>         | <span data-ttu-id="c4933-126">50</span><span class="sxs-lookup"><span data-stu-id="c4933-126">50</span></span>       | <span data-ttu-id="c4933-127">30</span><span class="sxs-lookup"><span data-stu-id="c4933-127">30</span></span>               | <span data-ttu-id="c4933-128">2</span><span class="sxs-lookup"><span data-stu-id="c4933-128">2</span></span>             |
| <span data-ttu-id="c4933-129">Interni scuri</span><span class="sxs-lookup"><span data-stu-id="c4933-129">Dark Indoors</span></span>       | <span data-ttu-id="c4933-130">51</span><span class="sxs-lookup"><span data-stu-id="c4933-130">51</span></span>         | <span data-ttu-id="c4933-131">200</span><span class="sxs-lookup"><span data-stu-id="c4933-131">200</span></span>      | <span data-ttu-id="c4933-132">125</span><span class="sxs-lookup"><span data-stu-id="c4933-132">125</span></span>              | <span data-ttu-id="c4933-133">3</span><span class="sxs-lookup"><span data-stu-id="c4933-133">3</span></span>             |
| <span data-ttu-id="c4933-134">Dim-door</span><span class="sxs-lookup"><span data-stu-id="c4933-134">Dim Indoors</span></span>        | <span data-ttu-id="c4933-135">201</span><span class="sxs-lookup"><span data-stu-id="c4933-135">201</span></span>        | <span data-ttu-id="c4933-136">400</span><span class="sxs-lookup"><span data-stu-id="c4933-136">400</span></span>      | <span data-ttu-id="c4933-137">300</span><span class="sxs-lookup"><span data-stu-id="c4933-137">300</span></span>              | <span data-ttu-id="c4933-138">4</span><span class="sxs-lookup"><span data-stu-id="c4933-138">4</span></span>             |
| <span data-ttu-id="c4933-139">Normale interno</span><span class="sxs-lookup"><span data-stu-id="c4933-139">Normal Indoors</span></span>     | <span data-ttu-id="c4933-140">401</span><span class="sxs-lookup"><span data-stu-id="c4933-140">401</span></span>        | <span data-ttu-id="c4933-141">1000</span><span class="sxs-lookup"><span data-stu-id="c4933-141">1000</span></span>     | <span data-ttu-id="c4933-142">700</span><span class="sxs-lookup"><span data-stu-id="c4933-142">700</span></span>              | <span data-ttu-id="c4933-143">5</span><span class="sxs-lookup"><span data-stu-id="c4933-143">5</span></span>             |
| <span data-ttu-id="c4933-144">Interni luminosi</span><span class="sxs-lookup"><span data-stu-id="c4933-144">Bright Indoors</span></span>     | <span data-ttu-id="c4933-145">1001</span><span class="sxs-lookup"><span data-stu-id="c4933-145">1001</span></span>       | <span data-ttu-id="c4933-146">5000</span><span class="sxs-lookup"><span data-stu-id="c4933-146">5000</span></span>     | <span data-ttu-id="c4933-147">3000</span><span class="sxs-lookup"><span data-stu-id="c4933-147">3000</span></span>             | <span data-ttu-id="c4933-148">6</span><span class="sxs-lookup"><span data-stu-id="c4933-148">6</span></span>             |
| <span data-ttu-id="c4933-149">Dim all'esterno</span><span class="sxs-lookup"><span data-stu-id="c4933-149">Dim Outdoors</span></span>       | <span data-ttu-id="c4933-150">5001</span><span class="sxs-lookup"><span data-stu-id="c4933-150">5001</span></span>       | <span data-ttu-id="c4933-151">10,000</span><span class="sxs-lookup"><span data-stu-id="c4933-151">10,000</span></span>   | <span data-ttu-id="c4933-152">7500</span><span class="sxs-lookup"><span data-stu-id="c4933-152">7500</span></span>             | <span data-ttu-id="c4933-153">7</span><span class="sxs-lookup"><span data-stu-id="c4933-153">7</span></span>             |
| <span data-ttu-id="c4933-154">Cloud all'esterno</span><span class="sxs-lookup"><span data-stu-id="c4933-154">Cloudy Outdoors</span></span>    | <span data-ttu-id="c4933-155">10.001</span><span class="sxs-lookup"><span data-stu-id="c4933-155">10,001</span></span>     | <span data-ttu-id="c4933-156">30.000</span><span class="sxs-lookup"><span data-stu-id="c4933-156">30,000</span></span>   | <span data-ttu-id="c4933-157">20.000</span><span class="sxs-lookup"><span data-stu-id="c4933-157">20,000</span></span>           | <span data-ttu-id="c4933-158">8</span><span class="sxs-lookup"><span data-stu-id="c4933-158">8</span></span>             |
| <span data-ttu-id="c4933-159">Luce solare diretta</span><span class="sxs-lookup"><span data-stu-id="c4933-159">Direct Sunlight</span></span>    | <span data-ttu-id="c4933-160">30.001</span><span class="sxs-lookup"><span data-stu-id="c4933-160">30,001</span></span>     | <span data-ttu-id="c4933-161">100,000</span><span class="sxs-lookup"><span data-stu-id="c4933-161">100,000</span></span>  | <span data-ttu-id="c4933-162">65.000</span><span class="sxs-lookup"><span data-stu-id="c4933-162">65,000</span></span>           | <span data-ttu-id="c4933-163">9</span><span class="sxs-lookup"><span data-stu-id="c4933-163">9</span></span>             |



 

<span data-ttu-id="c4933-164">Se si visualizzano questi dati usando i valori medi di questa tabella, si noterà che la relazione Lux-to-Lighting-Step non è lineare, come illustrato nel grafico seguente.</span><span class="sxs-lookup"><span data-stu-id="c4933-164">If we visualize this data by using the mean values from this table, we see that the lux-to-lighting-step relationship is not linear, as show in the following graph.</span></span>

![grafico di illuminazione lineare](images/luxtostep.png)

<span data-ttu-id="c4933-166">Tuttavia, se si visualizzano questi dati utilizzando una scala logaritmica sull'asse x, è possibile notare che emerge una relazione approssimativamente lineare.</span><span class="sxs-lookup"><span data-stu-id="c4933-166">However, if we view this data by using a logarithmic scale on the x-axis, we can see that a roughly linear relationship emerges.</span></span>

![grafico di illuminazione logaritmica](images/luxlogtostep.png)

### <a name="an-example-transform"></a><span data-ttu-id="c4933-168">Trasformazione di esempio</span><span class="sxs-lookup"><span data-stu-id="c4933-168">An Example Transform</span></span>

<span data-ttu-id="c4933-169">In base al set di dati di esempio per i sensori di luce di ambiente forniti in precedenza, è possibile arrivare all'equazione seguente per eseguire il mapping dei valori Lux alla percezione umana.</span><span class="sxs-lookup"><span data-stu-id="c4933-169">Based on the sample data set for ambient light sensors previously provided, you could arrive at the following equation to map lux values to human perception.</span></span> <span data-ttu-id="c4933-170">In questo esempio, i valori previsti variano da 0 Lux a 1 milione Lux.</span><span class="sxs-lookup"><span data-stu-id="c4933-170">In this example, the expected values range from 0 lux to 1,000,000 lux.</span></span>

![equazione valore LUX](images/sensor-lux-equation.jpg)

<span data-ttu-id="c4933-172">Questa equazione restituisce valori che variano in modo approssimativamente lineare tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="c4933-172">This equation results in values that vary in a roughly linear fashion between 0.0 and 1.0.</span></span> <span data-ttu-id="c4933-173">Questo risultato indica il modo in cui l'illuminazione percepita dall'uomo è cambiata in base al set di dati di esempio illustrato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c4933-173">This result indicates how human-perceived lighting changed based on the example data set that was shown previously.</span></span>

 

 



