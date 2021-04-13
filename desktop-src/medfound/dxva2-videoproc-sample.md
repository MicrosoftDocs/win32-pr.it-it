---
description: Mostra come usare l'elaborazione video di DXVA.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: Esempio DXVA2_VideoProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8497a241baf07b76148a5bc2e7ddb4dd5e878e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342496"
---
# <a name="dxva2_videoproc-sample"></a><span data-ttu-id="e5079-103">\_Esempio DXVA2 VideoProc</span><span class="sxs-lookup"><span data-stu-id="e5079-103">DXVA2\_VideoProc Sample</span></span>

<span data-ttu-id="e5079-104">Mostra come usare l' [elaborazione video di DXVA](dxva-video-processing.md).</span><span class="sxs-lookup"><span data-stu-id="e5079-104">Shows how to use [DXVA Video Processing](dxva-video-processing.md).</span></span>

<span data-ttu-id="e5079-105">Questo esempio genera video a livello di codice con un flusso primario e un sottoflusso.</span><span class="sxs-lookup"><span data-stu-id="e5079-105">This sample programmatically generates video with a primary stream and a substream.</span></span> <span data-ttu-id="e5079-106">Il flusso primario Visualizza le barre dei colori SMPTE e il sottoflusso è un rettangolo semitrasparente.</span><span class="sxs-lookup"><span data-stu-id="e5079-106">The primary stream displays SMPTE color bars, and the substream is a semi-transparent rectangle.</span></span> <span data-ttu-id="e5079-107">Il video viene quindi elaborato e visualizzato usando un processore video DXVA.</span><span class="sxs-lookup"><span data-stu-id="e5079-107">The video is then processed and displayed using a DXVA video processor.</span></span> <span data-ttu-id="e5079-108">L'utente può modificare i valori alfa planari, i rettangoli di origine e di destinazione, le regolazioni dei colori e lo spazio colore.</span><span class="sxs-lookup"><span data-stu-id="e5079-108">The user can change the planar alpha values, source and destination rectangles, color adjustments, and color space.</span></span>

![screenshot dell'esempio dxva2 \- videoproc](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="e5079-110">API illustrate</span><span class="sxs-lookup"><span data-stu-id="e5079-110">APIs Demonstrated</span></span>

<span data-ttu-id="e5079-111">In questo esempio vengono illustrate le interfacce DXVA seguenti:</span><span class="sxs-lookup"><span data-stu-id="e5079-111">This sample demonstrates the following DXVA interfaces:</span></span>

-   [<span data-ttu-id="e5079-112">**IDirectXVideoProcessorService**</span><span class="sxs-lookup"><span data-stu-id="e5079-112">**IDirectXVideoProcessorService**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [<span data-ttu-id="e5079-113">**IDirectXVideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="e5079-113">**IDirectXVideoProcessor**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a><span data-ttu-id="e5079-114">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="e5079-114">Usage</span></span>

<span data-ttu-id="e5079-115">L' \_ esempio DXVA2 VideoProc compila un'applicazione Windows.</span><span class="sxs-lookup"><span data-stu-id="e5079-115">The DXVA2\_VideoProc sample builds a Windows application.</span></span>

<span data-ttu-id="e5079-116">Opzioni della riga di comando:</span><span class="sxs-lookup"><span data-stu-id="e5079-116">Command line options:</span></span>



| <span data-ttu-id="e5079-117">Opzione</span><span class="sxs-lookup"><span data-stu-id="e5079-117">Option</span></span> | <span data-ttu-id="e5079-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5079-118">Description</span></span>                                                                          |
|--------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e5079-119">-HH</span><span class="sxs-lookup"><span data-stu-id="e5079-119">-hh</span></span>    | <span data-ttu-id="e5079-120">Impone all'applicazione di usare un dispositivo Direct3D hardware e un dispositivo DXVA hardware.</span><span class="sxs-lookup"><span data-stu-id="e5079-120">Forces the application to use a hardware Direct3D device and a hardware DXVA device.</span></span> |
| <span data-ttu-id="e5079-121">-HS</span><span class="sxs-lookup"><span data-stu-id="e5079-121">-hs</span></span>    | <span data-ttu-id="e5079-122">Impone all'applicazione di usare un dispositivo Direct3D hardware e un dispositivo DXVA software.</span><span class="sxs-lookup"><span data-stu-id="e5079-122">Forces the application to use a hardware Direct3D device and a software DXVA device.</span></span> |
| <span data-ttu-id="e5079-123">-ss</span><span class="sxs-lookup"><span data-stu-id="e5079-123">-ss</span></span>    | <span data-ttu-id="e5079-124">Impone all'applicazione di usare un dispositivo Direct3D software e un dispositivo DXVA software.</span><span class="sxs-lookup"><span data-stu-id="e5079-124">Forces the application to use a software Direct3D device and a software DXVA device.</span></span> |



 

<span data-ttu-id="e5079-125">Comandi da tastiera:</span><span class="sxs-lookup"><span data-stu-id="e5079-125">Keyboard commands:</span></span>



| <span data-ttu-id="e5079-126">Chiave</span><span class="sxs-lookup"><span data-stu-id="e5079-126">Key</span></span>       | <span data-ttu-id="e5079-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5079-127">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="e5079-128">ALT+INVIO</span><span class="sxs-lookup"><span data-stu-id="e5079-128">ALT+ENTER</span></span> | <span data-ttu-id="e5079-129">Passa tra la modalità finestra e la modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="e5079-129">Switch between windowed mode and full-screen mode.</span></span>      |
| <span data-ttu-id="e5079-130">F1 – F8</span><span class="sxs-lookup"><span data-stu-id="e5079-130">F1–F8</span></span>     | <span data-ttu-id="e5079-131">Immettere una delle modalità illustrate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e5079-131">Enter one of the modes shown in the following table.</span></span>    |
| <span data-ttu-id="e5079-132">FINE</span><span class="sxs-lookup"><span data-stu-id="e5079-132">END</span></span>       | <span data-ttu-id="e5079-133">Abilita o Disabilita la registrazione del debug per i frame eliminati.</span><span class="sxs-lookup"><span data-stu-id="e5079-133">Enable or disable debugging logging for dropped frames.</span></span> |
| <span data-ttu-id="e5079-134">HOME</span><span class="sxs-lookup"><span data-stu-id="e5079-134">HOME</span></span>      | <span data-ttu-id="e5079-135">Reimposta un parametro sul valore iniziale.</span><span class="sxs-lookup"><span data-stu-id="e5079-135">Reset a parameter to its initial value.</span></span>                 |



 

<span data-ttu-id="e5079-136">Ogni tasto funzione da F1 a F8 passa a una modalità in cui è possibile usare i tasti di direzione per modificare un determinato parametro di rendering.</span><span class="sxs-lookup"><span data-stu-id="e5079-136">Each of the function keys F1 through F8 switches to a mode in which the arrow keys can be used to adjust a particular rendering parameter.</span></span> <span data-ttu-id="e5079-137">Inoltre, il colore del sottoflusso cambia.</span><span class="sxs-lookup"><span data-stu-id="e5079-137">In addition, the color of the substream changes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5079-138">Chiave</span><span class="sxs-lookup"><span data-stu-id="e5079-138">Key</span></span></th>
<th><span data-ttu-id="e5079-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5079-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5079-140">F1</span><span class="sxs-lookup"><span data-stu-id="e5079-140">F1</span></span></td>
<td><span data-ttu-id="e5079-141">Modificare i valori alfa.</span><span class="sxs-lookup"><span data-stu-id="e5079-141">Adjust the alpha values.</span></span><br/>
<ul>
<li><span data-ttu-id="e5079-142">UP: aumenta l'alfa planare di entrambi i flussi.</span><span class="sxs-lookup"><span data-stu-id="e5079-142">UP: Increase the planar alpha of both streams.</span></span></li>
<li><span data-ttu-id="e5079-143">DOWN: riduce l'alfa planare di entrambi i flussi.</span><span class="sxs-lookup"><span data-stu-id="e5079-143">DOWN: Decrease the planar alpha of both streams.</span></span></li>
<li><span data-ttu-id="e5079-144">RIGHT: aumentare il pixel alfa del sottoflusso.</span><span class="sxs-lookup"><span data-stu-id="e5079-144">RIGHT: Increase the pixel alpha of the substream.</span></span></li>
<li><span data-ttu-id="e5079-145">LEFT: riduce il pixel alfa del sottoflusso.</span><span class="sxs-lookup"><span data-stu-id="e5079-145">LEFT: Decrease the pixel alpha of the substream.</span></span></li>
</ul>
<span data-ttu-id="e5079-146">Colore flusso substream: bianco</span><span class="sxs-lookup"><span data-stu-id="e5079-146">Substream color: White</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5079-147">F2</span><span class="sxs-lookup"><span data-stu-id="e5079-147">F2</span></span></td>
<td><span data-ttu-id="e5079-148">Modificare l'area di origine del flusso primario (zoom).</span><span class="sxs-lookup"><span data-stu-id="e5079-148">Adjust the primary stream's source area (zoom).</span></span><br/>
<ul>
<li><span data-ttu-id="e5079-149">UP: aumenta verticalmente (zoom avanti).</span><span class="sxs-lookup"><span data-stu-id="e5079-149">UP: Increase vertically (zoom in).</span></span></li>
<li><span data-ttu-id="e5079-150">DOWN: riduzione verticale (zoom indietro).</span><span class="sxs-lookup"><span data-stu-id="e5079-150">DOWN: Decrease vertically (zoom out).</span></span></li>
<li><span data-ttu-id="e5079-151">RIGHT: aumenta orizzontalmente (zoom avanti).</span><span class="sxs-lookup"><span data-stu-id="e5079-151">RIGHT: Increase horizontally (zoom in).</span></span></li>
<li><span data-ttu-id="e5079-152">LEFT: decrementa orizzontalmente (zoom indietro).</span><span class="sxs-lookup"><span data-stu-id="e5079-152">LEFT: Decrease horizontally (zoom out).</span></span></li>
</ul>
<span data-ttu-id="e5079-153">Colore flusso substream: rosso</span><span class="sxs-lookup"><span data-stu-id="e5079-153">Substream color: Red</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5079-154">F3</span><span class="sxs-lookup"><span data-stu-id="e5079-154">F3</span></span></td>
<td><span data-ttu-id="e5079-155">Spostare l'area di origine del flusso primario.</span><span class="sxs-lookup"><span data-stu-id="e5079-155">Move the primary stream's source area.</span></span><br/>
<ul>
<li><span data-ttu-id="e5079-156">SU: sposta su.</span><span class="sxs-lookup"><span data-stu-id="e5079-156">UP: Move up.</span></span></li>
<li><span data-ttu-id="e5079-157">GIÙ: Sposta giù.</span><span class="sxs-lookup"><span data-stu-id="e5079-157">DOWN: Move down.</span></span></li>
<li><span data-ttu-id="e5079-158">A destra: sposta a destra.</span><span class="sxs-lookup"><span data-stu-id="e5079-158">RIGHT: Move right.</span></span></li>
<li><span data-ttu-id="e5079-159">LEFT: sposta a sinistra.</span><span class="sxs-lookup"><span data-stu-id="e5079-159">LEFT: Move left.</span></span></li>
</ul>
<span data-ttu-id="e5079-160">Colore flusso substream: giallo</span><span class="sxs-lookup"><span data-stu-id="e5079-160">Substream color: Yellow</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5079-161">F4</span><span class="sxs-lookup"><span data-stu-id="e5079-161">F4</span></span></td>
<td><span data-ttu-id="e5079-162">Modificare l'area di destinazione del flusso primario.</span><span class="sxs-lookup"><span data-stu-id="e5079-162">Adjust the primary stream's destination area.</span></span><br/>
<ul>
<li><span data-ttu-id="e5079-163">UP: aumento verticale.</span><span class="sxs-lookup"><span data-stu-id="e5079-163">UP: Increase vertically.</span></span></li>
<li><span data-ttu-id="e5079-164">DOWN: riduzione verticale.</span><span class="sxs-lookup"><span data-stu-id="e5079-164">DOWN: Decrease vertically.</span></span></li>
<li><span data-ttu-id="e5079-165">RIGHT: aumenta orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="e5079-165">RIGHT: Increase horizontally.</span></span></li>
<li><span data-ttu-id="e5079-166">LEFT: diminuisce orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="e5079-166">LEFT: Decrease horizontally.</span></span></li>
</ul>
<span data-ttu-id="e5079-167">Colore flusso substream: verde</span><span class="sxs-lookup"><span data-stu-id="e5079-167">Substream color: Green</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5079-168">F5</span><span class="sxs-lookup"><span data-stu-id="e5079-168">F5</span></span></td>
<td><span data-ttu-id="e5079-169">Spostare l'area di destinazione del flusso primario.</span><span class="sxs-lookup"><span data-stu-id="e5079-169">Move the primary stream's destination area.</span></span><br/>
<ul>
<li><span data-ttu-id="e5079-170">SU: sposta su.</span><span class="sxs-lookup"><span data-stu-id="e5079-170">UP: Move up.</span></span></li>
<li><span data-ttu-id="e5079-171">GIÙ: Sposta giù.</span><span class="sxs-lookup"><span data-stu-id="e5079-171">DOWN: Move down.</span></span></li>
<li><span data-ttu-id="e5079-172">A destra: sposta a destra.</span><span class="sxs-lookup"><span data-stu-id="e5079-172">RIGHT: Move right.</span></span></li>
<li><span data-ttu-id="e5079-173">LEFT: sposta a sinistra.</span><span class="sxs-lookup"><span data-stu-id="e5079-173">LEFT: Move left.</span></span></li>
</ul>
<span data-ttu-id="e5079-174">Colore flusso substream: ciano</span><span class="sxs-lookup"><span data-stu-id="e5079-174">Substream color: Cyan</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5079-175">F6</span><span class="sxs-lookup"><span data-stu-id="e5079-175">F6</span></span></td>
<td><span data-ttu-id="e5079-176">Modificare il colore di sfondo o lo spazio colore.</span><span class="sxs-lookup"><span data-stu-id="e5079-176">Change background color or color space.</span></span><br/>
<ul>
<li><span data-ttu-id="e5079-177">Verso l'alto, verso il basso: scorrere gli spazi dei colori.</span><span class="sxs-lookup"><span data-stu-id="e5079-177">UP, DOWN: Cycle through color spaces.</span></span></li>
<li><span data-ttu-id="e5079-178">RIGHT, LEFT: scorre i colori di sfondo.</span><span class="sxs-lookup"><span data-stu-id="e5079-178">RIGHT, LEFT: Cycle through background colors.</span></span></li>
</ul>
<span data-ttu-id="e5079-179">Colore flusso substream: blu</span><span class="sxs-lookup"><span data-stu-id="e5079-179">Substream color: Blue</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5079-180">F7</span><span class="sxs-lookup"><span data-stu-id="e5079-180">F7</span></span></td>
<td><span data-ttu-id="e5079-181">Regolazione della luminosità e del contrasto.</span><span class="sxs-lookup"><span data-stu-id="e5079-181">Adjust brightness and contrast.</span></span><br/>
<ul>
<li><span data-ttu-id="e5079-182">UP: aumento della luminosità.</span><span class="sxs-lookup"><span data-stu-id="e5079-182">UP: Increase brightness.</span></span></li>
<li><span data-ttu-id="e5079-183">GIÙ: Diminuisci luminosità.</span><span class="sxs-lookup"><span data-stu-id="e5079-183">DOWN: Decrease brightness.</span></span></li>
<li><span data-ttu-id="e5079-184">RIGHT: aumenta il contrasto.</span><span class="sxs-lookup"><span data-stu-id="e5079-184">RIGHT: Increase contrast.</span></span></li>
<li><span data-ttu-id="e5079-185">LEFT: Riduci contrasto.</span><span class="sxs-lookup"><span data-stu-id="e5079-185">LEFT: Decrease contrast.</span></span></li>
</ul>
<span data-ttu-id="e5079-186">Colore flusso substream: Magenta</span><span class="sxs-lookup"><span data-stu-id="e5079-186">Substream color: Magenta</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5079-187">F8</span><span class="sxs-lookup"><span data-stu-id="e5079-187">F8</span></span></td>
<td><span data-ttu-id="e5079-188">Regolare la tonalità e la saturazione.</span><span class="sxs-lookup"><span data-stu-id="e5079-188">Adjust hue and saturation.</span></span><br/>
<ul>
<li><span data-ttu-id="e5079-189">SU: aumenta tonalità.</span><span class="sxs-lookup"><span data-stu-id="e5079-189">UP: Increase hue.</span></span></li>
<li><span data-ttu-id="e5079-190">GIÙ: Diminuisci tonalità.</span><span class="sxs-lookup"><span data-stu-id="e5079-190">DOWN: Decrease hue.</span></span></li>
<li><span data-ttu-id="e5079-191">RIGHT: aumenta la saturazione.</span><span class="sxs-lookup"><span data-stu-id="e5079-191">RIGHT: Increase saturation.</span></span></li>
<li><span data-ttu-id="e5079-192">LEFT: riduzione della saturazione.</span><span class="sxs-lookup"><span data-stu-id="e5079-192">LEFT: Decrease saturation.</span></span></li>
</ul>
<span data-ttu-id="e5079-193">Colore sottoflusso: nero</span><span class="sxs-lookup"><span data-stu-id="e5079-193">Substream color: Black</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e5079-194">In ogni modalità la pressione del tasto HOME consente di reimpostare i parametri per tale modalità sui valori iniziali.</span><span class="sxs-lookup"><span data-stu-id="e5079-194">In each mode, pressing the HOME key resets the parameters for that mode to their initial values.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5079-195">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5079-195">Requirements</span></span>



| <span data-ttu-id="e5079-196">Prodotto</span><span class="sxs-lookup"><span data-stu-id="e5079-196">Product</span></span>                                                        | <span data-ttu-id="e5079-197">Versione</span><span class="sxs-lookup"><span data-stu-id="e5079-197">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="e5079-198">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="e5079-198">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="e5079-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e5079-199">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="e5079-200">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="e5079-200">Downloading the Sample</span></span>

<span data-ttu-id="e5079-201">Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).</span><span class="sxs-lookup"><span data-stu-id="e5079-201">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5079-202">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5079-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5079-203">Accelerazione video DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="e5079-203">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="e5079-204">Elaborazione video DXVA</span><span class="sxs-lookup"><span data-stu-id="e5079-204">DXVA Video Processing</span></span>](dxva-video-processing.md)
</dt> <dt>

[<span data-ttu-id="e5079-205">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="e5079-205">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




