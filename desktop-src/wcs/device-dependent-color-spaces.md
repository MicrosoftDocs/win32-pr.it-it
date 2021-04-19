---
title: Spazi colori Device-Dependent
description: La maggior parte degli spazi dei colori dipende dal dispositivo.
ms.assetid: 657ec64b-8605-4d05-a7d6-9f8bb71e6a71
keywords:
- Windows Color System (WCS), spazi dei colori dipendenti dal dispositivo
- WCS (Windows Color System), spazi dei colori dipendenti dal dispositivo
- Gestione colori immagine, spazi colore dipendenti dal dispositivo
- gestione dei colori, spazi dei colori dipendenti dal dispositivo
- colori, spazi dei colori dipendenti dal dispositivo
- spazi dei colori, dipendenti dal dispositivo
- spazi dei colori dipendenti dal dispositivo
- punto bianco
- coloranti
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1523ee6ba81dcdc3b69a468546871cfd21913
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2021
ms.locfileid: "106320145"
---
# <a name="device-dependent-color-spaces"></a><span data-ttu-id="a2af9-112">Spazi colori Device-Dependent</span><span class="sxs-lookup"><span data-stu-id="a2af9-112">Device-Dependent Color Spaces</span></span>

<span data-ttu-id="a2af9-113">La maggior parte degli [spazi dei colori](c.md) dipende dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a2af9-113">Most [color spaces](c.md) are device dependent.</span></span> <span data-ttu-id="a2af9-114">Anche se un particolare dispositivo, ad esempio una stampante, può utilizzare lo spazio colore CMYK, i colori per i quali viene eseguito il rendering di valori CMYK specifici sono spesso leggermente diversi da tutti gli altri tipi di stampanti.</span><span class="sxs-lookup"><span data-stu-id="a2af9-114">Even though a particular device, such as a printer, may use the CMYK color space, the colors it renders for specific CMYK values are often slightly different than all other types of printers..</span></span> <span data-ttu-id="a2af9-115">È precisamente per questo motivo che il sistema di gestione dei colori WCS 1,0 è molto utile.</span><span class="sxs-lookup"><span data-stu-id="a2af9-115">It is precisely for this reason that the WCS 1.0 color management system is so useful.</span></span>

<span data-ttu-id="a2af9-116">Tutti gli spazi dei colori hanno un *punto bianco*, definito come il bianco bianco che può essere prodotto in tale spazio colore.</span><span class="sxs-lookup"><span data-stu-id="a2af9-116">All color spaces have a *white point*, which is defined as the whitest white that can be produced in that color space.</span></span> <span data-ttu-id="a2af9-117">Poiché i dispositivi possono differire gli uni dagli altri, anche i punti vuoti possono variare.</span><span class="sxs-lookup"><span data-stu-id="a2af9-117">Since devices can differ from one another, their white points can also differ.</span></span> <span data-ttu-id="a2af9-118">Tutti i colori che un dispositivo può produrre sono relativi al punto bianco.</span><span class="sxs-lookup"><span data-stu-id="a2af9-118">All colors that a device can produce are relative to its white point.</span></span> <span data-ttu-id="a2af9-119">Pertanto, un sistema di gestione dei colori deve essere in grado di eseguire il mapping del punto bianco di uno spazio colore a un altro e di mantenere le posizioni relative di tutti i colori.</span><span class="sxs-lookup"><span data-stu-id="a2af9-119">Therefore, a color management system must be able to map the white point of one color space into another and preserve the relative locations of all colors.</span></span> <span data-ttu-id="a2af9-120">Deve inoltre essere in grado di eseguire il mapping di un colore in uno spazio dei colori alla corrispondenza più vicina in un altro spazio di colore indipendentemente dalle differenze nei punti vuoti.</span><span class="sxs-lookup"><span data-stu-id="a2af9-120">It must also be able to map a color in one color space to its closest match in another color space regardless of the differences in the white points.</span></span> <span data-ttu-id="a2af9-121">WCS 1,0 è in grado di eseguire entrambe queste attività.</span><span class="sxs-lookup"><span data-stu-id="a2af9-121">WCS 1.0 is able to accomplish both of these tasks.</span></span>

<span data-ttu-id="a2af9-122">Lo spazio colore RGB viene spesso utilizzato nei monitoraggi computer.</span><span class="sxs-lookup"><span data-stu-id="a2af9-122">The RGB color space is often used on computer monitors.</span></span> <span data-ttu-id="a2af9-123">Di conseguenza, è dipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a2af9-123">As such, it is device dependent.</span></span> <span data-ttu-id="a2af9-124">Le stampanti usano in genere i [coloranti](c.md)CMYK.</span><span class="sxs-lookup"><span data-stu-id="a2af9-124">Printers typically use CMYK [colorants](c.md).</span></span> <span data-ttu-id="a2af9-125">Ogni stampante implementa la propria versione dello spazio dei colori CMYK.</span><span class="sxs-lookup"><span data-stu-id="a2af9-125">Each printer implements its own version of the CMYK color space.</span></span> <span data-ttu-id="a2af9-126">Le immagini digitali potrebbero non archiviare effettivamente i colori.</span><span class="sxs-lookup"><span data-stu-id="a2af9-126">Digital images may not actually store colors in them.</span></span> <span data-ttu-id="a2af9-127">Potrebbero archiviare i numeri degli indici in una tavolozza di colori.</span><span class="sxs-lookup"><span data-stu-id="a2af9-127">They may store index numbers into a palette of colors.</span></span> <span data-ttu-id="a2af9-128">Il risultato è che è molto difficile per gli sviluppatori di applicazioni singoli utilizzare o fornire un metodo standardizzato per lo sviluppo di immagini a colori da un dispositivo a un altro.</span><span class="sxs-lookup"><span data-stu-id="a2af9-128">The result is that it is very hard for individual application developers to use or provide a standardized method of moving color images from one device to another.</span></span> <span data-ttu-id="a2af9-129">I professionisti della creazione di immagini si riferiscono spesso alla frustrazione della creazione di un'immagine grafica sullo schermo di un computer e la loro disattivazione è molto diversa quando viene stampata</span><span class="sxs-lookup"><span data-stu-id="a2af9-129">Imaging professionals commonly experience the frustration of creating a graphic image on a computer screen and having it turn out very differently when it is printed.</span></span> <span data-ttu-id="a2af9-130">WCS 1,0 risolve queste esigenze di imaging.</span><span class="sxs-lookup"><span data-stu-id="a2af9-130">WCS 1.0 addresses these imaging needs.</span></span>

 

 




