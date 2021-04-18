---
description: Definisce i termini utilizzati in WIC.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Glossario componenti Windows Imaging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6812024571727c8f769df88f8233119eed13ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314472"
---
# <a name="windows-imaging-component-glossary"></a><span data-ttu-id="7cb9c-103">Glossario componenti Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="7cb9c-103">Windows Imaging Component Glossary</span></span>

## <a name="b"></a><span data-ttu-id="7cb9c-104">B</span><span class="sxs-lookup"><span data-stu-id="7cb9c-104">B</span></span>

<dl> <dt>

<span data-ttu-id="7cb9c-105">**profondità bit**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-105">**bit depth**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-106">Numero di valori dei colori che possono essere assegnati a un singolo pixel in un'immagine.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-106">The number of color values that can be assigned to a single pixel in an image.</span></span> <span data-ttu-id="7cb9c-107">La profondità del colore può variare da 1 bit (nero e bianco) a 32 bit (oltre 16,7 milioni colori).</span><span class="sxs-lookup"><span data-stu-id="7cb9c-107">Color depth can range from 1 bit (black and white) to 32 bits (over 16.7 million colors).</span></span> <span data-ttu-id="7cb9c-108">Vedere anche: profondità colore</span><span class="sxs-lookup"><span data-stu-id="7cb9c-108">See also: Color Depth</span></span>

</dd> <dt>

<span data-ttu-id="7cb9c-109">**bit per pixel (BPP)**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-109">**bits per pixel (bpp)**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-110">Numero di bit che rappresentano il valore del colore di ogni pixel in un'immagine digitalizzata.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-110">The number of bits that represent the color value of each pixel in a digitized image.</span></span> <span data-ttu-id="7cb9c-111">Vedere anche: BPP</span><span class="sxs-lookup"><span data-stu-id="7cb9c-111">See also:BPP</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="7cb9c-112">C</span><span class="sxs-lookup"><span data-stu-id="7cb9c-112">C</span></span>

<dl> <dt>

<span data-ttu-id="7cb9c-113">**Clipper**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-113">**clipper**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-114">Oggetto IWICBitmapClipper.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-114">An IWICBitmapClipper object.</span></span>

</dd> <dt>

<span data-ttu-id="7cb9c-115">**codec**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-115">**codec**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-116">Un filtro che comprime (codifica) o decomprime (Decodifica) un flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-116">A filter that compresses (encodes) or decompresses (decodes) a data stream.</span></span>

</dd> <dt>

<span data-ttu-id="7cb9c-117">**contesto colori**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-117">**color context**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-118">Astrazione per un profilo colori.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-118">An abstraction for a color profile.</span></span> <span data-ttu-id="7cb9c-119">Il profilo può essere caricato da un file (ad esempio, "sRGB Color Space Profile. ICM") o da un buffer di memoria ottenuto leggendo.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-119">The profile can be loaded from a file (ie. "sRGB Color Space Profile.icm") or from a memory buffer obtained by reading.</span></span> <span data-ttu-id="7cb9c-120">Le informazioni sul contesto dei colori sono definite dall'interfaccia IWICColorContext per WIC e vengono recuperate con il metodo GetColorContext.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-120">Color context information is defined by the IWICColorContext interface for WIC, and is retrieved with the GetColorContext method.</span></span>

</dd> <dt>

<span data-ttu-id="7cb9c-121">**trasformazione colore**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-121">**color transform**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-122">Mapping dei colori dal contesto del colore di origine al contesto del colore di destinazione in un formato pixel di output specificato.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-122">Mapping colors from the source color context to the destination color context in a given output pixel format.</span></span>

</dd> <dt>

<span data-ttu-id="7cb9c-123">**Modello colori CYMK**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-123">**CYMK color model**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-124">Spazio dei colori multidimensionali costituito dalle intensità cyan, magenta, Yellow e Black che compongono un determinato colore.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-124">Multidimensional color space consisting of the cyan, magenta, yellow, and black intensities that make up a given color.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="7cb9c-125">D</span><span class="sxs-lookup"><span data-stu-id="7cb9c-125">D</span></span>

<dl> <dt>

<span data-ttu-id="7cb9c-126">**decodificatore**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-126">**decoder**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-127">Vedere: codec</span><span class="sxs-lookup"><span data-stu-id="7cb9c-127">See Other Term: codec</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="7cb9c-128">E</span><span class="sxs-lookup"><span data-stu-id="7cb9c-128">E</span></span>

<dl> <dt>

<span data-ttu-id="7cb9c-129">**Encoder**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-129">**encoder**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-130">Vedere: codec</span><span class="sxs-lookup"><span data-stu-id="7cb9c-130">See Other Term: codec</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="7cb9c-131">L</span><span class="sxs-lookup"><span data-stu-id="7cb9c-131">L</span></span>

<dl> <dt>

<span data-ttu-id="7cb9c-132">**Lossless**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-132">**lossless**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-133">Tipo di compressione che garantisce che i dati originali possano essere recuperati esattamente, senza perdita di qualità dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-133">A type of compression that ensures that the original data can be recovered exactly, with no loss in image quality.</span></span>

</dd> <dt>

<span data-ttu-id="7cb9c-134">**con perdita**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-134">**lossy**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-135">Processo per la compressione dei dati in cui le informazioni ritenute non necessarie vengono rimosse e non possono essere recuperate durante la decompressione.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-135">A process for compressing data in which information deemed unnecessary is removed and cannot be recovered upon decompression.</span></span> <span data-ttu-id="7cb9c-136">Usato in genere con dati audio e visivi in cui è accettabile una lieve riduzione della qualità.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-136">Typically used with audio and visual data in which a slight degradation of quality is acceptable.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="7cb9c-137">M</span><span class="sxs-lookup"><span data-stu-id="7cb9c-137">M</span></span>

<dl> <dt>

<span data-ttu-id="7cb9c-138">**Apartment a thread multipli (MTA)**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-138">**multithreaded apartment (MTA)**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-139">Forma di multithreading supportata da Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="7cb9c-139">A form of multithreading that is supported by Component Object Model (COM).</span></span> <span data-ttu-id="7cb9c-140">In un modello di Apartment a thread multipli tutti i thread del processo che sono stati inizializzati come a thread libero si trovano in un unico Apartment.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-140">In a multithreaded apartment model, all of the threads in the process that have been initialized as free-threaded reside in a single apartment.</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="7cb9c-141">N</span><span class="sxs-lookup"><span data-stu-id="7cb9c-141">N</span></span>

<dl> <dt>

<span data-ttu-id="7cb9c-142">**formato pixel nativo**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-142">**native pixel format**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-143">Uno dei formati pixel forniti da WIC, in cui viene descritto il layout della memoria di ogni pixel in una bitmap.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-143">One of the pixel formats provided by WIC, wherein the memory layout of each pixel in a bitmap is described.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="7cb9c-144">P</span><span class="sxs-lookup"><span data-stu-id="7cb9c-144">P</span></span>

<dl> <dt>

<span data-ttu-id="7cb9c-145">**tavolozza**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-145">**palette**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-146">Set di colori utilizzati da un oggetto o da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-146">Set of colors used by an object or application.</span></span>

</dd> <dt>

<span data-ttu-id="7cb9c-147">**criteri per i metadati delle foto**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-147">**photo metadata policy**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-148">Criteri di Windows per la lettura, la scrittura e la rimozione dei metadati delle immagini.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-148">The windows policy for reading, writing, and removing image metadata.</span></span>

</dd> <dt>

<span data-ttu-id="7cb9c-149">**formato a pixel**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-149">**pixel format**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-150">Dimensioni e disposizione dei componenti colore pixel in memoria.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-150">Size and arrangement of pixel color components in memory.</span></span> <span data-ttu-id="7cb9c-151">Viene specificato in base al numero totale di bit utilizzati per pixel e al numero di bit utilizzati per archiviare i componenti rosso, verde, blu e alfa del colore.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-151">It is specified by the total number of bits used per pixel and the number of bits used to store the red, green, blue, and alpha components of the color.</span></span> <span data-ttu-id="7cb9c-152">Ad esempio, il formato pixel RGB24 utilizza 24 bit per archiviare un colore pixel, con otto bit ciascuno per rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-152">For example, the RGB24 pixel format uses 24 bits to store a pixel color, with eight bits each for red, green, and blue.</span></span> <span data-ttu-id="7cb9c-153">Il formato pixel ARGB32 utilizza 32 bit, con 24 bit di informazioni sui colori e 8 bit di informazioni sul canale alfa.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-153">The ARGB32 pixel format uses 32 bits, with 24 bits of color information and 8 bits of alpha channel information.</span></span>

</dd> <dt>

<span data-ttu-id="7cb9c-154">**decodifica progressiva**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-154">**progressive decoding**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-155">Processo per la decodifica delle immagini codificate con informazioni sui diversi livelli di decodifica.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-155">The process for decoding images that have been encoded with information about the different decoding levels.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="7cb9c-156">S</span><span class="sxs-lookup"><span data-stu-id="7cb9c-156">S</span></span>

<dl> <dt>

<span data-ttu-id="7cb9c-157">**flusso**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-157">**stream**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-158">Si riferisce a un'interfaccia COM IStream che può essere usata per leggere o scrivere in sequenza i dati in file, memoria o percorsi di rete.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-158">Refers to an IStream COM interface which can be used to sequentially read or write data to files, memory, or network locations.</span></span>

</dd> </dl>

## <a name="t"></a><span data-ttu-id="7cb9c-159">T</span><span class="sxs-lookup"><span data-stu-id="7cb9c-159">T</span></span>

<dl> <dt>

<span data-ttu-id="7cb9c-160">**curva tono**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-160">**tone curve**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-161">Grafico utilizzato nella fotografia digitale che Visualizza l'intervallo tonale dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-161">A graph used in digital photography that displays the tonal range of the image.</span></span>

</dd> </dl>

## <a name="w"></a><span data-ttu-id="7cb9c-162">W</span><span class="sxs-lookup"><span data-stu-id="7cb9c-162">W</span></span>

<dl> <dt>

<span data-ttu-id="7cb9c-163">**Windows Imaging Component (WIC)**</span><span class="sxs-lookup"><span data-stu-id="7cb9c-163">**Windows Imaging Component (WIC)**</span></span>
</dt> <dd>

<span data-ttu-id="7cb9c-164">Piattaforma estendibile che fornisce un'API di basso livello per le immagini digitali.</span><span class="sxs-lookup"><span data-stu-id="7cb9c-164">An extensible platform that provides low-level API for digital images.</span></span>

</dd> </dl>

 

 



