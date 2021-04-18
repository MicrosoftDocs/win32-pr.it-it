---
title: Elemento TITLE (Metafile)
description: L'elemento TITLE definisce una stringa di testo che specifica il titolo di un elemento ASX o ENTRY.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- Elemento TITLE (Metafile) Windows Media Player
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb58edbb3ffd99e8be557fdb05a7e51298fda14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331365"
---
# <a name="title-element-metafile"></a><span data-ttu-id="d84ee-104">Elemento TITLE (Metafile)</span><span class="sxs-lookup"><span data-stu-id="d84ee-104">TITLE Element (metafile)</span></span>

<span data-ttu-id="d84ee-105">L'elemento **title** definisce una stringa di testo che specifica il titolo di un elemento **ASX** o **entry** .</span><span class="sxs-lookup"><span data-stu-id="d84ee-105">The **TITLE** element defines a text string specifying the title for an **ASX** or **ENTRY** element.</span></span>

``` syntax
<TITLE>
   text string
</TITLE>
```

## <a name="attributes"></a><span data-ttu-id="d84ee-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="d84ee-106">Attributes</span></span>

<span data-ttu-id="d84ee-107">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="d84ee-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="d84ee-108">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="d84ee-108">Parent/Child Elements</span></span>



| <span data-ttu-id="d84ee-109">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="d84ee-109">Hierarchy</span></span>       | <span data-ttu-id="d84ee-110">Elementi</span><span class="sxs-lookup"><span data-stu-id="d84ee-110">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="d84ee-111">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d84ee-111">Parent elements</span></span> | <span data-ttu-id="d84ee-112">**ASX**, **voce**</span><span class="sxs-lookup"><span data-stu-id="d84ee-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="d84ee-113">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d84ee-113">Child elements</span></span>  | <span data-ttu-id="d84ee-114">nessuno</span><span class="sxs-lookup"><span data-stu-id="d84ee-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="d84ee-115">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="d84ee-115">Remarks</span></span>

<span data-ttu-id="d84ee-116">Questo elemento definisce una stringa di testo che specifica il titolo di un elemento **ASX** o **entry** .</span><span class="sxs-lookup"><span data-stu-id="d84ee-116">This element defines a text string that specifies the title of an **ASX** or **ENTRY** element.</span></span> <span data-ttu-id="d84ee-117">Il titolo viene visualizzato nel pannello di visualizzazione e nella finestra di dialogo **Proprietà** .</span><span class="sxs-lookup"><span data-stu-id="d84ee-117">The title is displayed in the display panel and **Properties** dialog box.</span></span>

<span data-ttu-id="d84ee-118">Quando questo elemento viene visualizzato all'interno di un elemento **ASX** , il testo viene visualizzato come **Mostra** informazioni.</span><span class="sxs-lookup"><span data-stu-id="d84ee-118">When this element appears within an **ASX** element, the text is displayed as **Show** information.</span></span> <span data-ttu-id="d84ee-119">Quando questo elemento viene visualizzato all'interno di un elemento **entry** , il testo viene visualizzato come informazioni di **ritaglio** .</span><span class="sxs-lookup"><span data-stu-id="d84ee-119">When this element appears within an **ENTRY** element, the text is displayed as **Clip** information.</span></span>

<span data-ttu-id="d84ee-120">Se un elemento **moreinfo** viene usato anche con l'elemento associato (padre), si tratta del testo del titolo che l'utente fa clic per accedere all'URL definito nell'elemento **moreinfo** .</span><span class="sxs-lookup"><span data-stu-id="d84ee-120">If a **MOREINFO** element is also used with the associated (parent) element, it is the title text that the user clicks to access the URL defined in the **MOREINFO** element.</span></span>

<span data-ttu-id="d84ee-121">Ogni elemento **ASX** e **entry** padre deve contenere al massimo un elemento **titolo** figlio.</span><span class="sxs-lookup"><span data-stu-id="d84ee-121">Each parent **ASX** and **ENTRY** element should contain at most one child **TITLE** element.</span></span> <span data-ttu-id="d84ee-122">Più elementi **title** dopo il primo verranno ignorati e non verranno visualizzati.</span><span class="sxs-lookup"><span data-stu-id="d84ee-122">Multiple **TITLE** elements after the first will be ignored and will not be displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="d84ee-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="d84ee-123">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Title of the Show</TITLE>
   <ENTRY>
      <TITLE>Title of the Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="d84ee-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d84ee-124">Requirements</span></span>



| <span data-ttu-id="d84ee-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d84ee-125">Requirement</span></span> | <span data-ttu-id="d84ee-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d84ee-126">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="d84ee-127">Versione</span><span class="sxs-lookup"><span data-stu-id="d84ee-127">Version</span></span><br/> | <span data-ttu-id="d84ee-128">Windows Media Player versione 70 o successiva</span><span class="sxs-lookup"><span data-stu-id="d84ee-128">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d84ee-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d84ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d84ee-130">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d84ee-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="d84ee-131">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d84ee-131">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





