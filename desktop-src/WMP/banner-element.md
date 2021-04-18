---
title: Elemento BANNER
description: L'elemento BANNER definisce un URL di un file grafico che verrà visualizzato nel pannello di visualizzazione.
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- Finestra di elemento BANNER Media Player
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e257c14e5908482cdf8de458c259bc64a55c6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331020"
---
# <a name="banner-element"></a><span data-ttu-id="18e51-104">Elemento BANNER</span><span class="sxs-lookup"><span data-stu-id="18e51-104">BANNER Element</span></span>

<span data-ttu-id="18e51-105">L'elemento **banner** definisce un URL di un file grafico che verrà visualizzato nel pannello di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="18e51-105">The **BANNER** element defines a URL to a graphic file that will appear in the display panel.</span></span>

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a><span data-ttu-id="18e51-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="18e51-106">Attributes</span></span>

<span data-ttu-id="18e51-107">**Href** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="18e51-107">**HREF** (required)</span></span>

<span data-ttu-id="18e51-108">URL di un file grafico visualizzato nel pannello di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="18e51-108">URL to a graphic file that is displayed in the display panel.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="18e51-109">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="18e51-109">Parent/Child Elements</span></span>



| <span data-ttu-id="18e51-110">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="18e51-110">Hierarchy</span></span>       | <span data-ttu-id="18e51-111">Elementi</span><span class="sxs-lookup"><span data-stu-id="18e51-111">Elements</span></span>                   |
|-----------------|----------------------------|
| <span data-ttu-id="18e51-112">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="18e51-112">Parent elements</span></span> | <span data-ttu-id="18e51-113">**ASX**, **voce**</span><span class="sxs-lookup"><span data-stu-id="18e51-113">**ASX**, **ENTRY**</span></span>         |
| <span data-ttu-id="18e51-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="18e51-114">Child elements</span></span>  | <span data-ttu-id="18e51-115">**abstract**, **moreinfo**</span><span class="sxs-lookup"><span data-stu-id="18e51-115">**ABSTRACT**, **MOREINFO**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="18e51-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="18e51-116">Remarks</span></span>

<span data-ttu-id="18e51-117">Questo elemento definisce un URL di un file grafico visualizzato nel pannello di visualizzazione di Windows Media Player, sotto il contenuto video.</span><span class="sxs-lookup"><span data-stu-id="18e51-117">This element defines a URL to a graphic file that appears in the Windows Media Player display panel, beneath the video content.</span></span> <span data-ttu-id="18e51-118">Se il supporto è solo audio, l'icona del banner viene visualizzata da sola.</span><span class="sxs-lookup"><span data-stu-id="18e51-118">If the media is audio only, the banner graphic is displayed by itself.</span></span> <span data-ttu-id="18e51-119">Windows Media Player riserva uno spazio 32 pixel di altezza di 194 pixel di larghezza (barra del banner) per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="18e51-119">Windows Media Player reserves a space 32 pixels high by 194 pixels wide (the banner bar) for the graphic.</span></span> <span data-ttu-id="18e51-120">Se il grafico definito nell'URL è più piccolo, viene visualizzato con le dimensioni originali.</span><span class="sxs-lookup"><span data-stu-id="18e51-120">If the graphic defined in the URL is smaller than that, it displays at its original size.</span></span> <span data-ttu-id="18e51-121">Se il grafico è più grande dello spazio riservato, Windows Media Player ridurrà l'immagine per adattarla allo spazio.</span><span class="sxs-lookup"><span data-stu-id="18e51-121">If the graphic is larger than the reserved space, Windows Media Player will crop the image to fit the space.</span></span>

<span data-ttu-id="18e51-122">È possibile usare un elemento **astratto** nell'ambito dell'elemento **banner** per visualizzare il testo come descrizione comando quando l'utente posiziona il puntatore del mouse sull'icona del banner.</span><span class="sxs-lookup"><span data-stu-id="18e51-122">You can use an **ABSTRACT** element within the scope of the **BANNER** element to display text as a ToolTip when the user pauses the mouse pointer over the banner graphic.</span></span> <span data-ttu-id="18e51-123">Un elemento **moreinfo** all'interno di un elemento **banner** definisce un URL a cui l'utente viene utilizzato quando l'utente fa clic sull'icona del banner.</span><span class="sxs-lookup"><span data-stu-id="18e51-123">A **MOREINFO** element within a **BANNER** element defines a URL to which the user is taken when the user clicks the banner graphic.</span></span> <span data-ttu-id="18e51-124">L'URL può essere qualsiasi percorso o protocollo, ad esempio un collegamento di posta elettronica, un URL Hypertext Transfer Protocol (HTTP) a un sito Web o anche un comando Microsoft JScript. Quando il puntatore viene spostato sul grafico, il grafico viene visualizzato in rilievo e ha un aspetto simile a un pulsante.</span><span class="sxs-lookup"><span data-stu-id="18e51-124">(The URL can be any path or protocol, such as an email link, a Hypertext Transfer Protocol (HTTP) URL to a website, or even a Microsoft JScript command.) When the pointer is moved over the graphic, the graphic becomes embossed and looks like a button.</span></span>

<span data-ttu-id="18e51-125">Viene visualizzato un elemento **banner** definito per un elemento **ASX** mentre tutti i clip della playlist sono in riproduzione.</span><span class="sxs-lookup"><span data-stu-id="18e51-125">A **BANNER** element defined for an **ASX** element displays while all clips in the playlist are playing.</span></span> <span data-ttu-id="18e51-126">Un elemento **banner** definito in un elemento **entry** viene visualizzato solo quando il clip sta eseguendo la riproduzione e durante tale periodo esegue l'override di qualsiasi banner definito all'interno dell'elemento **ASX** padre.</span><span class="sxs-lookup"><span data-stu-id="18e51-126">A **BANNER** element defined in an **ENTRY** element displays only while that clip is playing, and during that time overrides any banner defined within the parent **ASX** element.</span></span> <span data-ttu-id="18e51-127">È possibile specificare in che modo Windows Media Player riserva spazio per il banner impostando l'attributo **BANNERBAR** dell'elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="18e51-127">You can specify how Windows Media Player reserves space for the banner by setting the **BANNERBAR** attribute of the **ASX** element.</span></span>

<span data-ttu-id="18e51-128">Le immagini banner non sono supportate con i file DRM o quando Windows Media Player è incorporato in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="18e51-128">Banner images are not supported with DRM files or when Windows Media Player is embedded in a webpage.</span></span>

## <a name="examples"></a><span data-ttu-id="18e51-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="18e51-129">Examples</span></span>

<span data-ttu-id="18e51-130">Di seguito è riportato un esempio di elemento **banner** senza elementi figlio:</span><span class="sxs-lookup"><span data-stu-id="18e51-130">The following is an example of a **BANNER** element without child elements:</span></span>


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



<span data-ttu-id="18e51-131">Di seguito è riportato un esempio di un elemento **banner** contenente elementi **abstract** e **moreinfo** .</span><span class="sxs-lookup"><span data-stu-id="18e51-131">The following is an example of a **BANNER** element containing **ABSTRACT** and **MOREINFO** elements.</span></span>


```XML
<BANNER HREF="https://www.proseware.com/logos/banner1.bmp">
    <ABSTRACT>Click here to go to our website.</ABSTRACT>
    <MOREINFO HREF="https://sample.microsoft.com" />
    <!-- The text in the Abstract element displays as a 
         ToolTip when the mouse hovers over the banner 
         graphic. When a user clicks the banner, the URL 
         given in the MoreInfo element opens in the 
         browser. -->
</BANNER>
```



## <a name="requirements"></a><span data-ttu-id="18e51-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18e51-132">Requirements</span></span>



| <span data-ttu-id="18e51-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="18e51-133">Requirement</span></span> | <span data-ttu-id="18e51-134">Valore</span><span class="sxs-lookup"><span data-stu-id="18e51-134">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="18e51-135">Versione</span><span class="sxs-lookup"><span data-stu-id="18e51-135">Version</span></span><br/> | <span data-ttu-id="18e51-136">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="18e51-136">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="18e51-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18e51-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18e51-138">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="18e51-138">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="18e51-139">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="18e51-139">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





