---
description: Voci del registro di sistema Decoder-Specific
ms.assetid: 64ef260a-ed7f-4253-a644-bd3352b0ee41
title: Voci del registro di sistema Decoder-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17485e7adca62abd31643d84d371a0002724ea9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319116"
---
# <a name="decoder-specific-registry-entries"></a><span data-ttu-id="0276c-103">Voci del registro di sistema Decoder-Specific</span><span class="sxs-lookup"><span data-stu-id="0276c-103">Decoder-Specific Registry Entries</span></span>


<span data-ttu-id="0276c-104">Oltre alle voci del registro di sistema necessarie per tutti i codificatori e i decodificatori, le voci del registro di sistema seguenti sono necessarie specificamente per i decodificatori.</span><span class="sxs-lookup"><span data-stu-id="0276c-104">In addition to the registry entries required for all encoders and decoders, the following registry entries are required specifically for decoders.</span></span>

<span data-ttu-id="0276c-105">Queste voci registrano il decodificatore sotto la categoria di decodificatori di Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="0276c-105">These entries register your decoder under the category of Windows Imaging Component (WIC) decoders.</span></span> <span data-ttu-id="0276c-106">Il primo GUID in queste voci è l'identificatore di categoria (CATId) per [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="0276c-106">The first GUID in these entries is the category identifier (CATID) for [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {7ED96837-96F0-4812-B211-F13C24117ED3}
         Instance
            {Decoder CLSID}
               CLSID = {Decoder CLSID}
               FriendlyName = {Name of Decoder}
```

<span data-ttu-id="0276c-107">Come indicato nella sezione [individuazione ed arbitraggio](-wic-howwicworks.md) del funzionamento del componente Imaging di Windows, il meccanismo che consente di individuare un decodificatore appropriato per un'immagine specifica in fase di esecuzione è basato sulla corrispondenza di uno schema di identificazione incorporato nel file di immagine con un modello specificato nella voce del registro di sistema del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="0276c-107">As noted in [Discovery and Arbitration](-wic-howwicworks.md) section of How The Windows Imaging Component Works, the mechanism that enables an appropriate decoder for a specific image to be discovered at run time is based on matching an identifying pattern embedded in the image file with a pattern specified in the decoder’s registry entry.</span></span> <span data-ttu-id="0276c-108">Per abilitare l'individuazione in fase di esecuzione dei decodificatori, è necessario registrare il modello di identificazione univoco per il formato di immagine come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="0276c-108">To enable run-time discovery of decoders, you must register the unique identifying pattern for your image format as follows.</span></span> <span data-ttu-id="0276c-109">Tutte queste voci del registro di sistema sono necessarie, ad eccezione della voce **EndOfStream** , che è facoltativa, come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0276c-109">All of these registry entries are required except for the **EndOfStream** entry, which is optional, as described in the following table.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Decoder CLSID}
         Patterns
            {0}
               Position = Offset in block
               Length = Length of pattern
               Pattern = Pattern to match
               Mask = FF FF FF FF
               EndOfStream = 0|1
```



| <span data-ttu-id="0276c-110">Valore</span><span class="sxs-lookup"><span data-stu-id="0276c-110">Value</span></span>       | <span data-ttu-id="0276c-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0276c-111">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0276c-112">Posizione</span><span class="sxs-lookup"><span data-stu-id="0276c-112">Position</span></span>    | <span data-ttu-id="0276c-113">Offset nel file in cui è possibile trovare il modello.</span><span class="sxs-lookup"><span data-stu-id="0276c-113">The offset into the file where the pattern can be found.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="0276c-114">Length</span><span class="sxs-lookup"><span data-stu-id="0276c-114">Length</span></span>      | <span data-ttu-id="0276c-115">Lunghezza del modello.</span><span class="sxs-lookup"><span data-stu-id="0276c-115">The length of the pattern.</span></span>                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="0276c-116">Modello</span><span class="sxs-lookup"><span data-stu-id="0276c-116">Pattern</span></span>     | <span data-ttu-id="0276c-117">Bit effettivi che costituiscono il modello.</span><span class="sxs-lookup"><span data-stu-id="0276c-117">The actual bits that make up the pattern.</span></span> <span data-ttu-id="0276c-118">Si tratta dei bit che corrispondono al modello di identificazione in un file di immagine durante l'individuazione.</span><span class="sxs-lookup"><span data-stu-id="0276c-118">These are the bits that are matched against the identifying pattern in an image file during discovery.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="0276c-119">Mask</span><span class="sxs-lookup"><span data-stu-id="0276c-119">Mask</span></span>        | <span data-ttu-id="0276c-120">Consente i valori jolly nei criteri.</span><span class="sxs-lookup"><span data-stu-id="0276c-120">Allows for wildcard values in patterns.</span></span> <span data-ttu-id="0276c-121">La maschera viene applicata eseguendo un'operazione AND logica sul modello e sulla maschera.</span><span class="sxs-lookup"><span data-stu-id="0276c-121">The mask is applied by performing a logical AND operation on the pattern and the mask.</span></span> <span data-ttu-id="0276c-122">Qualsiasi bit del modello che corrisponde a un bit nella maschera con un valore pari a 0 viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="0276c-122">Any bit in the pattern that corresponds to a bit in the mask with a value of 0 is ignored.</span></span>                                                                                                       |
| <span data-ttu-id="0276c-123">EndOfStream</span><span class="sxs-lookup"><span data-stu-id="0276c-123">EndOfStream</span></span> | <span data-ttu-id="0276c-124">L'offset del pattern di identificazione deve essere calcolato dalla fine del flusso, anziché dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="0276c-124">The offset of the identifying pattern should be calculated from the end of the stream, rather than the beginning.</span></span> <span data-ttu-id="0276c-125">Alcuni formati di immagine posizionano il modello di identificazione alla fine del file o in prossimità della fine del file.</span><span class="sxs-lookup"><span data-stu-id="0276c-125">Some image formats place the identifying pattern at or near the end of the file.</span></span> <span data-ttu-id="0276c-126">Poiché l'impostazione predefinita prevede la ricerca dall'inizio, a meno che il modello non sia vicino alla fine del file, è possibile omettere questa voce.</span><span class="sxs-lookup"><span data-stu-id="0276c-126">Because the default is to seek from the beginning, unless your pattern is near the end of the file, you can omit this entry.</span></span> |



 

<span data-ttu-id="0276c-127">Un codec può supportare più di un modello di identificazione.</span><span class="sxs-lookup"><span data-stu-id="0276c-127">A codec can support more than one identifying pattern.</span></span> <span data-ttu-id="0276c-128">In tal caso, è necessario ripetere tutte le chiavi in **HKEY \_ classi \_ radice \\ CLSID \\ {decodificatore CLSID} \\ modelli** e usare la chiave numerica (0 nell'esempio) per distinguere tra i diversi modelli.</span><span class="sxs-lookup"><span data-stu-id="0276c-128">In that case, you would repeat all of the keys under **HKEY\_CLASSES\_ROOT\\CLSID\\{Decoder CLSID}\\Patterns**, and use the numerical key (0 in the example) to distinguish between the different patterns.</span></span> <span data-ttu-id="0276c-129">È necessario includere ognuno dei quattro valori sotto la chiave per ogni modello.</span><span class="sxs-lookup"><span data-stu-id="0276c-129">You must include each of the four values under the key for each pattern.</span></span>

## <a name="registering-a-container-format-with-metadata-readers"></a><span data-ttu-id="0276c-130">Registrazione di un formato contenitore con i lettori di metadati</span><span class="sxs-lookup"><span data-stu-id="0276c-130">Registering a Container Format with Metadata Readers</span></span>

<span data-ttu-id="0276c-131">Se si crea un nuovo formato del contenitore per il codec, è necessario creare anche le voci del registro di sistema per supportare l'individuazione dei lettori di metadati per i blocchi di metadati nelle immagini, proprio come per i writer dei metadati.</span><span class="sxs-lookup"><span data-stu-id="0276c-131">If you create a new container format for your codec, you must also create registry entries to support discovery of metadata readers for the metadata blocks in your images, just as you did for the metadata writers.</span></span> <span data-ttu-id="0276c-132">È necessario creare le voci seguenti nell'identificatore di classe (CLSID) del lettore di metadati per ogni formato di metadati supportato dal formato del contenitore.</span><span class="sxs-lookup"><span data-stu-id="0276c-132">The following entries need to be created under the class identifier (CLSID) of the metadata reader for each metadata format your container format supports.</span></span> <span data-ttu-id="0276c-133">Si noti che, se il codec usa un contenitore Tagged Image File Format (TIFF), queste informazioni sono già presenti nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0276c-133">(Note that, if your codec uses a Tagged Image File Format (TIFF) container, then this information is already in the registry.)</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Reader CLSID}
         Containers
            {Container Format GUID}
               
                  Position = Offset relative to its container
                  Pattern = Pattern used for metadata header
                  Mask = FF FF FF FF
                  DataOffset = Offset from beginning of header
```

<span data-ttu-id="0276c-134">Poiché le voci per i lettori di metadati vengono usate anche per l'individuazione, sono molto simili alle voci per i decodificatori.</span><span class="sxs-lookup"><span data-stu-id="0276c-134">Because the entries for metadata readers are also used for discovery, they are very similar to the entries for decoders.</span></span> <span data-ttu-id="0276c-135">Queste voci vengono usate dalla factory dei componenti per trovare i lettori di metadati supportati dal contenitore e per selezionare quello appropriato, quando l'implementazione di [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) richiede un lettore di metadati.</span><span class="sxs-lookup"><span data-stu-id="0276c-135">These entries are used by the component factory to find the metadata readers supported by your container, and to select the appropriate one, when your [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) implementation requests a metadata reader.</span></span>



| <span data-ttu-id="0276c-136">Valore</span><span class="sxs-lookup"><span data-stu-id="0276c-136">Value</span></span>      | <span data-ttu-id="0276c-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0276c-137">Description</span></span>                                                                                                                                                                                                                                                                 |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0276c-138">Posizione</span><span class="sxs-lookup"><span data-stu-id="0276c-138">Position</span></span>   | <span data-ttu-id="0276c-139">Offset nel contenitore del blocco di metadati in cui è possibile trovare l'intestazione dei metadati.</span><span class="sxs-lookup"><span data-stu-id="0276c-139">The offset in the metadata block’s container where the metadata header can be found.</span></span> <span data-ttu-id="0276c-140">Per i blocchi di metadati di primo livello, si tratta dell'offset nel flusso di file.</span><span class="sxs-lookup"><span data-stu-id="0276c-140">For top-level metadata blocks, this is the offset in the file stream.</span></span> <span data-ttu-id="0276c-141">Per i blocchi di metadati annidati in altri blocchi di metadati, si tratta dell'offset rispetto al blocco di metadati contenitore.</span><span class="sxs-lookup"><span data-stu-id="0276c-141">For metadata blocks nested in other metadata blocks, it is the offset relative to the containing metadata block.</span></span> |
| <span data-ttu-id="0276c-142">Modello</span><span class="sxs-lookup"><span data-stu-id="0276c-142">Pattern</span></span>    | <span data-ttu-id="0276c-143">Bit effettivi che costituiscono il modello.</span><span class="sxs-lookup"><span data-stu-id="0276c-143">The actual bits that make up the pattern.</span></span> <span data-ttu-id="0276c-144">Si tratta dei bit che corrispondono al modello di identificazione in un file di immagine durante l'individuazione.</span><span class="sxs-lookup"><span data-stu-id="0276c-144">These are the bits that are matched against the identifying pattern in an image file during discovery.</span></span>                                                                                                                            |
| <span data-ttu-id="0276c-145">Mask</span><span class="sxs-lookup"><span data-stu-id="0276c-145">Mask</span></span>       | <span data-ttu-id="0276c-146">L'intestazione dei metadati è generalmente definita dal gestore di metadati.</span><span class="sxs-lookup"><span data-stu-id="0276c-146">The metadata header is generally defined by the metadata handler.</span></span> <span data-ttu-id="0276c-147">È consigliabile usare l'intestazione di metadati standard per ogni lettore, a meno che, per qualche motivo, il modello deve avere un formato diverso nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="0276c-147">You should use the standard metadata header for each reader unless, for some reason, the pattern must have a different format in your container.</span></span>                                                          |
| <span data-ttu-id="0276c-148">DataOffset</span><span class="sxs-lookup"><span data-stu-id="0276c-148">DataOffset</span></span> | <span data-ttu-id="0276c-149">Offset dall'inizio dell'intestazione dei metadati in corrispondenza della quale iniziano i dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="0276c-149">The offset from the beginning of the metadata header at which the actual data begins.</span></span> <span data-ttu-id="0276c-150">Nei casi in cui i metadati non si trovano in un offset specifico dall'intestazione, questa voce può essere omessa.</span><span class="sxs-lookup"><span data-stu-id="0276c-150">In cases where the metadata isn’t located at a specific offset from the header, this entry can be omitted.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="0276c-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0276c-151">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0276c-152">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="0276c-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0276c-153">Voci del registro di sistema specifiche del codificatore</span><span class="sxs-lookup"><span data-stu-id="0276c-153">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)
</dt> <dt>

[<span data-ttu-id="0276c-154">Integrazione con raccolta foto di Windows e Esplora risorse</span><span class="sxs-lookup"><span data-stu-id="0276c-154">Integration with Windows Photo Gallery and Windows Explorer</span></span>](-wic-integrationregentries.md)
</dt> <dt>

[<span data-ttu-id="0276c-155">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="0276c-155">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="0276c-156">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="0276c-156">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



