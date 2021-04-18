---
title: Elemento ENTRYREF
description: L'elemento ENTRYREF punta agli elementi ENTRY in un metafile esterno.
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- Finestra elementi ENTRYREF Media Player
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 520a4262baf17badb136b55e7b2e216bf89d7edf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325254"
---
# <a name="entryref-element"></a><span data-ttu-id="4f531-104">Elemento ENTRYREF</span><span class="sxs-lookup"><span data-stu-id="4f531-104">ENTRYREF Element</span></span>

<span data-ttu-id="4f531-105">L'elemento **ENTRYREF** punta agli elementi **entry** in un metafile esterno.</span><span class="sxs-lookup"><span data-stu-id="4f531-105">The **ENTRYREF** element points to the **ENTRY** elements in an external metafile.</span></span>

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="4f531-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="4f531-106">Attributes</span></span>

<span data-ttu-id="4f531-107">**Href** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="4f531-107">**HREF** (required)</span></span>

<span data-ttu-id="4f531-108">URL di un metafile a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="4f531-108">URL to a referenced metafile.</span></span>

<span data-ttu-id="4f531-109">**CLIENTBIND**</span><span class="sxs-lookup"><span data-stu-id="4f531-109">**CLIENTBIND**</span></span>

<span data-ttu-id="4f531-110">Questo attributo non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="4f531-110">This attribute is no longer supported.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="4f531-111">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="4f531-111">Parent/Child Elements</span></span>



| <span data-ttu-id="4f531-112">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="4f531-112">Hierarchy</span></span>       | <span data-ttu-id="4f531-113">Elementi</span><span class="sxs-lookup"><span data-stu-id="4f531-113">Elements</span></span>                       |
|-----------------|--------------------------------|
| <span data-ttu-id="4f531-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="4f531-114">Parent elements</span></span> | <span data-ttu-id="4f531-115">**ASX**, **evento**, **ripetizione**</span><span class="sxs-lookup"><span data-stu-id="4f531-115">**ASX**, **EVENT**, **REPEAT**</span></span> |
| <span data-ttu-id="4f531-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="4f531-116">Child elements</span></span>  | <span data-ttu-id="4f531-117">nessuno</span><span class="sxs-lookup"><span data-stu-id="4f531-117">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="4f531-118">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="4f531-118">Remarks</span></span>

<span data-ttu-id="4f531-119">Questo elemento punta al contenuto di un metafile esterno.</span><span class="sxs-lookup"><span data-stu-id="4f531-119">This element points to the contents of an external metafile.</span></span> <span data-ttu-id="4f531-120">Windows Media Player elabora gli elementi **voce** del metafile a cui si fa riferimento come se fossero inclusi nel metafile primario nella posizione dell'elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="4f531-120">Windows Media Player processes the **ENTRY** elements of the referenced metafile as if they were included in the primary metafile at the position of the **ENTRYREF** element.</span></span> <span data-ttu-id="4f531-121">Tuttavia, ignora qualsiasi elemento **entry** nel metafile a cui si fa riferimento con l'attributo **SKIPIFREF** impostato su Yes.</span><span class="sxs-lookup"><span data-stu-id="4f531-121">However, it skips any **ENTRY** elements in the referenced metafile that have the **SKIPIFREF** attribute set to YES.</span></span>

<span data-ttu-id="4f531-122">Windows Media Player 7,0, 7,1 e Windows Media Player per Windows XP ignorano tutti gli elementi **ENTRYREF** nel metafile a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="4f531-122">Windows Media Player 7.0, 7.1, and Windows Media Player for Windows XP ignore any **ENTRYREF** elements in the referenced metafile.</span></span> <span data-ttu-id="4f531-123">Di conseguenza, i metafile possono essere annidati solo a livello profondo quando si usano queste versioni del lettore.</span><span class="sxs-lookup"><span data-stu-id="4f531-123">Thus, metafiles can only be nested one level deep when using these versions of the Player.</span></span> <span data-ttu-id="4f531-124">Windows Media Player ignora anche l'elemento **ASX** nel file a cui si fa riferimento insieme ai relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="4f531-124">Windows Media Player also ignores the **ASX** element in the referenced file along with its attributes.</span></span> <span data-ttu-id="4f531-125">Windows Media Player 9 Series o versioni successive supporta la nidificazione di metafile fino a cinque livelli di profondità.</span><span class="sxs-lookup"><span data-stu-id="4f531-125">Windows Media Player 9 Series or later supports nesting metafiles up to five levels deep.</span></span>

<span data-ttu-id="4f531-126">L'URL specificato nell'attributo **href** diventa l'URL di base per qualsiasi URL relativo nel metafile esterno.</span><span class="sxs-lookup"><span data-stu-id="4f531-126">The URL specified in the **HREF** attribute becomes the base URL for any relative URLs in the external metafile.</span></span> <span data-ttu-id="4f531-127">Questo URL viene usato quando una voce del metafile esterno viene riprodotta e l'utente la aggiunge alla libreria.</span><span class="sxs-lookup"><span data-stu-id="4f531-127">This URL is used when an entry from the external metafile is playing and the user adds it to the library.</span></span>

## <a name="examples"></a><span data-ttu-id="4f531-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="4f531-128">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example of Using EntryRef</TITLE>
   <ENTRYREF HREF="https://sample.microsoft.com/metafile.asx" />
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="4f531-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f531-129">Requirements</span></span>



| <span data-ttu-id="4f531-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f531-130">Requirement</span></span> | <span data-ttu-id="4f531-131">Valore</span><span class="sxs-lookup"><span data-stu-id="4f531-131">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="4f531-132">Versione</span><span class="sxs-lookup"><span data-stu-id="4f531-132">Version</span></span><br/> | <span data-ttu-id="4f531-133">Windows Media Player versione 70 o successiva</span><span class="sxs-lookup"><span data-stu-id="4f531-133">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f531-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f531-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f531-135">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4f531-135">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="4f531-136">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4f531-136">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





