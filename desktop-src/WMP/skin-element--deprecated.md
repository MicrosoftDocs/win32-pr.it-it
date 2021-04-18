---
title: Elemento SKIN (deprecato)
description: Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- Elemento SKIN (deprecato) Windows Media Player
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abf503706dec131eef411ebaf3625071e2b31098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329915"
---
# <a name="skin-element-deprecated"></a><span data-ttu-id="dda51-104">Elemento SKIN (deprecato)</span><span class="sxs-lookup"><span data-stu-id="dda51-104">SKIN Element (deprecated)</span></span>

<span data-ttu-id="dda51-105">Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="dda51-105">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="dda51-106">L'elemento **Skin** specifica un URL per un bordo.</span><span class="sxs-lookup"><span data-stu-id="dda51-106">The **SKIN** element specifies a URL to a border.</span></span>

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="dda51-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="dda51-107">Attributes</span></span>

<span data-ttu-id="dda51-108">**Href** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="dda51-108">**HREF** (required)</span></span>

<span data-ttu-id="dda51-109">URL per un file di bordo compresso con estensione WMZ.</span><span class="sxs-lookup"><span data-stu-id="dda51-109">URL for a compressed border file with a file name extension .wmz.</span></span> <span data-ttu-id="dda51-110">Per Windows Media Player 9 serie o versioni successive, questo valore può fare riferimento solo ai file di bordo nel disco rigido dell'utente che si trova nella stessa directory della playlist del metafile.</span><span class="sxs-lookup"><span data-stu-id="dda51-110">For Windows Media Player 9 Series or later, this value can reference only border files on the user's hard disk located in the same directory as the metafile playlist.</span></span> <span data-ttu-id="dda51-111">Vedere il codice di esempio.</span><span class="sxs-lookup"><span data-stu-id="dda51-111">See the example code.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="dda51-112">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="dda51-112">Parent/Child Elements</span></span>



| <span data-ttu-id="dda51-113">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="dda51-113">Hierarchy</span></span>       | <span data-ttu-id="dda51-114">Elementi</span><span class="sxs-lookup"><span data-stu-id="dda51-114">Elements</span></span> |
|-----------------|----------|
| <span data-ttu-id="dda51-115">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="dda51-115">Parent elements</span></span> | <span data-ttu-id="dda51-116">**ASX**</span><span class="sxs-lookup"><span data-stu-id="dda51-116">**ASX**</span></span>  |
| <span data-ttu-id="dda51-117">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="dda51-117">Child elements</span></span>  | <span data-ttu-id="dda51-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="dda51-118">None</span></span>     |



 

## <a name="remarks"></a><span data-ttu-id="dda51-119">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="dda51-119">Remarks</span></span>

<span data-ttu-id="dda51-120">L'elemento **Skin** viene usato per creare un bordo, che è simile a un oggetto Skin, ma viene visualizzato nell'area **Now Play** della modalità Full Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="dda51-120">The **SKIN** element is used to create a border, which is similar to a skin but is displayed in the **Now Playing** area of the full mode Windows Media Player.</span></span> <span data-ttu-id="dda51-121">L'elemento **Skin** viene usato solo per i bordi, che vengono visualizzati all'interno del Media Player di Windows in modalità completa e non per le interfacce normali, che sostituiscono completamente le Media Player di Windows in modalità compatta.</span><span class="sxs-lookup"><span data-stu-id="dda51-121">The **SKIN** element is used only for borders, which appear inside the full mode Windows Media Player, and not for regular skins, which entirely replace the compact mode Windows Media Player.</span></span>

<span data-ttu-id="dda51-122">In un pacchetto di download di Windows Media (con estensione di file WMD), l'elemento **Skin** Abilita un bordo per il contenuto e il collegamento ad altri siti.</span><span class="sxs-lookup"><span data-stu-id="dda51-122">In a Windows Media Download Package (with a .wmd file name extension), the **SKIN** element enables a border to have content and link to other sites.</span></span> <span data-ttu-id="dda51-123">Il pacchetto di download di Windows Media è un file compresso che contiene un file di bordo e un metafile di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dda51-123">The Windows Media Download Package is a compressed file that contains a border file and a Windows Media metafile.</span></span> <span data-ttu-id="dda51-124">Il file del bordo (con estensione WMZ) viene compresso e include un file di definizione dell'interfaccia (con estensione WMS).</span><span class="sxs-lookup"><span data-stu-id="dda51-124">The border file (with a .wmz file name extension) is compressed, and includes a skin definition file (with a .wms file name extension).</span></span>

<span data-ttu-id="dda51-125">Un elemento **Skin** è costituito da tre componenti:</span><span class="sxs-lookup"><span data-stu-id="dda51-125">A **SKIN** element has three components:</span></span>

-   <span data-ttu-id="dda51-126">Interfaccia personalizzata</span><span class="sxs-lookup"><span data-stu-id="dda51-126">A skin</span></span>
-   <span data-ttu-id="dda51-127">Contenuto</span><span class="sxs-lookup"><span data-stu-id="dda51-127">Some content</span></span>
-   <span data-ttu-id="dda51-128">Un metafile</span><span class="sxs-lookup"><span data-stu-id="dda51-128">A metafile</span></span>

<span data-ttu-id="dda51-129">Le interfacce incluse nei pacchetti di download di Windows Media devono essere rettangolari in forma.</span><span class="sxs-lookup"><span data-stu-id="dda51-129">Skins included with Windows Media Download Packages must be rectangular in shape.</span></span> <span data-ttu-id="dda51-130">La creazione di bordi con interfacce che non sono rettangolari può produrre risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="dda51-130">Creating borders with skins that are not rectangular may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="dda51-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="dda51-131">Examples</span></span>


```XML
<ASX version = "3.0">
    <TITLE>A Skin Element</TITLE>
    <SKIN HREF = "YourTest.wmz" />

    <ENTRY>
        <PARAM name="YourAlbumTitle" value="YourTitle.jpg"/>
        <PARAM name="link" value="https://www.proseware.com"/>
        <TITLE>(The Artist)-YourTitle</TITLE>
        <REF HREF="(The Artist)-YourSongTitle.wma"/>
    </ENTRY>

</ASX>
```



## <a name="requirements"></a><span data-ttu-id="dda51-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dda51-132">Requirements</span></span>



| <span data-ttu-id="dda51-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="dda51-133">Requirement</span></span> | <span data-ttu-id="dda51-134">Valore</span><span class="sxs-lookup"><span data-stu-id="dda51-134">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="dda51-135">Versione</span><span class="sxs-lookup"><span data-stu-id="dda51-135">Version</span></span><br/> | <span data-ttu-id="dda51-136">Windows Media Player versione 70 o successiva</span><span class="sxs-lookup"><span data-stu-id="dda51-136">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dda51-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dda51-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dda51-138">**Bordi per Windows Media Player (deprecato)**</span><span class="sxs-lookup"><span data-stu-id="dda51-138">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="dda51-139">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="dda51-139">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="dda51-140">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="dda51-140">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





