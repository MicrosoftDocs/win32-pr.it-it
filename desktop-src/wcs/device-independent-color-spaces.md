---
title: Spazi colori Device-Independent
description: Riconoscendo la necessità di misure di colore standard, indipendenti dal dispositivo, la Commissione International de Eclairage (International Commission on Illumination), o CIE, ha creato uno spazio di colore basato su \ 0034; Imagine \ 0034; colori primari.
ms.assetid: 8597dad3-1eb8-49f9-9843-1f9068a65925
keywords:
- Windows Color System (WCS), spazi dei colori indipendenti dal dispositivo
- WCS (Windows Color System), spazi dei colori indipendenti dal dispositivo
- Gestione colori immagine, spazi colori indipendenti dal dispositivo
- gestione dei colori, spazi dei colori indipendenti dal dispositivo
- colori, spazi dei colori indipendenti dal dispositivo
- spazi dei colori, indipendenti dal dispositivo
- spazi dei colori indipendenti dal dispositivo
- Commission International de Eclairage (CIE)
- International Commission on illuminazione (CIE)
- CIE (Commission International de Eclairage)
- CIE (International Commission on Illumination)
- Spazio colore CIE XYZ
- Area colore XYZ
- spazio colore sRGB
- spazi colore, CIE XYZ
- spazi colore, sRGB
- spazi colore, XYZ
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d044379f8f04467f7be94f09d1eb1fa41816d3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2021
ms.locfileid: "106320144"
---
# <a name="device-independent-color-spaces"></a><span data-ttu-id="9415c-120">Spazi colori Device-Independent</span><span class="sxs-lookup"><span data-stu-id="9415c-120">Device-Independent Color Spaces</span></span>

<span data-ttu-id="9415c-121">Riconoscendo la necessità di misure di colore standard e indipendenti dal dispositivo, la Commissione International de Eclairage (International Commission on Illumination), o CIE, ha creato uno [spazio di colore](c.md) basato su [colori primari](p.md)"immaginari".</span><span class="sxs-lookup"><span data-stu-id="9415c-121">Recognizing the need for standard, device-independent color measurements, the Commission International de l'Eclairage (International Commission on Illumination), or CIE, created a [color space](c.md) based on "imaginary" [primary colors](p.md).</span></span> <span data-ttu-id="9415c-122">Non sono previsti dispositivi reali per produrre colori in questo spazio colore.</span><span class="sxs-lookup"><span data-stu-id="9415c-122">No actual device is expected to produce colors in this color space.</span></span> <span data-ttu-id="9415c-123">Viene usato come mezzo per convertire i colori da uno spazio colore a un altro.</span><span class="sxs-lookup"><span data-stu-id="9415c-123">It is used as a means of converting colors from one color space to another.</span></span> <span data-ttu-id="9415c-124">I colori primari in questo spazio colore sono i colori astratti X, Y e Z.</span><span class="sxs-lookup"><span data-stu-id="9415c-124">The primary colors in this color space are the abstract colors X, Y, and Z.</span></span>

<span data-ttu-id="9415c-125">Lo spazio colore CIE XYZ 1931 viene ampiamente usato come base per la conversione dello spazio colore.</span><span class="sxs-lookup"><span data-stu-id="9415c-125">The 1931 CIEXYZ color space is widely used as the basis for color space conversion.</span></span> <span data-ttu-id="9415c-126">Con la crescita di Internet, tuttavia, le considerazioni sulla larghezza di banda hanno reso lo spazio dei colori XYZ poco ingombrante.</span><span class="sxs-lookup"><span data-stu-id="9415c-126">With the rise of the Internet, however, bandwidth considerations have made the XYZ color space unwieldy.</span></span> <span data-ttu-id="9415c-127">Lo scambio di immagini con la larghezza di banda limitata di Internet richiede un modello di [colore](c.md)più compatto.</span><span class="sxs-lookup"><span data-stu-id="9415c-127">The exchange of images over the limited bandwidth of the Internet necessitates a more compact [color model](c.md).</span></span>

<span data-ttu-id="9415c-128">Di conseguenza, Hewlett-Packard e Microsoft hanno proposto l'adozione di uno spazio di colore RGB predefinito standard noto come sRGB, in modo da consentire una gestione dei colori accurata con un sovraccarico di dati molto ridotto.</span><span class="sxs-lookup"><span data-stu-id="9415c-128">As a result, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined RGB color space known as sRGB, so as to allow accurate color management with very little data overhead.</span></span> <span data-ttu-id="9415c-129">Questo standard è stato approvato come standard internazionale formale dal International Electrotechnical Commission (IEC) come IEC 61966-2-1: sistemi multimediali e EquipmentColour Measurement e ManagementPart 2-1: color ManagementDefault RGB Color Space.</span><span class="sxs-lookup"><span data-stu-id="9415c-129">This standard has been approved as a formal international standard by the International Electrotechnical Commission (IEC) as IEC 61966-2-1: Multimedia Systems and EquipmentColour Measurement and ManagementPart 2-1: Colour ManagementDefault RGB Colour Space.</span></span> <span data-ttu-id="9415c-130">È disponibile direttamente da IEC all'indirizzo <https://www.iec.ch/> .</span><span class="sxs-lookup"><span data-stu-id="9415c-130">It is available directly from the IEC at <https://www.iec.ch/>.</span></span> <span data-ttu-id="9415c-131">Informazioni sui problemi tecnici relativi a sRGB sono disponibili su Internet all'indirizzo:</span><span class="sxs-lookup"><span data-stu-id="9415c-131">Information discussing the technical issues involved in sRGB is available on the Internet at:</span></span>

[<span data-ttu-id="9415c-132">Uno spazio di colore predefinito standard per Internet-sRGB</span><span class="sxs-lookup"><span data-stu-id="9415c-132">A Standard Default Color Space for the Internet - sRGB</span></span>](https://www.w3.org/Graphics/Color/sRGB.html)

<span data-ttu-id="9415c-133">Una versione del file della Guida di un white paper illustrare i problemi tecnici correlati a sRGB, sRGB. HLP, è disponibile nella \\ cartella della guida del riferimento per programmatori WCS 1,0 in Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="9415c-133">A help-file version of a white paper discussing the technical issues involved in sRGB, sRGB.HLP, is available in the \\Help folder of the WCS 1.0 Programmer's Reference in the Platform SDK.</span></span>

<span data-ttu-id="9415c-134">Formati di file diversi possono usare o aggiungere un flag per specificare che l'immagine è nello spazio dei colori di sRGB.</span><span class="sxs-lookup"><span data-stu-id="9415c-134">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="9415c-135">Nel formato DIB (Device-Independent Bitmap) di Windows, l'impostazione del membro **bV5CSType** della struttura [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) su LCS \_ sRGB specifica che i colori DIB si trovano nello spazio dei colori di sRGB.</span><span class="sxs-lookup"><span data-stu-id="9415c-135">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) structure to LCS\_sRGB specifies that the DIB colors are in the sRGB color space.</span></span>

 

 




