---
description: Modello concettuale
ms.assetid: f906466e-acdc-4d0f-bf27-c5a25dc56c01
title: Modello concettuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a17538e7fdb454fa8eb61ab951a3316b0f0c327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233009"
---
# <a name="the-conceptual-model"></a><span data-ttu-id="c73b8-103">Modello concettuale</span><span class="sxs-lookup"><span data-stu-id="c73b8-103">The Conceptual Model</span></span>

<span data-ttu-id="c73b8-104">In questa sezione vengono descritti gli oggetti, le proprietà e le risorse che costituiscono il modello concettuale WPD.</span><span class="sxs-lookup"><span data-stu-id="c73b8-104">This section describes the objects, properties, and resources that constitute the WPD conceptual model.</span></span>

### <a name="objects"></a><span data-ttu-id="c73b8-105">Oggetti</span><span class="sxs-lookup"><span data-stu-id="c73b8-105">Objects</span></span>

<span data-ttu-id="c73b8-106">In WPD, le entità logiche nei dispositivi sono definite oggetti.</span><span class="sxs-lookup"><span data-stu-id="c73b8-106">In WPD, logical entities on devices are referred to as objects.</span></span> <span data-ttu-id="c73b8-107">In genere, ma non sempre, rappresentano i dati nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c73b8-107">Typically, but not always, these represent data on the device.</span></span> <span data-ttu-id="c73b8-108">Gli oggetti dispongono di proprietà a cui fanno riferimento gli identificatori di oggetto.</span><span class="sxs-lookup"><span data-stu-id="c73b8-108">Objects have properties, and are referenced by object identifiers.</span></span> <span data-ttu-id="c73b8-109">Esempi di oggetti includono immagini e cartelle in una fotocamera, canzoni e playlist su un lettore multimediale, contatti su un telefono cellulare e così via.</span><span class="sxs-lookup"><span data-stu-id="c73b8-109">Examples of objects include pictures and folders on a camera, songs and playlists on a media player, contacts on a mobile phone, and so on.</span></span>

<span data-ttu-id="c73b8-110">Gli oggetti possono anche rappresentare parti funzionali o informative del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c73b8-110">Objects can also represent functional or informational parts of the device.</span></span> <span data-ttu-id="c73b8-111">Esempi di questi includono i controlli dei giocatori (riproduzione/record/pausa), le impostazioni della fotocamera, le funzionalità SMS di un telefono cellulare e così via.</span><span class="sxs-lookup"><span data-stu-id="c73b8-111">Examples of these include player controls (play/record/pause), camera settings, a mobile phone's SMS capabilities, and so on.</span></span>

<span data-ttu-id="c73b8-112">I due argomenti seguenti forniscono esempi e illustrazioni di due tipi di oggetti: l'oggetto Image e l'oggetto Mediacast.</span><span class="sxs-lookup"><span data-stu-id="c73b8-112">The two following topics give examples and illustrations of two types of objects: the Image object and the Mediacast object.</span></span>

### <a name="image-object"></a><span data-ttu-id="c73b8-113">Image (oggetto)</span><span class="sxs-lookup"><span data-stu-id="c73b8-113">Image Object</span></span>

<span data-ttu-id="c73b8-114">Un oggetto Image rappresenta un'immagine ancora.</span><span class="sxs-lookup"><span data-stu-id="c73b8-114">An image object represents a still image.</span></span> <span data-ttu-id="c73b8-115">Il diagramma seguente mostra le relazioni tra un oggetto immagine, le relative proprietà e le relative risorse.</span><span class="sxs-lookup"><span data-stu-id="c73b8-115">The following diagram shows the relationships between an Image object, its properties, and its resources.</span></span>

![diagramma che mostra un oggetto WPD e la relativa relazione con le relative proprietà e risorse](images/wpd-overview-figure2.gif)

<span data-ttu-id="c73b8-117">Per ulteriori informazioni sull'oggetto Image e sulle relative proprietà, vedere l'argomento relativo all' [**\_ immagine del \_ tipo \_ di contenuto WPD**](wpd-content-type-image.md) .</span><span class="sxs-lookup"><span data-stu-id="c73b8-117">For more information about the Image object and its properties, see the [**WPD\_CONTENT\_TYPE\_IMAGE**](wpd-content-type-image.md) topic.</span></span>

### <a name="mediacast-object"></a><span data-ttu-id="c73b8-118">Oggetto Mediacast</span><span class="sxs-lookup"><span data-stu-id="c73b8-118">Mediacast Object</span></span>

<span data-ttu-id="c73b8-119">Un oggetto Mediacast può essere considerato come un oggetto contenitore che raggruppa il contenuto correlato, così come una playlist di gruppi di musica.</span><span class="sxs-lookup"><span data-stu-id="c73b8-119">A Mediacast object can be thought of as a container object that groups related content, just as a playlist groups music.</span></span> <span data-ttu-id="c73b8-120">Spesso, un oggetto Mediacast viene usato per raggruppare il contenuto multimediale pubblicato online.</span><span class="sxs-lookup"><span data-stu-id="c73b8-120">Often, a Mediacast object is used to group media content that was published online.</span></span> <span data-ttu-id="c73b8-121">Un canale RSS, ad esempio, può essere rappresentato come un oggetto Mediacast i cui riferimenti a oggetti puntano a oggetti contenuto che rappresentano ogni elemento nel canale.</span><span class="sxs-lookup"><span data-stu-id="c73b8-121">For example, an RSS channel can be represented as a Mediacast object whose object references point to content objects that represent each item in the channel.</span></span> <span data-ttu-id="c73b8-122">Il diagramma seguente illustra la relazione tra un oggetto Mediacast e i tre oggetti audio in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="c73b8-122">The following diagram shows the relationship between a Mediacast object and the three audio objects it contains.</span></span>

![diagramma che mostra la struttura gerarchica di un oggetto medica e di tre oggetti in esso contenuti](images/mediacast1.gif)

<span data-ttu-id="c73b8-124">I riferimenti all'oggetto audio sono specificati nella proprietà [riferimenti a \_ oggetti \_ WPD](object-properties.md) per l'oggetto Mediacast.</span><span class="sxs-lookup"><span data-stu-id="c73b8-124">The references to the audio object are specified in the [WPD\_OBJECT\_REFERENCES](object-properties.md) property for the Mediacast object.</span></span> <span data-ttu-id="c73b8-125">Per ulteriori informazioni sulle proprietà supportate da un oggetto Mediacast, vedere l'argomento relativo al [**\_ \_ \_ \_ cast del tipo di contenuto WPD**](wpd-content-type-media-cast.md) .</span><span class="sxs-lookup"><span data-stu-id="c73b8-125">For more information about the properties supported by a Mediacast object, see the [**WPD\_CONTENT\_TYPE\_MEDIA\_CAST**](wpd-content-type-media-cast.md) topic.</span></span>

### <a name="properties"></a><span data-ttu-id="c73b8-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c73b8-126">Properties</span></span>

<span data-ttu-id="c73b8-127">Le proprietà dell'oggetto forniscono un meccanismo per lo scambio di metadati che descrivono oggetti.</span><span class="sxs-lookup"><span data-stu-id="c73b8-127">Object properties provide a mechanism for exchanging object-describing metadata.</span></span> <span data-ttu-id="c73b8-128">Ad esempio, un oggetto Image può includere proprietà che descrivono il nome file, le dimensioni, il formato, la larghezza in pixel e così via.</span><span class="sxs-lookup"><span data-stu-id="c73b8-128">For example, an image object may include properties that describe its filename, size, format, width in pixels, and so on.</span></span>

<span data-ttu-id="c73b8-129">Le proprietà hanno un valore corrente, nonché gli attributi.</span><span class="sxs-lookup"><span data-stu-id="c73b8-129">Properties have a current value, as well as attributes.</span></span> <span data-ttu-id="c73b8-130">WPD definisce un set di proprietà standard che costituiscono le definizioni di API e DDI.</span><span class="sxs-lookup"><span data-stu-id="c73b8-130">WPD defines a set of standard properties that make up the API and DDI definitions.</span></span> <span data-ttu-id="c73b8-131">I fornitori non sono limitati alle proprietà WPD predefinite e possono aggiungerne di propri.</span><span class="sxs-lookup"><span data-stu-id="c73b8-131">Vendors are not limited to the predefined WPD properties and are free to add their own.</span></span>

### <a name="property-attributes"></a><span data-ttu-id="c73b8-132">Attributi di proprietà</span><span class="sxs-lookup"><span data-stu-id="c73b8-132">Property Attributes</span></span>

<span data-ttu-id="c73b8-133">Gli attributi delle proprietà descrivono i diritti di accesso, i valori validi e altre informazioni correlate a una proprietà.</span><span class="sxs-lookup"><span data-stu-id="c73b8-133">Property attributes describe the access rights, valid values, and other information related to a property.</span></span> <span data-ttu-id="c73b8-134">Ad esempio, la proprietà che rappresenta la velocità in bit può essere un intervallo compreso tra 8 kilobit al secondo (Kbps) e 20 kbps con un valore di passaggio di 1 Kbps.</span><span class="sxs-lookup"><span data-stu-id="c73b8-134">For example, the property representing bit rate could be a range from 8 kilobits per second (Kbps) to 20 Kbps with a step value of 1 Kbps.</span></span>

<span data-ttu-id="c73b8-135">I diritti di accesso indicano se i chiamanti possono leggere, scrivere e/o eliminare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="c73b8-135">Access rights indicate whether callers can read, write and/or delete the property.</span></span> <span data-ttu-id="c73b8-136">I valori validi indicano restrizioni per i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="c73b8-136">Valid values indicate restrictions for property values.</span></span> <span data-ttu-id="c73b8-137">I valori validi sono detti di un formato specifico.</span><span class="sxs-lookup"><span data-stu-id="c73b8-137">Valid values are said to be of a specific form.</span></span> <span data-ttu-id="c73b8-138">I formati di valore validi includono intervallo, ovvero la proprietà può assumere un valore da min a max con il passaggio specificato, enumerazione (ovvero, il valore della proprietà è uno di quelli nell'elenco specificato) e None (ovvero non sono presenti valori validi specifici).</span><span class="sxs-lookup"><span data-stu-id="c73b8-138">Valid value forms include Range (that is, property can take a value from Min to Max with specified Step), Enumeration (that is, property value is one of those in the specified List), and None (that is, there are no specific valid values).</span></span>

### <a name="resources"></a><span data-ttu-id="c73b8-139">Risorse</span><span class="sxs-lookup"><span data-stu-id="c73b8-139">Resources</span></span>

<span data-ttu-id="c73b8-140">Le risorse sono segnaposto per dati binari.</span><span class="sxs-lookup"><span data-stu-id="c73b8-140">Resources are placeholders for binary data.</span></span> <span data-ttu-id="c73b8-141">Un oggetto può avere più di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="c73b8-141">An object can have more than one resource.</span></span> <span data-ttu-id="c73b8-142">Se, ad esempio, l'oggetto rappresenta un file di immagine con un'annotazione audio, le risorse per questo oggetto potrebbero essere le seguenti:</span><span class="sxs-lookup"><span data-stu-id="c73b8-142">For example, if the object represented an image file with an audio annotation, then the resources for this object might be as follows:</span></span>

-   <span data-ttu-id="c73b8-143">Risorsa predefinita.</span><span class="sxs-lookup"><span data-stu-id="c73b8-143">A default resource.</span></span> <span data-ttu-id="c73b8-144">Questa risorsa rappresenta l'intero file di immagine.</span><span class="sxs-lookup"><span data-stu-id="c73b8-144">This resource represents the entire image file.</span></span> <span data-ttu-id="c73b8-145">Sono inclusi dati incorporati, ad esempio annotazioni audio, anteprime e così via.</span><span class="sxs-lookup"><span data-stu-id="c73b8-145">(This includes any embedded data such as audio annotations, thumbnails, and so on)</span></span>
-   <span data-ttu-id="c73b8-146">Una risorsa di anteprima.</span><span class="sxs-lookup"><span data-stu-id="c73b8-146">A thumbnail resource.</span></span> <span data-ttu-id="c73b8-147">Questa risorsa rappresenta i dati di anteprima per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="c73b8-147">This resource represents the thumbnail data for the image.</span></span>
-   <span data-ttu-id="c73b8-148">Una risorsa di annotazione audio.</span><span class="sxs-lookup"><span data-stu-id="c73b8-148">An audio annotation resource.</span></span> <span data-ttu-id="c73b8-149">Questa risorsa rappresenta i dati audio associati all'immagine.</span><span class="sxs-lookup"><span data-stu-id="c73b8-149">This resource represents the audio data associated with the image.</span></span>

### <a name="resource-attributes"></a><span data-ttu-id="c73b8-150">Attributi delle risorse</span><span class="sxs-lookup"><span data-stu-id="c73b8-150">Resource Attributes</span></span>

<span data-ttu-id="c73b8-151">Analogamente agli attributi delle proprietà, gli attributi delle risorse descrivono i diritti di accesso, le dimensioni, il formato e altre informazioni correlate a una risorsa.</span><span class="sxs-lookup"><span data-stu-id="c73b8-151">Similar to property attributes, resource attributes describe the access rights, size, format, and other information related to a resource.</span></span> <span data-ttu-id="c73b8-152">Ad esempio, gli attributi per una risorsa di annotazione audio in un oggetto Image possono specificare la velocità in bit, il numero di canali e il formato dati dell'audio.</span><span class="sxs-lookup"><span data-stu-id="c73b8-152">For example, the attributes for an audio annotation resource on an image object may specify the bit rate, channel count, and data format of the audio.</span></span>

### <a name="rendering-profiles-and-resource-attributes"></a><span data-ttu-id="c73b8-153">Profili di rendering e attributi delle risorse</span><span class="sxs-lookup"><span data-stu-id="c73b8-153">Rendering Profiles and Resource Attributes</span></span>

<span data-ttu-id="c73b8-154">Il profilo di rendering è un metodo usato dalle applicazioni per individuare gli attributi validi per una determinata risorsa.</span><span class="sxs-lookup"><span data-stu-id="c73b8-154">The rendering profile is one method that applications use to discover the valid attributes for a given resource.</span></span> <span data-ttu-id="c73b8-155">Ad esempio, un telefono cellulare può supportare bitmap con restrizioni specifiche sui valori di larghezza e altezza minimi e massimi.</span><span class="sxs-lookup"><span data-stu-id="c73b8-155">For example, a mobile phone may support bitmaps with specific restrictions on the minimum and maximum width and height values.</span></span> <span data-ttu-id="c73b8-156">Eseguendo una query sui profili di rendering per l'oggetto bitmap, un'applicazione può recuperare i valori esatti.</span><span class="sxs-lookup"><span data-stu-id="c73b8-156">By querying the rendering profiles for the bitmap object, an application can retrieve those exact values.</span></span>

<span data-ttu-id="c73b8-157">Nell'output di esempio seguente vengono identificate le informazioni sul profilo di rendering restituite dal dispositivo se sono supportate bitmap con un'altezza minima di 10 pixel, una larghezza minima di 20 pixel, un'altezza massima di 1000 pixel e una larghezza massima di 2000 pixel.</span><span class="sxs-lookup"><span data-stu-id="c73b8-157">The following sample output identifies the rendering profile information that the device would return if it supported bitmaps with a minimum height of 10 pixels, a minimum width of 20 pixels, a maximum height of 1000 pixels and a maximum width of 2000 pixels.</span></span>


```C++
WPD_OBJECT_FORMAT = WPD_OBJECT_FORMAT_BMP
WPD_MEDIA_HEIGHT:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  10
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  10 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_MEDIA_WIDTH:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX =  2000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE = 0
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  2000 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
```



<span data-ttu-id="c73b8-158">Vedere l'argomento [recupero delle funzionalità di rendering supportate da un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md) nella Guida alla programmazione per una descrizione del modo in cui l'applicazione può recuperare un profilo di rendering e gli attributi delle risorse associati.</span><span class="sxs-lookup"><span data-stu-id="c73b8-158">See the [Retrieving the Rendering Capabilities Supported by a Device](retrieving-the-rendering-capabilities-supported-by-a-device.md) topic in the programming guide for a description of how your application can retrieve a rendering profile (and the associated resource attributes).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c73b8-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c73b8-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c73b8-160">**Panoramica dell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="c73b8-160">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



