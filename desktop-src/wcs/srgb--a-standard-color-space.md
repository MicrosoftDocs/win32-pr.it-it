---
title: sRGB uno spazio colore standard
description: A causa delle considerazioni sulla larghezza di banda di Internet, Hewlett-Packard e Microsoft hanno proposto l'adozione di uno spazio dei colori predefinito standard noto come sRGB (IEC 61966-2-1), in modo da consentire un mapping accurato dei colori con un sovraccarico di dati molto ridotto.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Windows Color System (WCS), spazio colore sRGB
- WCS (sistema di colori Windows), spazio colore sRGB
- Gestione colori immagine, spazio colore sRGB
- gestione dei colori, spazio colore sRGB
- colori, spazio colore sRGB
- spazio colore sRGB
- spazi colore, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3167e44f149982a809826bcb9b64b3ec6e3c24
ms.sourcegitcommit: da13d459791d115df883fa4dd348931d0902c2cc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/30/2021
ms.locfileid: "106320175"
---
# <a name="srgb-a-standard-color-space"></a><span data-ttu-id="25ba5-110">sRGB: uno spazio colore standard</span><span class="sxs-lookup"><span data-stu-id="25ba5-110">sRGB: A Standard Color Space</span></span>

<span data-ttu-id="25ba5-111">A causa delle considerazioni sulla larghezza di banda di Internet, Hewlett-Packard e Microsoft hanno proposto l'adozione di uno [spazio dei colori](c.md) predefinito standard noto come *sRGB* (IEC 61966-2-1), in modo da consentire un mapping accurato dei [colori](c.md) con un sovraccarico di dati molto ridotto.</span><span class="sxs-lookup"><span data-stu-id="25ba5-111">As a result of Internet bandwidth considerations, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined [color space](c.md) known as *sRGB* (IEC 61966-2-1), so as to allow accurate [color mapping](c.md) with very little data overhead.</span></span>

<span data-ttu-id="25ba5-112">Una versione del file della Guida di un white paper illustrando i dettagli tecnici di sRGB, sRGB. hlp, è disponibile nella \\ cartella della Guida di informazioni di riferimento per programmatori WCS 1,0.</span><span class="sxs-lookup"><span data-stu-id="25ba5-112">A help-file version of a white paper discussing the technical details of sRGB, sRGB.hlp, is available in the \\Help folder of the WCS 1.0 Programmer's Reference.</span></span>

<span data-ttu-id="25ba5-113">Formati di file diversi possono usare o aggiungere un flag per specificare che l'immagine è nello spazio dei colori di sRGB.</span><span class="sxs-lookup"><span data-stu-id="25ba5-113">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="25ba5-114">Nel formato DIB (Device-Independent Bitmap) di Windows, l'impostazione del membro **bV5CSType** della struttura [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) su **LCS \_ sRGB** specifica che i colori DIB si trovano nello spazio dei colori di sRGB.</span><span class="sxs-lookup"><span data-stu-id="25ba5-114">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure to **LCS\_sRGB** specifies that the DIB colors are in the sRGB color space.</span></span>

<span data-ttu-id="25ba5-115">WCS 1,0 fornisce supporto nativo per sRGB.</span><span class="sxs-lookup"><span data-stu-id="25ba5-115">WCS 1.0 provides native support for sRGB.</span></span> <span data-ttu-id="25ba5-116">Esistono due modi per usare WCS 1,0 per il rendering di un'immagine definita nello spazio dei colori sRGB:</span><span class="sxs-lookup"><span data-stu-id="25ba5-116">There are two ways to use WCS 1.0 for rendering an image defined in the sRGB color space:</span></span>

<span data-ttu-id="25ba5-117">**Per eseguire il rendering di un'immagine all'interno del contesto di dispositivo**</span><span class="sxs-lookup"><span data-stu-id="25ba5-117">**To render an image inside the device context**</span></span>

1.  <span data-ttu-id="25ba5-118">Creare un contesto di dispositivo (DC) nel dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="25ba5-118">Create a device context (DC) on the display device.</span></span>
2.  <span data-ttu-id="25ba5-119">Impostare la gestione dei colori mediante la funzione [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) .</span><span class="sxs-lookup"><span data-stu-id="25ba5-119">Set color management using the [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) function.</span></span>
3.  <span data-ttu-id="25ba5-120">Usare la funzione [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) per trasferire la DIB nel controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="25ba5-120">Use the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function to transfer the DIB into the DC.</span></span> <span data-ttu-id="25ba5-121">Fino a quando il membro **bV5CSMType** della struttura [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) è impostato su **LCS \_ sRGB**, il sistema eseguirà la gestione dei colori appropriata.</span><span class="sxs-lookup"><span data-stu-id="25ba5-121">As long as the **bV5CSMType** member of the DIBs [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure is set to **LCS\_sRGB**, the system will perform the appropriate color management.</span></span>

<span data-ttu-id="25ba5-122">**Per eseguire il rendering di un'immagine all'esterno del contesto di dispositivo**</span><span class="sxs-lookup"><span data-stu-id="25ba5-122">**To render an image outside the device context**</span></span>

1.  <span data-ttu-id="25ba5-123">Creare una trasformazione usando [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw).</span><span class="sxs-lookup"><span data-stu-id="25ba5-123">Create a transform using [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw).</span></span> <span data-ttu-id="25ba5-124">Il membro **lcsCSType** della struttura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) a cui punta il parametro *PLogColorSpace* deve essere impostato su **LCS \_ sRGB**.</span><span class="sxs-lookup"><span data-stu-id="25ba5-124">The **lcsCSType** member of the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure pointed to by the *pLogColorSpace* parameter should be set to **LCS\_sRGB**.</span></span> <span data-ttu-id="25ba5-125">Il parametro *hDestProfile* indica lo spazio dei colori del dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="25ba5-125">The *hDestProfile* parameter indicates the display device's color space.</span></span>
2.  <span data-ttu-id="25ba5-126">Usare la trasformazione colore creata per trovare la corrispondenza con il colore dell'immagine prima di visualizzarla nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25ba5-126">Use the created color transform to color match the image before displaying it on the device.</span></span>

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a><span data-ttu-id="25ba5-127">Impostazioni predefinite WCS 1,0 per spazio colore di input e profilo di output</span><span class="sxs-lookup"><span data-stu-id="25ba5-127">WCS 1.0 Defaults for Input Color Space and Output Profile</span></span>

<span data-ttu-id="25ba5-128">Quando non viene specificato alcuno spazio colore di input, per impostazione predefinita WCS 1,0 utilizza lo spazio colore sRGB come spazio colore di input per il [mapping dei colori](c.md).</span><span class="sxs-lookup"><span data-stu-id="25ba5-128">When no input color space is specified, by default WCS 1.0 uses the sRGB color space as the input color space for [color mapping](c.md).</span></span>

<span data-ttu-id="25ba5-129">Quando non viene specificato alcun profilo di output, ma viene specificato un dispositivo predefinito, WCS 1,0 seleziona un profilo di output predefinito.</span><span class="sxs-lookup"><span data-stu-id="25ba5-129">When no output profile is specified, but a default device is specified, WCS 1.0 selects a default output profile.</span></span> <span data-ttu-id="25ba5-130">Se al dispositivo predefinito non è associato un profilo, WCS 1,0 utilizza lo spazio di colore sRGB come profilo di output.</span><span class="sxs-lookup"><span data-stu-id="25ba5-130">If the default device does not have an associated profile, WCS 1.0 uses the sRGB color space as the output profile.</span></span>

<span data-ttu-id="25ba5-131">La tabella seguente illustra le trasformazioni dei colori risultanti quando non è disponibile un dispositivo predefinito.</span><span class="sxs-lookup"><span data-stu-id="25ba5-131">The following table shows the resulting color transforms when a default device is not available.</span></span>



|                                 | <span data-ttu-id="25ba5-132">Profilo di output specificato</span><span class="sxs-lookup"><span data-stu-id="25ba5-132">Output Profile Specified</span></span>                              | <span data-ttu-id="25ba5-133">Profilo di output non specificato</span><span class="sxs-lookup"><span data-stu-id="25ba5-133">Output Profile Not Specified</span></span>                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="25ba5-134">Spazio colore di input specificato</span><span class="sxs-lookup"><span data-stu-id="25ba5-134">Input Color Space Specified</span></span>     | <span data-ttu-id="25ba5-135">Transform usa i profili specificati.</span><span class="sxs-lookup"><span data-stu-id="25ba5-135">Transform uses the specified profiles.</span></span>                | <span data-ttu-id="25ba5-136">Trasforma converte dallo spazio colore di input noto a sRGB.</span><span class="sxs-lookup"><span data-stu-id="25ba5-136">Transform converts from known input color space to sRGB.</span></span> |
| <span data-ttu-id="25ba5-137">Spazio colore di input non specificato</span><span class="sxs-lookup"><span data-stu-id="25ba5-137">Input Color Space Not Specified</span></span> | <span data-ttu-id="25ba5-138">Trasforma converte da sRGB a profilo di output noto.</span><span class="sxs-lookup"><span data-stu-id="25ba5-138">Transform converts from sRGB to known output profile.</span></span> | <span data-ttu-id="25ba5-139">Si presuppone la trasformazione da sRGB a sRGB; non viene eseguita alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="25ba5-139">Transform from sRGB to sRGB is assumed; nothing is done.</span></span> |



 

## <a name="srgb-and-embedded-profiles"></a><span data-ttu-id="25ba5-140">Profili sRGB e incorporati</span><span class="sxs-lookup"><span data-stu-id="25ba5-140">sRGB and Embedded Profiles</span></span>

<span data-ttu-id="25ba5-141">A partire da ICM versione 2,0, le applicazioni che utilizzano WCS possono incorporare i profili nelle immagini.</span><span class="sxs-lookup"><span data-stu-id="25ba5-141">Beginning with ICM version 2.0, applications that utilize WCS can embed profiles in images.</span></span> <span data-ttu-id="25ba5-142">I profili incorporati consentono alle applicazioni degli utenti di mantenere un aspetto coerente dei colori anche se le immagini vengono trasmesse attraverso Internet.</span><span class="sxs-lookup"><span data-stu-id="25ba5-142">Embedded profiles assist users' applications in maintaining a consistent color appearance even if images are transmitted across the Internet.</span></span>

<span data-ttu-id="25ba5-143">Le immagini che usano lo spazio dei colori sRGB non necessitano di un profilo colori incorporato.</span><span class="sxs-lookup"><span data-stu-id="25ba5-143">Images that use the sRGB color space do not need an embedded color profile.</span></span> <span data-ttu-id="25ba5-144">Poiché non dispongono di un profilo incorporato, le immagini basate su sRGB sono più piccole e più facilmente trasferibili tra canali di dati con una larghezza di banda limitata.</span><span class="sxs-lookup"><span data-stu-id="25ba5-144">Because they have no embedded profile, sRGB-based images are smaller and more readily transferable across data channels with limited bandwidth.</span></span>

<span data-ttu-id="25ba5-145">Le applicazioni devono impostare il flag **LCS \_ sRGB** nell'intestazione bitmap dell'immagine per indicare che l'immagine usa lo spazio dei colori di sRGB.</span><span class="sxs-lookup"><span data-stu-id="25ba5-145">Applications should set the **LCS\_sRGB** flag in the image's bitmap header to indicate that the image uses the sRGB color space.</span></span> <span data-ttu-id="25ba5-146">Per informazioni dettagliate, vedere [strutture di intestazione bitmap di Windows](using-structures-in-wcs-1-0.md) e [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span><span class="sxs-lookup"><span data-stu-id="25ba5-146">For details, see [Windows Bitmap Header Structures](using-structures-in-wcs-1-0.md) and [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span></span>

 

 