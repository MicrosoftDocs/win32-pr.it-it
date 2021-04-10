---
description: Questo argomento introduce il nuovo schema XMP (Extensible Metadata Platform) e la proprietà Photo System. Photo. PeopleNames di Windows 7 che consente l'assegnazione di tag a singoli utenti in una foto digitale.
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: Cenni preliminari sull'assegnazione di tag agli utenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f2080e51d4d340474e0610fcce9512fc72429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131894"
---
# <a name="people-tagging-overview"></a><span data-ttu-id="168a3-103">Cenni preliminari sull'assegnazione di tag agli utenti</span><span class="sxs-lookup"><span data-stu-id="168a3-103">People Tagging Overview</span></span>

<span data-ttu-id="168a3-104">Questo argomento introduce il nuovo schema XMP (Extensible Metadata Platform) e la proprietà Photo [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) di Windows 7 che consente l'assegnazione di tag a singoli utenti in una foto digitale.</span><span class="sxs-lookup"><span data-stu-id="168a3-104">This topic introduces the new Extensible Metadata Platform (XMP) schema and the Windows 7 photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) that enables the tagging of individuals in a digital photo.</span></span> <span data-ttu-id="168a3-105">In questo argomento viene inoltre illustrato come utilizzare l'API di Windows Imaging Component (WIC) per leggere e scrivere i metadati necessari per l'assegnazione di tag agli utenti.</span><span class="sxs-lookup"><span data-stu-id="168a3-105">This topic also discusses how to use the Windows Imaging Component (WIC) API to both read and write the metadata needed for people tagging.</span></span>

<span data-ttu-id="168a3-106">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="168a3-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="168a3-107">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="168a3-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="168a3-108">Introduzione</span><span class="sxs-lookup"><span data-stu-id="168a3-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="168a3-109">Assegnazione di tag agli utenti</span><span class="sxs-lookup"><span data-stu-id="168a3-109">People Tagging</span></span>](#people-tagging-overview)
    -   [<span data-ttu-id="168a3-110">Nomi di persone</span><span class="sxs-lookup"><span data-stu-id="168a3-110">People Names</span></span>](#people-names)
    -   [<span data-ttu-id="168a3-111">Rettangoli people</span><span class="sxs-lookup"><span data-stu-id="168a3-111">People Rectangles</span></span>](#people-rectangles)
-   [<span data-ttu-id="168a3-112">Riferimento allo schema</span><span class="sxs-lookup"><span data-stu-id="168a3-112">Schema Reference</span></span>](#schema-reference)
    -   [<span data-ttu-id="168a3-113">Schema di Microsoft Photo 1,2</span><span class="sxs-lookup"><span data-stu-id="168a3-113">Microsoft Photo 1.2 Schema</span></span>](#microsoft-photo-12-schema)
    -   [<span data-ttu-id="168a3-114">Schema Microsoft Photo RegionInfo</span><span class="sxs-lookup"><span data-stu-id="168a3-114">Microsoft Photo RegionInfo Schema</span></span>](#microsoft-photo-regioninfo-schema)
    -   [<span data-ttu-id="168a3-115">Schema area foto Microsoft</span><span class="sxs-lookup"><span data-stu-id="168a3-115">Microsoft Photo Region Schema</span></span>](#microsoft-photo-regioninfo-schema)
    -   [<span data-ttu-id="168a3-116">Metadati di esempio</span><span class="sxs-lookup"><span data-stu-id="168a3-116">Sample Metadata</span></span>](#sample-metadata)
-   [<span data-ttu-id="168a3-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="168a3-117">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="168a3-118">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="168a3-118">Prerequisites</span></span>

<span data-ttu-id="168a3-119">Per comprendere questo argomento, è necessario avere familiarità con le interfacce del decodificatore WIC e i componenti di Component Object Model correlati (COM), come descritto in [Panoramica dei componenti di Windows Imaging](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="168a3-119">To understand this topic, you should be familiar with the WIC decoder interfaces and its related Component Object Model (COM) components, as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> <span data-ttu-id="168a3-120">Consente inoltre di avere una conoscenza generale dei metadati di imaging, in particolare XMP.</span><span class="sxs-lookup"><span data-stu-id="168a3-120">It also helps to have a general familiarity with imaging metadata, especially XMP.</span></span>

## <a name="introduction"></a><span data-ttu-id="168a3-121">Introduzione</span><span class="sxs-lookup"><span data-stu-id="168a3-121">Introduction</span></span>

<span data-ttu-id="168a3-122">Microsoft ha creato un nuovo schema XMP per l'assegnazione di tag alle persone all'interno di un'immagine digitale.</span><span class="sxs-lookup"><span data-stu-id="168a3-122">Microsoft has created a new XMP schema for tagging people within a digital image.</span></span> <span data-ttu-id="168a3-123">Questo schema consente alle applicazioni di archiviare i nomi e i percorsi di singoli utenti presenti nell'immagine come metadati all'interno dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="168a3-123">This schema enables applications to store the names and locations of individuals who are in the image as metadata within the image.</span></span> <span data-ttu-id="168a3-124">Oltre al nuovo schema, la nuova proprietà Photo [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) è disponibile in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="168a3-124">In addition to the new schema, the new photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) is available in Windows 7.</span></span> <span data-ttu-id="168a3-125">Questa nuova proprietà consente alle applicazioni di leggere i nomi dei singoli archiviati nei metadati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="168a3-125">This new property enables applications to read the individual's names stored in the image metadata.</span></span> <span data-ttu-id="168a3-126">WIC utilizza queste nuove funzionalità consentendo alle applicazioni di leggere e scrivere facilmente i metadati per l'assegnazione di tag a foto digitali.</span><span class="sxs-lookup"><span data-stu-id="168a3-126">WIC utilizes these new features by enabling applications to easily read and write people tagging metadata to digital photos.</span></span>

## <a name="people-tagging"></a><span data-ttu-id="168a3-127">Assegnazione di tag agli utenti</span><span class="sxs-lookup"><span data-stu-id="168a3-127">People Tagging</span></span>

<span data-ttu-id="168a3-128">WIC fornisce agli sviluppatori di applicazioni i componenti COM che leggono i dati delle immagini e i metadati delle immagini.</span><span class="sxs-lookup"><span data-stu-id="168a3-128">WIC provides application developers with COM components which read image data as well as image metadata.</span></span> <span data-ttu-id="168a3-129">Per la lettura e la scrittura di metadati, ad esempio la nuova funzionalità di assegnazione di tag agli utenti, WIC fornisce le interfacce [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) e [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="168a3-129">For reading and writing metadata, such as the new people tagging feature, WIC provides the [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) and [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) interfaces.</span></span> <span data-ttu-id="168a3-130">Queste interfacce consentono alle applicazioni di usare il [linguaggio di query dei metadati](-wic-codec-metadataquerylanguage.md) per scrivere i metadati nei singoli frame di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="168a3-130">These interfaces enable applications to use the [metadata query language](-wic-codec-metadataquerylanguage.md) to write metadata to the individual frames of an image.</span></span> <span data-ttu-id="168a3-131">Nella sezione seguente viene illustrato come leggere e scrivere i metadati per l'assegnazione di tag alle persone nei metadati di un'immagine usando Reader e writer di query WIC.</span><span class="sxs-lookup"><span data-stu-id="168a3-131">The following section demonstrates how to read and write the people-tagging metadata into an image's metadata by using WIC query readers and writers.</span></span>

### <a name="people-names"></a><span data-ttu-id="168a3-132">Nomi di persone</span><span class="sxs-lookup"><span data-stu-id="168a3-132">People Names</span></span>

<span data-ttu-id="168a3-133">Parte della funzionalità di assegnazione di tag agli utenti è la possibilità di ottenere semplicemente un elenco dei nomi delle persone contrassegnate all'interno dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="168a3-133">Part of the people-tagging feature is the ability to simply get a list the names of the people tagged within the image.</span></span> <span data-ttu-id="168a3-134">Questa parte della funzionalità è supportata dai gestori di metadati [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) e WIC.</span><span class="sxs-lookup"><span data-stu-id="168a3-134">This part of the feature is supported by the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) and WIC's metadata handlers.</span></span> <span data-ttu-id="168a3-135">L'interfaccia [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) , in combinazione con la proprietà System. Photo. PeopleNames, viene usata per leggere i nomi delle persone identificate in un'immagine e archiviate nei metadati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="168a3-135">The [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) interface, in conjunction with the System.Photo.PeopleNames property, are used to read the names of people identified in an image and stored in the image metadata.</span></span>

<span data-ttu-id="168a3-136">Nell'esempio di codice seguente viene illustrato un lettore di query ottenuto da un frame immagine per eseguire una query sui metadati di un'immagine per i nomi con tag della proprietà [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) .</span><span class="sxs-lookup"><span data-stu-id="168a3-136">The following code example demonstrates a query reader obtained from an image frame to query an image's metadata for tagged names of the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) property.</span></span>


```C++
// Not shown: image decoding, retrieving an image frame. 
...
PROPVARIANT value;
IWICMetadataQueryReader *pQueryReader = NULL;
...
// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

// Query for the System.Photo.PeopleNames property.
if (SUCCEEDED(hr))
{
    // Get the property metadata by property name.
    hr = pQueryReader->GetMetadataByName(L"System.Photo.PeopleNames", &value);
}
```



<span data-ttu-id="168a3-137">L'espressione di query "System. Photo. PeopleNames" esegue una query sul frame per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="168a3-137">The query expression "System.Photo.PeopleNames" queries the frame for the property.</span></span> <span data-ttu-id="168a3-138">Se i metadati per l'assegnazione di tag sono presenti e contengono i nomi delle persone, il valore [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) verrà impostato su VT \_ LPWSTR e il valore dei dati conterrà l'elenco dei nomi con tag.</span><span class="sxs-lookup"><span data-stu-id="168a3-138">If the people-tagging metadata exists and contains people's names, the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value will be set to VT\_LPWSTR and the data value will contain the list of tagged names.</span></span> <span data-ttu-id="168a3-139">Per altre informazioni sulla lettura dei metadati delle immagini, vedere [Cenni preliminari sulla lettura e scrittura dei metadati delle immagini](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="168a3-139">For more information on reading image metadata, see [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

<span data-ttu-id="168a3-140">L'esecuzione di query per il tag People names è utile solo se l'immagine contiene effettivamente i metadati di Tag people.</span><span class="sxs-lookup"><span data-stu-id="168a3-140">Querying for the people names tag is only useful if the image actually contains the people-tagging metadata.</span></span> <span data-ttu-id="168a3-141">Per eseguire questa operazione, un'applicazione deve prima di tutto scriverla.</span><span class="sxs-lookup"><span data-stu-id="168a3-141">For this to occur, an application must first have written it.</span></span> <span data-ttu-id="168a3-142">Per scrivere i metadati dei nomi di persone, usare un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) e il percorso XMP esplicito dei metadati.</span><span class="sxs-lookup"><span data-stu-id="168a3-142">To write the people names metadata, use an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) and the explicit XMP path of the metadata.</span></span> <span data-ttu-id="168a3-143">Nell'esempio di codice riportato di seguito viene illustrato l'utilizzo di un writer di query per scrivere un nome nel percorso della query.</span><span class="sxs-lookup"><span data-stu-id="168a3-143">The following code example demonstrates using a query writer to write a name to the query path.</span></span>


```C++
// Not shown: image encoding, retrieving/creating the image frame,
// creating the IWICImagingFactory 
...
IWICImagingFactory *pFactory = NULL;
IWICMetadataQueryWriter *pQueryWriter = NULL;
...
// Get the query writer from the image frame.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pQueryWriter);
}

// A query writer specifically for this person's XMP struct
IWICMetadataQueryWriter *pXMPStructQueryWriter = NULL;

// Create a query writer specifically for an XMP Struct
hr = pFactory->CreateQueryWriter(
    GUID_MetadataFormatXMPStruct,
    NULL,
    &pXMPStructQueryWriter
    );

// Create a variant representing the structure created above
PROPVARIANT xmpStruct;
PropVariantInit(&xmpStruct);

// VT_UNKNOWN indicates that we're setting a COM object, in this case a XMPStruct
// which will hold the name and rectangle
xmpStruct.vt = VT_UNKNOWN; 
xmpStruct.punkVal = pXMPStructQueryWriter;

if(SUCCEEDED(hr))
{
    // WIC will automatically create the xmp base, the RegionInfo struct, and the Regions
    // bag (an unordered array) but structs within that bag need to be explicitly created.
    // The {ulong=0} in the query means to insert the new struct at the start of the bag,
    // {} could also be used to insert at the end of the bag.
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions/{ulong=0}",
        &xmpStruct
        );
}

// Set up the PROPVARIANT with the name information
PROPVARIANT personName;
PropVariantInit(&personName);
personName.vt = VT_LPWSTR;
personName.pwszVal = L"John Doe";

if(SUCCEEDED(hr))
{
    // Set the name metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:PersonDisplayName",
        &personName
        );  
}
```



<span data-ttu-id="168a3-144">Si noti il passaggio che costruisce la struttura XMP e la relativa impostazione `MPRI:Regions/{ulong=0}` .</span><span class="sxs-lookup"><span data-stu-id="168a3-144">Note the step constructing the XMP structure and setting it under `MPRI:Regions/{ulong=0}`.</span></span> <span data-ttu-id="168a3-145">Senza questo passaggio, WIC non è in grado di identificare la posizione in cui posizionare il `PersonDisplayName` in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="168a3-145">Without this step, the WIC can't identify where to place the `PersonDisplayName` later on.</span></span> <span data-ttu-id="168a3-146">Si noti inoltre che viene utilizzato il percorso di query esplicito anziché [System. Photo. PeopleNames](-wic-photoprop-system-photo-peoplenames.md), i cui criteri dei metadati non supportano la scrittura di metadati.</span><span class="sxs-lookup"><span data-stu-id="168a3-146">Also note that the explicit query path is used instead of [System.Photo.PeopleNames](-wic-photoprop-system-photo-peoplenames.md), whose metadata policy does not support writing metadata.</span></span>

### <a name="people-rectangles"></a><span data-ttu-id="168a3-147">Rettangoli people</span><span class="sxs-lookup"><span data-stu-id="168a3-147">People Rectangles</span></span>

<span data-ttu-id="168a3-148">I nomi delle persone, tuttavia, fanno parte della funzionalità di assegnazione di tag degli utenti.</span><span class="sxs-lookup"><span data-stu-id="168a3-148">People's names however, are only part of the people-tagging feature.</span></span> <span data-ttu-id="168a3-149">Oltre a archiviare i nomi delle persone nei metadati, lo schema supporta anche le informazioni sull'area che identificano l'area specifica (un rettangolo) che la persona viene visualizzata nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="168a3-149">In addition to storing people's names in the metadata, the schema also supports region information that identifies the specific area (a rectangle) the person is shown in the image.</span></span>

<span data-ttu-id="168a3-150">Le informazioni sul rettangolo sono rappresentate da quattro valori decimali delimitati da virgole, ad esempio "0,25, 0,25, 0,25, 0,25".</span><span class="sxs-lookup"><span data-stu-id="168a3-150">The rectangle information is represented by four comma-delimited decimal values, such as "0.25, 0.25, 0.25, 0.25".</span></span> <span data-ttu-id="168a3-151">I primi due valori specificano la coordinata superiore sinistra; gli ultimi due specificano l'altezza e la larghezza del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="168a3-151">The first two values specify the top-left coordinate; the final two specify the height and width of the rectangle.</span></span> <span data-ttu-id="168a3-152">Le dimensioni dell'immagine ai fini della definizione dei rettangoli people vengono normalizzate su 1, il che significa che nell'esempio "0,25, 0,25, 0,25, 0,25", il rettangolo inizia con 1/4 della distanza dalla parte superiore e 1/4 della distanza dalla sinistra dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="168a3-152">The dimensions of the image for the purposes of defining people rectangles are normalized to 1, which means that in the "0.25, 0.25, 0.25, 0.25" example, the rectangle starts 1/4 of the distance from the top and 1/4 of the distance from the left of the image.</span></span> <span data-ttu-id="168a3-153">Sia l'altezza che la larghezza del rettangolo sono pari a 1/4 della dimensione delle rispettive dimensioni di immagine.</span><span class="sxs-lookup"><span data-stu-id="168a3-153">Both the height and width of the rectangle are 1/4 of the size of their respective image dimensions.</span></span>

<span data-ttu-id="168a3-154">Le informazioni sul rettangolo che identificano i singoli vengono scritte nello stesso modo in cui vengono scritti i nomi delle persone, all'interno della stessa struttura.</span><span class="sxs-lookup"><span data-stu-id="168a3-154">The rectangle information that identifies individuals is written in the same way people's names are written, within the same structure.</span></span> <span data-ttu-id="168a3-155">Per scrivere i metadati del rettangolo, usare un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) e il percorso XMP esplicito dei metadati.</span><span class="sxs-lookup"><span data-stu-id="168a3-155">To write the rectangle metadata, use an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) and the explicit XMP path of the metadata.</span></span> <span data-ttu-id="168a3-156">Nell'esempio di codice seguente viene continuato l'esempio precedente e viene aggiunto un rettangolo che rappresenta ' John Doe ' ai metadati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="168a3-156">The following code example continues the previous example and adds a rectangle representing 'John Doe' to the image's metadata.</span></span> <span data-ttu-id="168a3-157">Si noti che usa lo stesso `{ulong=0}` indice per associare il rettangolo a "John Doe".</span><span class="sxs-lookup"><span data-stu-id="168a3-157">Note that it uses the same `{ulong=0}` index to associate this rectangle with 'John Doe'.</span></span>


```C++
// Set up the PROPVARIANT with the rectangle information
PROPVARIANT rectangle;
PropVariantInit(&rectangle);
rectangle.vt = VT_LPWSTR;
rectangle.pwszVal = L"0.0,0.0,0.25,0.25";

if(SUCCEEDED(hr))
{
    // Set the rectangle metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:Rectangle",
        &rectangle
        );
}
```



## <a name="schema-reference"></a><span data-ttu-id="168a3-158">Riferimenti agli schemi</span><span class="sxs-lookup"><span data-stu-id="168a3-158">Schema Reference</span></span>

<span data-ttu-id="168a3-159">Gli schemi Microsoft XMP per la codifica di persone definiscono un set di proprietà per contrassegnare i singoli utenti nelle foto digitali.</span><span class="sxs-lookup"><span data-stu-id="168a3-159">The Microsoft XMP schemas for people tagging define a set of properties to tag individuals in digital photos.</span></span>

<span data-ttu-id="168a3-160">Le sezioni seguenti forniscono le definizioni dello schema necessarie per l'assegnazione di tag agli utenti.</span><span class="sxs-lookup"><span data-stu-id="168a3-160">The following sections provide the schema definitions needed for people tagging.</span></span> <span data-ttu-id="168a3-161">Laddove possibile, le definizioni dello schema utilizzano le convenzioni fornite dalle [specifiche di Adobe Extensible Metadata Platform (XMP)](https://www.adobe.com/devnet/xmp/).</span><span class="sxs-lookup"><span data-stu-id="168a3-161">Wherever possible, the schema definitions use the conventions provided by [Adobe's Extensible Metadata Platform (XMP) Specifications](https://www.adobe.com/devnet/xmp/).</span></span> <span data-ttu-id="168a3-162">Le definizioni dello schema in questo argomento illustrano lo spazio dei nomi XML Uniform Resource Identifier (URI) che identifica lo schema e il prefisso dello spazio dei nomi dello schema preferito, seguito da una tabella in cui sono elencate tutte le proprietà definite per lo schema.</span><span class="sxs-lookup"><span data-stu-id="168a3-162">The schema definitions in this topic show the XML namespace Uniform Resource Identifier (URI) that identifies the schema and the preferred schema namespace prefix, followed by a table that lists all properties defined for the schema.</span></span> <span data-ttu-id="168a3-163">Ogni tabella contiene le colonne seguenti:</span><span class="sxs-lookup"><span data-stu-id="168a3-163">Each table has the following columns:</span></span>

-   <span data-ttu-id="168a3-164">**Proprietà** : nome della proprietà, incluso il prefisso dello spazio dei nomi preferito.</span><span class="sxs-lookup"><span data-stu-id="168a3-164">**Property** - The name of the property, including the preferred namespace prefix.</span></span>

-   <span data-ttu-id="168a3-165">**Tipo valore** : tipo di valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="168a3-165">**Value type** - The value type of the property.</span></span> <span data-ttu-id="168a3-166">Gli schemi di supporto per l'assegnazione di tag degli utenti usano i tipi di valore XMP, quando possibile, inclusi data e testo.</span><span class="sxs-lookup"><span data-stu-id="168a3-166">The people-tagging support schemas use the XMP value types whenever possible, including Date and Text.</span></span> <span data-ttu-id="168a3-167">I tipi di matrice sono preceduti dal tipo di contenitore: `alt` , `bag` o `seq` .</span><span class="sxs-lookup"><span data-stu-id="168a3-167">Array types are preceded by the container type: `alt`, `bag`, or `seq`.</span></span>

-   <span data-ttu-id="168a3-168">**Category** : le proprietà dello schema sono interne o esterne:</span><span class="sxs-lookup"><span data-stu-id="168a3-168">**Category** - Schema properties are internal or external:</span></span>

    -   <span data-ttu-id="168a3-169">I metadati interni devono essere impostati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="168a3-169">Internal metadata must be set by the application.</span></span>

    -   <span data-ttu-id="168a3-170">I metadati esterni devono essere impostati dall'utente e sono indipendenti dal contenuto del documento.</span><span class="sxs-lookup"><span data-stu-id="168a3-170">External metadata must be set by the user and is independent of the contents of the document.</span></span>

-   <span data-ttu-id="168a3-171">**Descrizione** : Descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="168a3-171">**Description** - The description of the property.</span></span>

### <a name="microsoft-photo-12-schema"></a><span data-ttu-id="168a3-172">Schema di Microsoft Photo 1,2</span><span class="sxs-lookup"><span data-stu-id="168a3-172">Microsoft Photo 1.2 Schema</span></span>

<span data-ttu-id="168a3-173">Lo schema Microsoft Photo 1,2 fornisce un set di proprietà per le aree dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="168a3-173">The Microsoft Photo 1.2 schema provides a set of properties for image regions.</span></span>

-   <span data-ttu-id="168a3-174">L'URI dello spazio dei nomi dello schema è `https://ns.microsoft.com/photo/1.2/` .</span><span class="sxs-lookup"><span data-stu-id="168a3-174">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/`.</span></span>
-   <span data-ttu-id="168a3-175">Il prefisso dello spazio dei nomi dello schema preferito è `MP` .</span><span class="sxs-lookup"><span data-stu-id="168a3-175">The preferred schema namespace prefix is `MP`.</span></span>



| <span data-ttu-id="168a3-176">Proprietà</span><span class="sxs-lookup"><span data-stu-id="168a3-176">Property</span></span>      | <span data-ttu-id="168a3-177">Tipo di valore</span><span class="sxs-lookup"><span data-stu-id="168a3-177">Value type</span></span> | <span data-ttu-id="168a3-178">Category</span><span class="sxs-lookup"><span data-stu-id="168a3-178">Category</span></span> | <span data-ttu-id="168a3-179">Descrizione</span><span class="sxs-lookup"><span data-stu-id="168a3-179">Description</span></span>                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="168a3-180">MP: RegionInfo</span><span class="sxs-lookup"><span data-stu-id="168a3-180">MP:RegionInfo</span></span> | <span data-ttu-id="168a3-181">RegionInfo</span><span class="sxs-lookup"><span data-stu-id="168a3-181">RegionInfo</span></span> | <span data-ttu-id="168a3-182">Interno</span><span class="sxs-lookup"><span data-stu-id="168a3-182">Internal</span></span> | <span data-ttu-id="168a3-183">**obbligatorio** : archivia la radice dei metadati per l'assegnazione di tag agli utenti.</span><span class="sxs-lookup"><span data-stu-id="168a3-183">**required** : Stores the root of the people-tagging metadata.</span></span> <span data-ttu-id="168a3-184">Vedere la sezione schema di Microsoft Photo RegionInfo che segue.</span><span class="sxs-lookup"><span data-stu-id="168a3-184">See the Microsoft Photo RegionInfo Schema section which follows.</span></span> |



 

### <a name="microsoft-photo-regioninfo-schema"></a><span data-ttu-id="168a3-185">Schema Microsoft Photo RegionInfo</span><span class="sxs-lookup"><span data-stu-id="168a3-185">Microsoft Photo RegionInfo Schema</span></span>

<span data-ttu-id="168a3-186">Lo schema Microsoft Photo RegionInfo 1,2 fornisce un set di proprietà per informazioni sull'area.</span><span class="sxs-lookup"><span data-stu-id="168a3-186">The Microsoft Photo RegionInfo 1.2 schema provides a set of properties for region info.</span></span>

-   <span data-ttu-id="168a3-187">L'URI dello spazio dei nomi dello schema è `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .</span><span class="sxs-lookup"><span data-stu-id="168a3-187">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/t/RegionInfo#`.</span></span>
-   <span data-ttu-id="168a3-188">Il prefisso dello spazio dei nomi dello schema preferito è `MPRI` .</span><span class="sxs-lookup"><span data-stu-id="168a3-188">The preferred schema namespace prefix is `MPRI`.</span></span>



| <span data-ttu-id="168a3-189">Proprietà</span><span class="sxs-lookup"><span data-stu-id="168a3-189">Property</span></span>              | <span data-ttu-id="168a3-190">Tipo di valore</span><span class="sxs-lookup"><span data-stu-id="168a3-190">Value type</span></span> | <span data-ttu-id="168a3-191">Category</span><span class="sxs-lookup"><span data-stu-id="168a3-191">Category</span></span> | <span data-ttu-id="168a3-192">Descrizione</span><span class="sxs-lookup"><span data-stu-id="168a3-192">Description</span></span>                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="168a3-193">MPRI:DateRegionsValid</span><span class="sxs-lookup"><span data-stu-id="168a3-193">MPRI:DateRegionsValid</span></span> | <span data-ttu-id="168a3-194">Data</span><span class="sxs-lookup"><span data-stu-id="168a3-194">Date</span></span>       | <span data-ttu-id="168a3-195">Esterno</span><span class="sxs-lookup"><span data-stu-id="168a3-195">External</span></span> | <span data-ttu-id="168a3-196">**facoltativo** : data di creazione dell'ultima area.</span><span class="sxs-lookup"><span data-stu-id="168a3-196">**optional** : Date that the last region was created.</span></span>                                                          |
| <span data-ttu-id="168a3-197">MPRI: aree</span><span class="sxs-lookup"><span data-stu-id="168a3-197">MPRI:Regions</span></span>          | <span data-ttu-id="168a3-198">Area del contenitore</span><span class="sxs-lookup"><span data-stu-id="168a3-198">bag Region</span></span> | <span data-ttu-id="168a3-199">Esterno</span><span class="sxs-lookup"><span data-stu-id="168a3-199">External</span></span> | <span data-ttu-id="168a3-200">**obbligatorio** : archivia le aree di tag degli utenti.</span><span class="sxs-lookup"><span data-stu-id="168a3-200">**required** : Stores the people tagging regions.</span></span> <span data-ttu-id="168a3-201">Vedere la sezione relativa allo schema dell'area di foto Microsoft riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="168a3-201">See the Microsoft Photo Region Schema section which follows.</span></span> |



 

### <a name="microsoft-photo-region-schema"></a><span data-ttu-id="168a3-202">Schema area foto Microsoft</span><span class="sxs-lookup"><span data-stu-id="168a3-202">Microsoft Photo Region Schema</span></span>

<span data-ttu-id="168a3-203">Lo schema Microsoft Photo Region 1,2 fornisce un set di proprietà per le aree dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="168a3-203">The Microsoft Photo Region 1.2 schema provides a set of properties for image regions.</span></span>

-   <span data-ttu-id="168a3-204">L'URI dello spazio dei nomi dello schema è `https://ns.microsoft.com/photo/1.2/t/Region#` .</span><span class="sxs-lookup"><span data-stu-id="168a3-204">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/t/Region#`.</span></span>
-   <span data-ttu-id="168a3-205">Il prefisso dello spazio dei nomi dello schema preferito è `MPReg` .</span><span class="sxs-lookup"><span data-stu-id="168a3-205">The preferred schema namespace prefix is `MPReg`.</span></span>



| <span data-ttu-id="168a3-206">MPReg: Proprietà</span><span class="sxs-lookup"><span data-stu-id="168a3-206">MPReg:Property</span></span>          | <span data-ttu-id="168a3-207">Tipo di valore</span><span class="sxs-lookup"><span data-stu-id="168a3-207">Value type</span></span> | <span data-ttu-id="168a3-208">Category</span><span class="sxs-lookup"><span data-stu-id="168a3-208">Category</span></span> | <span data-ttu-id="168a3-209">Descrizione</span><span class="sxs-lookup"><span data-stu-id="168a3-209">Description</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="168a3-210">MPReg:PersonDisplayName</span><span class="sxs-lookup"><span data-stu-id="168a3-210">MPReg:PersonDisplayName</span></span> | <span data-ttu-id="168a3-211">Testo</span><span class="sxs-lookup"><span data-stu-id="168a3-211">Text</span></span>       | <span data-ttu-id="168a3-212">Esterno</span><span class="sxs-lookup"><span data-stu-id="168a3-212">External</span></span> | <span data-ttu-id="168a3-213">**obbligatorio** : archivia il nome della persona nel rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="168a3-213">**required** : Stores the name of the person in the given rectangle.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="168a3-214">MPReg: rettangolo</span><span class="sxs-lookup"><span data-stu-id="168a3-214">MPReg:Rectangle</span></span>         | <span data-ttu-id="168a3-215">Testo</span><span class="sxs-lookup"><span data-stu-id="168a3-215">Text</span></span>       | <span data-ttu-id="168a3-216">Esterno</span><span class="sxs-lookup"><span data-stu-id="168a3-216">External</span></span> | <span data-ttu-id="168a3-217">**facoltativo** : archivia il rettangolo che identifica la persona all'interno della foto.</span><span class="sxs-lookup"><span data-stu-id="168a3-217">**optional** : Stores the rectangle that identifies the person within the photo.</span></span> <span data-ttu-id="168a3-218">Il rettangolo viene archiviato come quattro valori decimali delimitati da virgole.</span><span class="sxs-lookup"><span data-stu-id="168a3-218">The rectangle is stored as four comma-delimited decimal values.</span></span> <span data-ttu-id="168a3-219">I primi due valori specificano la coordinata superiore sinistra; gli ultimi due specificano l'altezza e la larghezza del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="168a3-219">The first two values specify the top left coordinate; the final two specify the height and width of the rectangle.</span></span> <span data-ttu-id="168a3-220">I valori decimali devono essere normalizzati in 1.</span><span class="sxs-lookup"><span data-stu-id="168a3-220">The decimal values must be normalized to 1.</span></span> |
| <span data-ttu-id="168a3-221">MPReg:PersonEmailDigest</span><span class="sxs-lookup"><span data-stu-id="168a3-221">MPReg:PersonEmailDigest</span></span> | <span data-ttu-id="168a3-222">Testo</span><span class="sxs-lookup"><span data-stu-id="168a3-222">Text</span></span>       | <span data-ttu-id="168a3-223">Esterno</span><span class="sxs-lookup"><span data-stu-id="168a3-223">External</span></span> | <span data-ttu-id="168a3-224">**facoltativo** : archivia l'hash del messaggio crittografato SHA-1 dell'indirizzo di posta elettronica attivo della persona.</span><span class="sxs-lookup"><span data-stu-id="168a3-224">**optional** : Stores the SHA-1 encrypted message hash of the person's Live e-mail address.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="168a3-225">MPReg:PersonLiveIdCID</span><span class="sxs-lookup"><span data-stu-id="168a3-225">MPReg:PersonLiveIdCID</span></span>   | <span data-ttu-id="168a3-226">Testo</span><span class="sxs-lookup"><span data-stu-id="168a3-226">Text</span></span>       | <span data-ttu-id="168a3-227">Esterno</span><span class="sxs-lookup"><span data-stu-id="168a3-227">External</span></span> | <span data-ttu-id="168a3-228">**facoltativo** : archivia la rappresentazione decimale con segno del CID attivo della persona, un intero a 64 bit che identifica pubblicamente un'identità Live.</span><span class="sxs-lookup"><span data-stu-id="168a3-228">**optional** :Stores the signed decimal representation of the person's Live CID, a 64-bit integer that publicly identifies a Live identity.</span></span>                                                                                                                                                                     |



 

### <a name="sample-metadata"></a><span data-ttu-id="168a3-229">Metadati di esempio</span><span class="sxs-lookup"><span data-stu-id="168a3-229">Sample Metadata</span></span>

<span data-ttu-id="168a3-230">Di seguito è riportata una rappresentazione dei metadati XMP per l'assegnazione di tag alle persone.</span><span class="sxs-lookup"><span data-stu-id="168a3-230">The following is a representation of the XMP metadata for people tagging.</span></span>

``` syntax
<rdf:Description rdf:about="" xmlns:MP="https://ns.microsoft.com/photo/1.2/">
<MP:RegionInfo> 
<rdf:Description xmlns:MPRI="https://ns.microsoft.com/photo/1.2/t/RegionInfo#">
   <MPRI:Regions> 
       <rdf:Bag> 
          <rdf:li> 
       <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#"> 
           <MPReg:Rectangle>0.790650, 0.441734, 0.209350, 0.279133
           </MPReg:Rectangle>
           <MPReg:PersonDisplayName>John Doe</MPReg:PersonDisplayName> 
           <MPReg:PersonEmailDigest>2FD4E1C67A2D28FCED849EE1BB76E7391B93EB13</MPReg:PersonEmailDigest> 
           <MPReg:PersonLiveIdCID>1234567890123456789</MPReg:PersonLiveIdCID> 
       </rdf:Description> 
         </rdf:li> 
         <rdf:li>
             <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#">
                  <MPReg:Rectangle>0.222656, 0.302083, 0.378906, 0.505208</MPReg:Rectangle> 
                  <MPReg:PersonDisplayName>Jane Doe</MPReg:PersonDisplayName> 
              </rdf:Description> 
         </rdf:li> 
<!-- Addition Regions --> ... 
<rdf:li>...
</rdf:li> 
</rdf:Bag> 
</MPRI:Regions> </rdf:Description> </MP:RegionInfo> </rdf:Description>
```

## <a name="related-topics"></a><span data-ttu-id="168a3-231">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="168a3-231">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="168a3-232">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="168a3-232">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="168a3-233">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="168a3-233">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="168a3-234">Cenni preliminari sui metadati WIC</span><span class="sxs-lookup"><span data-stu-id="168a3-234">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="168a3-235">Panoramica della lettura e della scrittura dei metadati delle immagini</span><span class="sxs-lookup"><span data-stu-id="168a3-235">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="168a3-236">Cenni preliminari sul linguaggio di query dei metadati</span><span class="sxs-lookup"><span data-stu-id="168a3-236">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
