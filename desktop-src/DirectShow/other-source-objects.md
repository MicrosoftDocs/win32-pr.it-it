---
description: Altri oggetti di origine
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: Altri oggetti di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c76c8f6cb104e87630f178a82d613675b96723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747050"
---
# <a name="other-source-objects"></a><span data-ttu-id="30d31-103">Altri oggetti di origine</span><span class="sxs-lookup"><span data-stu-id="30d31-103">Other Source Objects</span></span>

<span data-ttu-id="30d31-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="30d31-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="30d31-105">Oltre alle origini video e audio, i [servizi di modifica DirectShow](directshow-editing-services.md) (des) supportano gli oggetti di origine seguenti.</span><span class="sxs-lookup"><span data-stu-id="30d31-105">In addition to video and audio sources, [DirectShow Editing Services](directshow-editing-services.md) (DES) supports the following source objects.</span></span>

<span data-ttu-id="30d31-106">**Immagini ancora**</span><span class="sxs-lookup"><span data-stu-id="30d31-106">**Still Images**</span></span>

<span data-ttu-id="30d31-107">DES supporta i formati di file seguenti per le immagini ancora:</span><span class="sxs-lookup"><span data-stu-id="30d31-107">DES supports the following file formats for still images:</span></span>

-   <span data-ttu-id="30d31-108">Bitmap (.bmp)</span><span class="sxs-lookup"><span data-stu-id="30d31-108">Bitmap (.bmp)</span></span>
-   <span data-ttu-id="30d31-109">GIF (Graphics Interchange Format)</span><span class="sxs-lookup"><span data-stu-id="30d31-109">GIF (Graphics Interchange Format)</span></span>
-   <span data-ttu-id="30d31-110">JPEG (Joint Photographic Experts Group)</span><span class="sxs-lookup"><span data-stu-id="30d31-110">JPEG (Joint Photographic Experts Group)</span></span>
-   <span data-ttu-id="30d31-111">Targa o scheda grafica TrueVision (. tga): modalità 2 (RGB non compresso) in formato a 16 bit, 24, bit o 32 bit.</span><span class="sxs-lookup"><span data-stu-id="30d31-111">Targa or Truevision Graphics Adapter (.tga): Mode 2 (uncompressed RGB) in 16-bit, 24,-bit, or 32-bit format.</span></span>

<span data-ttu-id="30d31-112">Questi file possono essere usati come immagini ancora o per creare animazioni.</span><span class="sxs-lookup"><span data-stu-id="30d31-112">These files can be used as still images or to create animations.</span></span> <span data-ttu-id="30d31-113">Per i file bitmap, JPEG e targa, se si usa il file come immagine ancora, chiamare il metodo [**IAMTimelineSrc:: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) per impostare la frequenza dei fotogrammi su zero.</span><span class="sxs-lookup"><span data-stu-id="30d31-113">For bitmap, JPEG, and Targa files, if you are using the file as a still image, call the [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) method to set the frame rate to zero.</span></span>

<span data-ttu-id="30d31-114">**Sequenze DIB**</span><span class="sxs-lookup"><span data-stu-id="30d31-114">**DIB Sequences**</span></span>

<span data-ttu-id="30d31-115">Data una serie di file bitmap, JPEG o targa, il motore di rendering può costruire una sequenza DIB.</span><span class="sxs-lookup"><span data-stu-id="30d31-115">Given a series of bitmap, JPEG, or Targa files, the render engine can construct a DIB sequence.</span></span> <span data-ttu-id="30d31-116">Per creare una sequenza DIB, assegnare i nomi numerici sequenziali ai file, ad esempio Image001.bmp, Image002.bmp, Image003.bmp e così via.</span><span class="sxs-lookup"><span data-stu-id="30d31-116">To create a DIB sequence, give the files numerically sequential names, such as Image001.bmp, Image002.bmp, Image003.bmp, and so on.</span></span> <span data-ttu-id="30d31-117">Usare il primo file nella sequenza come origine.</span><span class="sxs-lookup"><span data-stu-id="30d31-117">Use the first file in the sequence as the source.</span></span> <span data-ttu-id="30d31-118">Impostare la frequenza dei fotogrammi per la sequenza chiamando [**IAMTimelineSrc:: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md).</span><span class="sxs-lookup"><span data-stu-id="30d31-118">Set the frame rate for the sequence by calling [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md).</span></span> <span data-ttu-id="30d31-119">Il motore di rendering scorre le immagini nella sequenza in base alla frequenza dei fotogrammi specificata.</span><span class="sxs-lookup"><span data-stu-id="30d31-119">The render engine cycles through the images in the sequence at the specified frame rate.</span></span>

<span data-ttu-id="30d31-120">Se la sequenza è troppo corta per riempire la durata, data la frequenza dei fotogrammi, il resto della durata è nero a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="30d31-120">If the sequence is too short to fill the duration, given the frame rate, the rest of the duration is solid black.</span></span> <span data-ttu-id="30d31-121">Non si verificano errori durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="30d31-121">No error occurs during rendering.</span></span>

<span data-ttu-id="30d31-122">**Origini GIF**</span><span class="sxs-lookup"><span data-stu-id="30d31-122">**GIF Sources**</span></span>

<span data-ttu-id="30d31-123">DES supporta le origini GIF, incluse le gif animate e trasparenti, usando la specifica GIF89a.</span><span class="sxs-lookup"><span data-stu-id="30d31-123">DES supports GIF sources, including animated and transparent GIFs, using the GIF89a specification.</span></span> <span data-ttu-id="30d31-124">Con un GIF animato, a differenza degli altri tipi di file, non è necessario impostare la frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="30d31-124">With an animated GIF, unlike the other file types, you do not need to set the frame rate.</span></span> <span data-ttu-id="30d31-125">Il file GIF specifica il ritardo tra le singole immagini nell'animazione.</span><span class="sxs-lookup"><span data-stu-id="30d31-125">The GIF file specifies the delay between each image in the animation.</span></span>

<span data-ttu-id="30d31-126">Per supportare le gif trasparenti, DES converte le aree trasparenti nell'immagine nel RGB RGB RGB (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="30d31-126">To support transparent GIFs, DES converts transparent regions in the image to the RGB triplet RGB(0,0,0).</span></span> <span data-ttu-id="30d31-127">È quindi possibile usare la [transizione della chiave](key-transition.md) per la chiave su RGB (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="30d31-127">You can then use the [Key Transition](key-transition.md) to key on RGB(0,0,0).</span></span>

<span data-ttu-id="30d31-128">DES converte anche le aree nere che rientrano nell'intervallo RGB (0-7, 0-7, 0-7) nel valore RGB (8, 8, 8), ad eccezione dell'indice di trasparenza, se rientra in tale intervallo.</span><span class="sxs-lookup"><span data-stu-id="30d31-128">DES also converts any black regions that fall within the range RGB(0–7,0–7,0–7) to the value RGB(8,8,8)—except for the transparency index, if it falls in that range.</span></span> <span data-ttu-id="30d31-129">Questa conversione non è rilevabile a occhio.</span><span class="sxs-lookup"><span data-stu-id="30d31-129">This conversion is not detectable to the eye.</span></span>

<span data-ttu-id="30d31-130">**Origine colore video**</span><span class="sxs-lookup"><span data-stu-id="30d31-130">**Video Color Source**</span></span>

<span data-ttu-id="30d31-131">L'oggetto di [origine colore video](video-color-source.md) crea un'immagine video continua di un colore a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="30d31-131">The [Video Color Source](video-color-source.md) object creates a continuous video image of a solid color.</span></span> <span data-ttu-id="30d31-132">Un utilizzo di questo oggetto consiste nel renderlo un livello in una transizione.</span><span class="sxs-lookup"><span data-stu-id="30d31-132">One use for this object is to make it a layer in a transition.</span></span> <span data-ttu-id="30d31-133">Ad esempio, usarla in una dissolvenza video o in una dissolvenza in uscita.</span><span class="sxs-lookup"><span data-stu-id="30d31-133">For example, use it in a video fade-in or fade-out.</span></span>

<span data-ttu-id="30d31-134">**Filtri di origine personalizzati**</span><span class="sxs-lookup"><span data-stu-id="30d31-134">**Custom Source Filters**</span></span>

<span data-ttu-id="30d31-135">I DES possono usare un filtro di origine DirectShow come origine della sequenza temporale, se il filtro soddisfa le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="30d31-135">DES can use a DirectShow source filter as a timeline source, if the filter meets the following conditions:</span></span>

-   <span data-ttu-id="30d31-136">Supporta la ricerca</span><span class="sxs-lookup"><span data-stu-id="30d31-136">It supports seeking</span></span>
-   <span data-ttu-id="30d31-137">Produce un formato supportato da DES.</span><span class="sxs-lookup"><span data-stu-id="30d31-137">It produces a format that DES supports.</span></span> <span data-ttu-id="30d31-138">Il formato può essere compresso purché il sistema dell'utente disponga di un filtro DirectShow in grado di decodificarlo.</span><span class="sxs-lookup"><span data-stu-id="30d31-138">The format can be compressed as long as the user's system has a DirectShow filter capable of decoding it.</span></span>

<span data-ttu-id="30d31-139">Per utilizzare un'origine personalizzata, specificare il CLSID del filtro come GUID dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="30d31-139">To use a custom source, specify the CLSID of the filter as the subobject GUID of the source object.</span></span> <span data-ttu-id="30d31-140">Per ulteriori informazioni, vedere [sottooggetti](subobjects.md).</span><span class="sxs-lookup"><span data-stu-id="30d31-140">For more information, see [Subobjects](subobjects.md).</span></span> <span data-ttu-id="30d31-141">Per supportare le proprietà personalizzate, implementarle come proprietà "put" di **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="30d31-141">To support custom properties, implement them as **IDispatch** "put" properties.</span></span> <span data-ttu-id="30d31-142">Negli oggetti di origine sono supportate solo le proprietà statiche. le proprietà dinamiche non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="30d31-142">Only static properties are supported on source objects; dynamic properties are not supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30d31-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="30d31-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30d31-144">Utilizzo di origini</span><span class="sxs-lookup"><span data-stu-id="30d31-144">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



