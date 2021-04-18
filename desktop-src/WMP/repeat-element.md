---
title: Elemento REPEAT
description: L'elemento REPEAT definisce il numero di volte in cui Windows Media Player ripete uno o più elementi ENTRY o ENTRYREF.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- Ripeti finestre elementi Media Player
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aff7d5eaa9594882b029f0b02f4888d93fff01d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331584"
---
# <a name="repeat-element"></a><span data-ttu-id="f9211-104">Elemento REPEAT</span><span class="sxs-lookup"><span data-stu-id="f9211-104">REPEAT Element</span></span>

<span data-ttu-id="f9211-105">L'elemento **Repeat** definisce il numero di volte in cui Windows Media Player ripete uno o più elementi **entry** o **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="f9211-105">The **REPEAT** element defines the number of times Windows Media Player repeats one or more **ENTRY** or **ENTRYREF** elements.</span></span>

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a><span data-ttu-id="f9211-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="f9211-106">Attributes</span></span>

<span data-ttu-id="f9211-107">**COUNT**</span><span class="sxs-lookup"><span data-stu-id="f9211-107">**COUNT**</span></span>

<span data-ttu-id="f9211-108">Integer che rappresenta il numero di volte in cui Windows Media Player ripete gli elementi **entry** e **ENTRYREF** all'interno dell'ambito di questo elemento.</span><span class="sxs-lookup"><span data-stu-id="f9211-108">Integer representing the number of times Windows Media Player repeats the **ENTRY** and **ENTRYREF** elements within this element's scope.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="f9211-109">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="f9211-109">Parent/Child Elements</span></span>



| <span data-ttu-id="f9211-110">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="f9211-110">Hierarchy</span></span>       | <span data-ttu-id="f9211-111">Elementi</span><span class="sxs-lookup"><span data-stu-id="f9211-111">Elements</span></span>                |
|-----------------|-------------------------|
| <span data-ttu-id="f9211-112">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f9211-112">Parent elements</span></span> | <span data-ttu-id="f9211-113">**ASX**</span><span class="sxs-lookup"><span data-stu-id="f9211-113">**ASX**</span></span>                 |
| <span data-ttu-id="f9211-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f9211-114">Child elements</span></span>  | <span data-ttu-id="f9211-115">**voce**, **ENTRYREF**</span><span class="sxs-lookup"><span data-stu-id="f9211-115">**ENTRY**, **ENTRYREF**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f9211-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9211-116">Remarks</span></span>

<span data-ttu-id="f9211-117">Questo elemento definisce il numero di volte in cui Windows Media Player ripete o scorre i clip definiti dalla **voce** e **ENTRYREF** gli elementi all'interno dell'ambito di questo elemento.</span><span class="sxs-lookup"><span data-stu-id="f9211-117">This element defines the number of times Windows Media Player repeats, or loops through, the clips defined by the **ENTRY** and **ENTRYREF** elements within this element's scope.</span></span> <span data-ttu-id="f9211-118">Solo il primo elemento **Repeat** in un metafile è valido. gli elementi **ripetuti** successivi vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="f9211-118">Only the first **REPEAT** element in a metafile is valid; subsequent **REPEAT** elements are ignored.</span></span>

<span data-ttu-id="f9211-119">Se non è definito alcun attributo **count** , il contenuto negli elementi **entry** e **ENTRYREF** associati si ripete un numero infinito di volte.</span><span class="sxs-lookup"><span data-stu-id="f9211-119">If no **COUNT** attribute is defined, the content in the associated **ENTRY** and **ENTRYREF** elements repeats an infinite number of times.</span></span> <span data-ttu-id="f9211-120">Il valore zero fa in modo che Windows Media Player ignori l'elemento **Repeat** e riproduca il contenuto una volta.</span><span class="sxs-lookup"><span data-stu-id="f9211-120">A value of zero causes Windows Media Player to ignore the **REPEAT** element and play the content once.</span></span>

## <a name="examples"></a><span data-ttu-id="f9211-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="f9211-121">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <ENTRY>
        <REF HREF="mms://example.microsoft.com/clip1.asf" />
<!-- This clip plays once. -->
   </ENTRY>

   <REPEAT COUNT="2">
      <ENTRY>
     <REF HREF="mms://example.microsoft.com/clip2.asf" />
     <REF HREF="mms://example.microsoft.com/clip3.asf" />
 <!-- These clips play twice. -->
      </ENTRY>
   </REPEAT>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="f9211-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9211-122">Requirements</span></span>



| <span data-ttu-id="f9211-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9211-123">Requirement</span></span> | <span data-ttu-id="f9211-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f9211-124">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="f9211-125">Versione</span><span class="sxs-lookup"><span data-stu-id="f9211-125">Version</span></span><br/> | <span data-ttu-id="f9211-126">Windows Media Player versione 70 o successiva</span><span class="sxs-lookup"><span data-stu-id="f9211-126">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9211-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9211-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9211-128">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f9211-128">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="f9211-129">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f9211-129">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





