---
title: Valori di attributo per il contenuto TV
description: Valori di attributo per il contenuto TV
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
keywords:
- Media Player di Windows, attributi per elementi multimediali
- Modello a oggetti di Windows Media Player, attributi per elementi multimediali
- modello a oggetti, attributi per elementi multimediali
- Windows Media Player Mobile, attributi per elementi multimediali
- Controllo ActiveX di Windows Media Player, attributi per elementi multimediali
- Controllo ActiveX Windows Media Player Mobile, attributi per elementi multimediali
- Controllo ActiveX, attributi per elementi multimediali
- Windows Media Player Library, attributi per elementi multimediali
- libreria, attributi per elementi multimediali
- attributi, contenuto TV
- Valori degli attributi di contenuto TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb63e872edd80944772a320da5f2094e6d8f5757
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045351"
---
# <a name="attribute-values-for-tv-content"></a><span data-ttu-id="26582-114">Valori di attributo per il contenuto TV</span><span class="sxs-lookup"><span data-stu-id="26582-114">Attribute Values for TV Content</span></span>

<span data-ttu-id="26582-115">In questo argomento, l'oggetto **Player** è stato definito nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="26582-115">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="26582-116">Windows Media Player 10 o versione successiva può organizzare il contenuto della TV nella libreria.</span><span class="sxs-lookup"><span data-stu-id="26582-116">Windows Media Player 10 or later can organize TV content in the library.</span></span> <span data-ttu-id="26582-117">Windows Media Player considera il contenuto TV come una sottocategoria di contenuto video.</span><span class="sxs-lookup"><span data-stu-id="26582-117">Windows Media Player treats TV content as a subcategory of video content.</span></span> <span data-ttu-id="26582-118">Per visualizzare il contenuto video nei nodi TV della libreria, impostare gli attributi **WM/MediaClassPrimaryID** e **WM/MediaClassSecondaryID** sui valori nella tabella seguente utilizzando il *supporto*. metodo **setItemInfo** :</span><span class="sxs-lookup"><span data-stu-id="26582-118">To make video content appear in the TV nodes in the library, set the **WM/MediaClassPrimaryID** and the **WM/MediaClassSecondaryID** attributes to the values in the following table by using the *media*.**setItemInfo** method:</span></span>



| <span data-ttu-id="26582-119">Attributo</span><span class="sxs-lookup"><span data-stu-id="26582-119">Attribute</span></span>                    | <span data-ttu-id="26582-120">Valore</span><span class="sxs-lookup"><span data-stu-id="26582-120">Value</span></span>                                |
|------------------------------|--------------------------------------|
| <span data-ttu-id="26582-121">**WM/MediaClassPrimaryID**</span><span class="sxs-lookup"><span data-stu-id="26582-121">**WM/MediaClassPrimaryID**</span></span>   | <span data-ttu-id="26582-122">DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B</span><span class="sxs-lookup"><span data-stu-id="26582-122">DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B</span></span> |
| <span data-ttu-id="26582-123">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="26582-123">**WM/MediaClassSecondaryID**</span></span> | <span data-ttu-id="26582-124">BA7F258A-62F7-47A9-B21F-4651C42A000E</span><span class="sxs-lookup"><span data-stu-id="26582-124">BA7F258A-62F7-47A9-B21F-4651C42A000E</span></span> |



 

<span data-ttu-id="26582-125">È anche possibile usare questi valori per determinare se un particolare elemento multimediale digitale contiene contenuto TV usando il *supporto*. **GetItemInfo** o *supporti*. metodi **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="26582-125">You can also use these values to determine whether a particular digital media item contains TV content by using the *media*.**getItemInfo** or *media*.**getItemInfoByType** methods.</span></span>

<span data-ttu-id="26582-126">Ricordarsi di usare i valori **GUID** come valori **stringa** quando si specificano o si recuperano questi valori.</span><span class="sxs-lookup"><span data-stu-id="26582-126">Remember to use the **GUID** values as **string** values when specifying or retrieving these values.</span></span>

<span data-ttu-id="26582-127">Il codice di esempio C# seguente imposta gli attributi della classe multimediale in modo che un elemento multimediale venga identificato come contenuto TV.</span><span class="sxs-lookup"><span data-stu-id="26582-127">The following C# example code sets the media class attributes so that a media item will be identified as TV content.</span></span>


```C++
// Initialize the media object.
// This code assumes only 1 item named MyFile.
IWMPMedia3 media = (IWMPMedia3)Player.mediaCollection.getByName("MyFile").item(0);

// Set the primary media-class identifier.
media.setItemInfo("WM/MediaClassPrimaryID", "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B");

// Set the secondary media-class identifier.
media.setItemInfo("WM/MediaClassSecondaryID", "BA7F258A-62F7-47A9-B21F-4651C42A000E");

```



<span data-ttu-id="26582-128">Per ulteriori informazioni sui possibili valori per gli attributi delle classi multimediali, vedere le [linee guida sull'utilizzo dei metadati di Windows Media](/previous-versions/ms867702(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="26582-128">For more info about the possible values for the media class attributes, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="26582-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26582-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26582-130">**Attributi elemento multimediale**</span><span class="sxs-lookup"><span data-stu-id="26582-130">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="26582-131">**Accesso alla libreria**</span><span class="sxs-lookup"><span data-stu-id="26582-131">**Library Access**</span></span>](library-access.md)
</dt> <dt>

[<span data-ttu-id="26582-132">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="26582-132">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 




