---
title: sRGB A Spazio colori standard
description: In seguito a considerazioni sulla larghezza di banda Internet, Hewlett-Packard e Microsoft hanno proposto l'adozione di uno spazio colori predefinito standard noto come sRGB (IEC 61966-2-1), in modo da consentire un mapping dei colori accurato con un sovraccarico dei dati molto ridotto.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Windows Color System (WCS),sRGB color space
- WCS (Windows Color System),sRGB color space
- gestione colori immagine,spazio colore sRGB
- gestione dei colori, spazio colore sRGB
- colori, spazio colore sRGB
- Spazio colore sRGB
- spazi colori, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5d1b2d87cdca5424f8393ae47e592718f33985
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443642"
---
# <a name="srgb-a-standard-color-space"></a><span data-ttu-id="795ea-110">sRGB: spazio colore standard</span><span class="sxs-lookup"><span data-stu-id="795ea-110">sRGB: A Standard Color Space</span></span>

<span data-ttu-id="795ea-111">In seguito a considerazioni sulla larghezza di banda Internet, Hewlett-Packard e [](c.md) Microsoft hanno proposto l'adozione di uno spazio colori predefinito standard noto come *sRGB* (IEC 61966-2-1), in modo da consentire un [mapping](c.md) dei colori accurato con un sovraccarico dei dati molto ridotto.</span><span class="sxs-lookup"><span data-stu-id="795ea-111">As a result of Internet bandwidth considerations, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined [color space](c.md) known as *sRGB* (IEC 61966-2-1), so as to allow accurate [color mapping](c.md) with very little data overhead.</span></span>

<span data-ttu-id="795ea-112">Una versione del file della Guida di un white paper che illustra i dettagli tecnici di sRGB, sRGB.hlp, è disponibile nella cartella Guida di \\ WCS 1.0 Programmer's Reference (Guida di riferimento per programmatori WCS 1.0).</span><span class="sxs-lookup"><span data-stu-id="795ea-112">A help-file version of a white paper discussing the technical details of sRGB, sRGB.hlp, is available in the \\Help folder of the WCS 1.0 Programmer's Reference.</span></span>

<span data-ttu-id="795ea-113">Formati di file diversi possono usare o aggiungere un flag per specificare che l'immagine si trova nello spazio colore sRGB.</span><span class="sxs-lookup"><span data-stu-id="795ea-113">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="795ea-114">Nel formato DIB (Device-Independent Bitmap) di Windows, l'impostazione del membro **bV5CSType** della struttura [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) su **LCS \_ sRGB** specifica che i colori DIB sono nello spazio colori sRGB.</span><span class="sxs-lookup"><span data-stu-id="795ea-114">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure to **LCS\_sRGB** specifies that the DIB colors are in the sRGB color space.</span></span>

<span data-ttu-id="795ea-115">WCS 1.0 offre supporto nativo per sRGB.</span><span class="sxs-lookup"><span data-stu-id="795ea-115">WCS 1.0 provides native support for sRGB.</span></span> <span data-ttu-id="795ea-116">Esistono due modi per usare WCS 1.0 per il rendering di un'immagine definita nello spazio colore sRGB:</span><span class="sxs-lookup"><span data-stu-id="795ea-116">There are two ways to use WCS 1.0 for rendering an image defined in the sRGB color space:</span></span>

<span data-ttu-id="795ea-117">**Per eseguire il rendering di un'immagine all'interno del contesto di dispositivo**</span><span class="sxs-lookup"><span data-stu-id="795ea-117">**To render an image inside the device context**</span></span>

1.  <span data-ttu-id="795ea-118">Creare un contesto di dispositivo nel dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="795ea-118">Create a device context (DC) on the display device.</span></span>
2.  <span data-ttu-id="795ea-119">Impostare la gestione dei colori [**usando la funzione SetICMMode.**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)</span><span class="sxs-lookup"><span data-stu-id="795ea-119">Set color management using the [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) function.</span></span>
3.  <span data-ttu-id="795ea-120">Usare la [**funzione SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) per trasferire il DIB nel controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="795ea-120">Use the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function to transfer the DIB into the DC.</span></span> <span data-ttu-id="795ea-121">Se il membro **bV5CSMType** della struttura [**DIBs BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) è impostato su **LCS \_ sRGB,** il sistema eseguirà la gestione dei colori appropriata.</span><span class="sxs-lookup"><span data-stu-id="795ea-121">As long as the **bV5CSMType** member of the DIBs [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure is set to **LCS\_sRGB**, the system will perform the appropriate color management.</span></span>

<span data-ttu-id="795ea-122">**Per eseguire il rendering di un'immagine all'esterno del contesto di dispositivo**</span><span class="sxs-lookup"><span data-stu-id="795ea-122">**To render an image outside the device context**</span></span>

1.  <span data-ttu-id="795ea-123">Creare una trasformazione usando [**CreateColorTransformW.**](/windows/win32/api/icm/nf-icm-createcolortransformw)</span><span class="sxs-lookup"><span data-stu-id="795ea-123">Create a transform using [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw).</span></span> <span data-ttu-id="795ea-124">Il **membro lcsCSType** della struttura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) a cui punta il *parametro pLogColorSpace* deve essere impostato su **LCS \_ sRGB.**</span><span class="sxs-lookup"><span data-stu-id="795ea-124">The **lcsCSType** member of the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure pointed to by the *pLogColorSpace* parameter should be set to **LCS\_sRGB**.</span></span> <span data-ttu-id="795ea-125">Il *parametro hDestProfile* indica lo spazio colore del dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="795ea-125">The *hDestProfile* parameter indicates the display device's color space.</span></span>
2.  <span data-ttu-id="795ea-126">Usare la trasformazione colore creata in modo che il colore corrisponda all'immagine prima di visualizzarla nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="795ea-126">Use the created color transform to color match the image before displaying it on the device.</span></span>

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a><span data-ttu-id="795ea-127">Impostazioni predefinite di WCS 1.0 per lo spazio colore di input e il profilo di output</span><span class="sxs-lookup"><span data-stu-id="795ea-127">WCS 1.0 Defaults for Input Color Space and Output Profile</span></span>

<span data-ttu-id="795ea-128">Quando non viene specificato alcuno spazio colore di input, per impostazione predefinita WCS 1.0 usa lo spazio colore sRGB come spazio colore di input per il [mapping dei colori](c.md).</span><span class="sxs-lookup"><span data-stu-id="795ea-128">When no input color space is specified, by default WCS 1.0 uses the sRGB color space as the input color space for [color mapping](c.md).</span></span>

<span data-ttu-id="795ea-129">Quando non viene specificato alcun profilo di output, ma viene specificato un dispositivo predefinito, WCS 1.0 seleziona un profilo di output predefinito.</span><span class="sxs-lookup"><span data-stu-id="795ea-129">When no output profile is specified, but a default device is specified, WCS 1.0 selects a default output profile.</span></span> <span data-ttu-id="795ea-130">Se al dispositivo predefinito non è associato un profilo, WCS 1.0 usa lo spazio colore sRGB come profilo di output.</span><span class="sxs-lookup"><span data-stu-id="795ea-130">If the default device does not have an associated profile, WCS 1.0 uses the sRGB color space as the output profile.</span></span>

<span data-ttu-id="795ea-131">La tabella seguente illustra le trasformazioni di colore risultanti quando non è disponibile un dispositivo predefinito.</span><span class="sxs-lookup"><span data-stu-id="795ea-131">The following table shows the resulting color transforms when a default device is not available.</span></span>



|  &nbsp;                               | <span data-ttu-id="795ea-132">Profilo di output specificato</span><span class="sxs-lookup"><span data-stu-id="795ea-132">Output Profile Specified</span></span>                              | <span data-ttu-id="795ea-133">Profilo di output non specificato</span><span class="sxs-lookup"><span data-stu-id="795ea-133">Output Profile Not Specified</span></span>                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="795ea-134">Spazio colore di input specificato</span><span class="sxs-lookup"><span data-stu-id="795ea-134">Input Color Space Specified</span></span>     | <span data-ttu-id="795ea-135">Transform usa i profili specificati.</span><span class="sxs-lookup"><span data-stu-id="795ea-135">Transform uses the specified profiles.</span></span>                | <span data-ttu-id="795ea-136">Transform converte lo spazio colore di input noto in sRGB.</span><span class="sxs-lookup"><span data-stu-id="795ea-136">Transform converts from known input color space to sRGB.</span></span> |
| <span data-ttu-id="795ea-137">Spazio colore di input non specificato</span><span class="sxs-lookup"><span data-stu-id="795ea-137">Input Color Space Not Specified</span></span> | <span data-ttu-id="795ea-138">Transform converte da sRGB a profilo di output noto.</span><span class="sxs-lookup"><span data-stu-id="795ea-138">Transform converts from sRGB to known output profile.</span></span> | <span data-ttu-id="795ea-139">Si presuppone la trasformazione da sRGB a sRGB. non viene eseguita alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="795ea-139">Transform from sRGB to sRGB is assumed; nothing is done.</span></span> |



 

## <a name="srgb-and-embedded-profiles"></a><span data-ttu-id="795ea-140">sRGB e profili incorporati</span><span class="sxs-lookup"><span data-stu-id="795ea-140">sRGB and Embedded Profiles</span></span>

<span data-ttu-id="795ea-141">A partire da ICM versione 2.0, le applicazioni che utilizzano WCS possono incorporare i profili nelle immagini.</span><span class="sxs-lookup"><span data-stu-id="795ea-141">Beginning with ICM version 2.0, applications that utilize WCS can embed profiles in images.</span></span> <span data-ttu-id="795ea-142">I profili incorporati consentono alle applicazioni degli utenti di mantenere un aspetto di colore coerente anche se le immagini vengono trasmesse su Internet.</span><span class="sxs-lookup"><span data-stu-id="795ea-142">Embedded profiles assist users' applications in maintaining a consistent color appearance even if images are transmitted across the Internet.</span></span>

<span data-ttu-id="795ea-143">Le immagini che usano lo spazio colore sRGB non necessitano di un profilo colori incorporato.</span><span class="sxs-lookup"><span data-stu-id="795ea-143">Images that use the sRGB color space do not need an embedded color profile.</span></span> <span data-ttu-id="795ea-144">Poiché non hanno un profilo incorporato, le immagini basate su sRGB sono più piccole e più facilmente trasferibili tra i canali di dati con larghezza di banda limitata.</span><span class="sxs-lookup"><span data-stu-id="795ea-144">Because they have no embedded profile, sRGB-based images are smaller and more readily transferable across data channels with limited bandwidth.</span></span>

<span data-ttu-id="795ea-145">Le applicazioni devono impostare il flag **LCS \_ sRGB** nell'intestazione bitmap dell'immagine per indicare che l'immagine usa lo spazio colore sRGB.</span><span class="sxs-lookup"><span data-stu-id="795ea-145">Applications should set the **LCS\_sRGB** flag in the image's bitmap header to indicate that the image uses the sRGB color space.</span></span> <span data-ttu-id="795ea-146">Per informazioni dettagliate, vedere [Strutture di intestazione bitmap di Windows](using-structures-in-wcs-1-0.md) e [**LOGCOLORSPACE.**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)</span><span class="sxs-lookup"><span data-stu-id="795ea-146">For details, see [Windows Bitmap Header Structures](using-structures-in-wcs-1-0.md) and [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span></span>

 

 