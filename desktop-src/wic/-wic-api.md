---
description: Windows Imaging Component (WIC) fornisce un'API basata su Component Object Model (COM) per l'utilizzo in C e C++.
ms.assetid: 74b14b5e-70e9-410f-a6e6-d8873a5f4fa4
title: Panoramica dell'API WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86e5a876010e52489adac9baa7ce57fdfdf80f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313437"
---
# <a name="wic-api-overview"></a><span data-ttu-id="5304f-103">Panoramica dell'API WIC</span><span class="sxs-lookup"><span data-stu-id="5304f-103">WIC API Overview</span></span>

<span data-ttu-id="5304f-104">Windows Imaging Component (WIC) fornisce un'API basata su Component Object Model (COM) per l'utilizzo in C e C++.</span><span class="sxs-lookup"><span data-stu-id="5304f-104">The Windows Imaging Component (WIC) provides a Component Object Model (COM) based API for use in C and C++.</span></span> <span data-ttu-id="5304f-105">L'API WIC espone un'ampia gamma di funzionalità correlate all'immagine, tra cui:</span><span class="sxs-lookup"><span data-stu-id="5304f-105">The WIC API exposes a variety of image-related functionality, including:</span></span>

-   <span data-ttu-id="5304f-106">Codec predefiniti per i formati di immagine Web standard.</span><span class="sxs-lookup"><span data-stu-id="5304f-106">Built-in codecs for the standard web image formats.</span></span>
-   <span data-ttu-id="5304f-107">Supporto incorporato per i formati di metadati standard.</span><span class="sxs-lookup"><span data-stu-id="5304f-107">Built-in support for standard metadata formats.</span></span>
-   <span data-ttu-id="5304f-108">Ampia gamma di supporto per il formato pixel.</span><span class="sxs-lookup"><span data-stu-id="5304f-108">Wide range of pixel format support.</span></span>
-   <span data-ttu-id="5304f-109">Supporto per colori elevati; inclusi i formati di intervallo esteso a 30 bit, a 32 bit e di precisione elevata e a 48 bit e i formati pixel a gamma ampia.</span><span class="sxs-lookup"><span data-stu-id="5304f-109">High-color support; including 30-bit extended range, 30-bit high precision, and 48-bit high precision and wide gamut pixel formats.</span></span>
-   <span data-ttu-id="5304f-110">Framework estensibile per codec di immagini, formati pixel e formati di metadati.</span><span class="sxs-lookup"><span data-stu-id="5304f-110">Extensible framework for image codecs, pixel formats, and metadata formats.</span></span>

<span data-ttu-id="5304f-111">Questo argomento contiene gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="5304f-111">This topic contains the following topics.</span></span>

-   [<span data-ttu-id="5304f-112">File di intestazione WIC</span><span class="sxs-lookup"><span data-stu-id="5304f-112">WIC Header Files</span></span>](#wic-header-files)
-   [<span data-ttu-id="5304f-113">File di libreria</span><span class="sxs-lookup"><span data-stu-id="5304f-113">Library Files</span></span>](#library-files)
-   [<span data-ttu-id="5304f-114">Class factory</span><span class="sxs-lookup"><span data-stu-id="5304f-114">Class Factories</span></span>](#class-factories)
-   [<span data-ttu-id="5304f-115">Componenti per la creazione di immagini</span><span class="sxs-lookup"><span data-stu-id="5304f-115">Imaging Components</span></span>](#imaging-components)
-   [<span data-ttu-id="5304f-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5304f-116">See Also</span></span>](#see-also)

## <a name="wic-header-files"></a><span data-ttu-id="5304f-117">File di intestazione WIC</span><span class="sxs-lookup"><span data-stu-id="5304f-117">WIC Header Files</span></span>

<span data-ttu-id="5304f-118">Le API WIC sono definite nei file di intestazione e IDL (Interface Definition Language) seguenti:</span><span class="sxs-lookup"><span data-stu-id="5304f-118">The WIC APIs are defined in the following header and Interface Definition Language (IDL) files:</span></span>



| <span data-ttu-id="5304f-119">File</span><span class="sxs-lookup"><span data-stu-id="5304f-119">File</span></span>              | <span data-ttu-id="5304f-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5304f-120">Description</span></span>                                          |
|-------------------|------------------------------------------------------|
| <span data-ttu-id="5304f-121">wincodec. h</span><span class="sxs-lookup"><span data-stu-id="5304f-121">wincodec.h</span></span>        | <span data-ttu-id="5304f-122">Definisce le versioni C e C++ delle API WIC primarie.</span><span class="sxs-lookup"><span data-stu-id="5304f-122">Defines C and C++ versions of the primary WIC APIs.</span></span>  |
| <span data-ttu-id="5304f-123">wincodec. idl</span><span class="sxs-lookup"><span data-stu-id="5304f-123">wincodec.idl</span></span>      | <span data-ttu-id="5304f-124">Definisce le interfacce WIC primarie.</span><span class="sxs-lookup"><span data-stu-id="5304f-124">Defines the primary WIC interfaces.</span></span>                  |
| <span data-ttu-id="5304f-125">wincodecsdk. h</span><span class="sxs-lookup"><span data-stu-id="5304f-125">wincodecsdk.h</span></span>     | <span data-ttu-id="5304f-126">Definisce le versioni C e C++ delle API WIC dei metadati.</span><span class="sxs-lookup"><span data-stu-id="5304f-126">Defines C and C++ versions of the metadata WIC APIs.</span></span> |
| <span data-ttu-id="5304f-127">wincodecsdk. idl</span><span class="sxs-lookup"><span data-stu-id="5304f-127">wincodecsdk.idl</span></span>   | <span data-ttu-id="5304f-128">Definisce le interfacce dei metadati WIC.</span><span class="sxs-lookup"><span data-stu-id="5304f-128">Defines the WIC metadata interfaces.</span></span>                 |
| <span data-ttu-id="5304f-129">\_proxy wincodec. h</span><span class="sxs-lookup"><span data-stu-id="5304f-129">wincodec\_proxy.h</span></span> | <span data-ttu-id="5304f-130">Definisce le esportazioni del proxy WIC.</span><span class="sxs-lookup"><span data-stu-id="5304f-130">Defines the WIC proxy exports.</span></span>                       |



 

<span data-ttu-id="5304f-131">Per usare WIC, le applicazioni devono includere wincodec. h e/o wincodecsdk. h, a seconda dell'API necessaria per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5304f-131">To use WIC, your applications must include wincodec.h and/or wincodecsdk.h, depending on the API your application needs.</span></span>

## <a name="library-files"></a><span data-ttu-id="5304f-132">File di libreria</span><span class="sxs-lookup"><span data-stu-id="5304f-132">Library Files</span></span>

<span data-ttu-id="5304f-133">File della libreria WIC:</span><span class="sxs-lookup"><span data-stu-id="5304f-133">The WIC library files:</span></span>



| <span data-ttu-id="5304f-134">File</span><span class="sxs-lookup"><span data-stu-id="5304f-134">File</span></span>              | <span data-ttu-id="5304f-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5304f-135">Description</span></span>                                                            |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="5304f-136">windowscodecs. lib</span><span class="sxs-lookup"><span data-stu-id="5304f-136">windowscodecs.lib</span></span> | <span data-ttu-id="5304f-137">Libreria di importazione fornita da Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="5304f-137">Import library provided by the Windows Software Development Kit (SDK).</span></span> |
| <span data-ttu-id="5304f-138">windowscodecs.dll</span><span class="sxs-lookup"><span data-stu-id="5304f-138">windowscodecs.dll</span></span> | <span data-ttu-id="5304f-139">Libreria di implementazione azionaria fornita dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5304f-139">Stock implementation library provided by the operating system.</span></span>         |



 

<span data-ttu-id="5304f-140">Per eseguire il collegamento alle API WIC, l'applicazione deve includere windowscodec. lib come dipendenza aggiuntiva del linker.</span><span class="sxs-lookup"><span data-stu-id="5304f-140">To link to WIC APIs, your application must include windowscodec.lib as an additional linker dependency.</span></span>

## <a name="class-factories"></a><span data-ttu-id="5304f-141">Class factory</span><span class="sxs-lookup"><span data-stu-id="5304f-141">Class Factories</span></span>

<span data-ttu-id="5304f-142">Nella tabella seguente vengono descritte le due class factory COM fornite dalle API WIC per la creazione di componenti WIC.</span><span class="sxs-lookup"><span data-stu-id="5304f-142">The following table describes the two COM class factories the WIC APIs provide for creating WIC components.</span></span>



| <span data-ttu-id="5304f-143">Interfaccia Factory</span><span class="sxs-lookup"><span data-stu-id="5304f-143">Factory Interface</span></span>                                               | <span data-ttu-id="5304f-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5304f-144">Description</span></span>                                                                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5304f-145">**IWICImagingFactory**</span><span class="sxs-lookup"><span data-stu-id="5304f-145">**IWICImagingFactory**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)     | <span data-ttu-id="5304f-146">Class factory primario per lo sviluppo di applicazioni mediante componenti WIC.</span><span class="sxs-lookup"><span data-stu-id="5304f-146">Primary class factory for application development using WIC components.</span></span> <span data-ttu-id="5304f-147">Questa factory crea componenti come decodificatori di immagini, codificatori e flussi.</span><span class="sxs-lookup"><span data-stu-id="5304f-147">This factory creates components such as image decoders, encoders and streams.</span></span>   |
| [<span data-ttu-id="5304f-148">**IWICComponentFactory**</span><span class="sxs-lookup"><span data-stu-id="5304f-148">**IWICComponentFactory**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) | <span data-ttu-id="5304f-149">Class factory di destinazione per gli sviluppatori di componenti WIC.</span><span class="sxs-lookup"><span data-stu-id="5304f-149">Class factory targeted for WIC component developers.</span></span> <span data-ttu-id="5304f-150">I componenti creati da questa factory vengono usati principalmente per lo sviluppo di codec e gestori di metadati.</span><span class="sxs-lookup"><span data-stu-id="5304f-150">Components created from this factory are primarily used in codec and metadata handler development.</span></span> |



 

<span data-ttu-id="5304f-151">Per creare una class factory, utilizzare la funzione com [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="5304f-151">To create either class factory, use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM function.</span></span> <span data-ttu-id="5304f-152">Nell'esempio seguente viene illustrata la creazione di WIC Imaging Factory.</span><span class="sxs-lookup"><span data-stu-id="5304f-152">The following example demonstrates the creation of the WIC imaging factory.</span></span>


```C++
// Initialize COM
CoInitialize(NULL);

// The factory pointer
IWICImagingFactory *pFactory = NULL;

// Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&pFactory)
);
```



## <a name="imaging-components"></a><span data-ttu-id="5304f-153">Componenti per la creazione di immagini</span><span class="sxs-lookup"><span data-stu-id="5304f-153">Imaging Components</span></span>

<span data-ttu-id="5304f-154">Le API WIC forniscono diversi tipi di componenti per la creazione di immagini.</span><span class="sxs-lookup"><span data-stu-id="5304f-154">The WIC APIs provide several types of imaging components.</span></span> <span data-ttu-id="5304f-155">Nella tabella seguente vengono descritti alcuni dei componenti di WIC comuni.</span><span class="sxs-lookup"><span data-stu-id="5304f-155">The following table describes some of the common WIC components.</span></span> <span data-ttu-id="5304f-156">Per un elenco completo dei componenti disponibili, vedere [interfacce WIC](-wic-codec-ifaces.md).</span><span class="sxs-lookup"><span data-stu-id="5304f-156">For a full list of available components, see [WIC interfaces](-wic-codec-ifaces.md).</span></span>



| <span data-ttu-id="5304f-157">Tipo di componente</span><span class="sxs-lookup"><span data-stu-id="5304f-157">Component Type</span></span>                                                      | <span data-ttu-id="5304f-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5304f-158">Description</span></span>                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5304f-159">**Bitmap**</span><span class="sxs-lookup"><span data-stu-id="5304f-159">**Bitmap**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                             | <span data-ttu-id="5304f-160">Rappresenta una rappresentazione in memoria scrivibile di un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource).</span><span class="sxs-lookup"><span data-stu-id="5304f-160">Represents a writable in-memory representation of an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource).</span></span> |
| [<span data-ttu-id="5304f-161">**Decodificatore**</span><span class="sxs-lookup"><span data-stu-id="5304f-161">**Decoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)                     | <span data-ttu-id="5304f-162">Usato per decodificare i dati immagine da un flusso in un formato utile per l'elaborazione di immagini.</span><span class="sxs-lookup"><span data-stu-id="5304f-162">Used to decode image data from a stream into a format that is useful for image processing.</span></span>                    |
| [<span data-ttu-id="5304f-163">**Encoder**</span><span class="sxs-lookup"><span data-stu-id="5304f-163">**Encoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)                     | <span data-ttu-id="5304f-164">Scrive i dati dell'immagine in un flusso.</span><span class="sxs-lookup"><span data-stu-id="5304f-164">Writes image data to a stream.</span></span>                                                                                |
| [<span data-ttu-id="5304f-165">**Stream**</span><span class="sxs-lookup"><span data-stu-id="5304f-165">**Stream**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)                             | <span data-ttu-id="5304f-166">Utilizzato per leggere e scrivere dati da un file, da una risorsa di rete, da un blocco di memoria e così via.</span><span class="sxs-lookup"><span data-stu-id="5304f-166">Used to read and write data from a file, network resource, a block of memory, and so on.</span></span>                      |
| [<span data-ttu-id="5304f-167">**Convertitore di formato**</span><span class="sxs-lookup"><span data-stu-id="5304f-167">**Format Converter**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)          | <span data-ttu-id="5304f-168">Utilizzato per eseguire la conversione da un formato pixel a un altro.</span><span class="sxs-lookup"><span data-stu-id="5304f-168">Used to convert from one pixel format to another.</span></span>                                                             |
| [<span data-ttu-id="5304f-169">**Lettore di query dei metadati**</span><span class="sxs-lookup"><span data-stu-id="5304f-169">**Metadata Query Reader**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) | <span data-ttu-id="5304f-170">Utilizzato per leggere i metadati di un'immagine o di un frame di immagine.</span><span class="sxs-lookup"><span data-stu-id="5304f-170">Used to read metadata of an image or image frame.</span></span>                                                             |
| [<span data-ttu-id="5304f-171">**Writer di query dei metadati**</span><span class="sxs-lookup"><span data-stu-id="5304f-171">**Metadata Query Writer**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) | <span data-ttu-id="5304f-172">Utilizzato per scrivere i metadati in un'immagine o in un frame di immagine.</span><span class="sxs-lookup"><span data-stu-id="5304f-172">Used to write metadata to an image or image frame.</span></span>                                                            |



 

## <a name="see-also"></a><span data-ttu-id="5304f-173">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5304f-173">See Also</span></span>

[<span data-ttu-id="5304f-174">Riferimenti</span><span class="sxs-lookup"><span data-stu-id="5304f-174">References</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="5304f-175">Esempi ed esempi di codice</span><span class="sxs-lookup"><span data-stu-id="5304f-175">Samples and Code Examples</span></span>](-wic-samples.md)


 

 
