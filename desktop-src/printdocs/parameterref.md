---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2ef6655439718c1038afe2d342910c54db45ba
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320961"
---
# <a name="parameterref"></a><span data-ttu-id="976f7-104">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="976f7-104">ParameterRef</span></span>

<span data-ttu-id="976f7-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="976f7-105">This topic is not current.</span></span> <span data-ttu-id="976f7-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="976f7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="976f7-107">Un elemento ParameterRef definisce un riferimento a un elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="976f7-107">A ParameterRef element defines a reference to a ParameterInit element.</span></span> <span data-ttu-id="976f7-108">Un elemento ScoredProperty che contiene un elemento ParameterRef non dispone di un elemento value impostato in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="976f7-108">A ScoredProperty element that contains a ParameterRef element does not have an explicitly-set Value element.</span></span> <span data-ttu-id="976f7-109">L'elemento ScoredProperty riceve invece il valore dall'elemento ParameterInit a cui fa riferimento un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="976f7-109">Instead, the ScoredProperty element receives its value from the ParameterInit element referenced by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="976f7-110">Tag elemento</span><span class="sxs-lookup"><span data-stu-id="976f7-110">Element Tag</span></span>

<ParameterRef>

## <a name="xml-attributes"></a><span data-ttu-id="976f7-111">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="976f7-111">XML Attributes</span></span>

<span data-ttu-id="976f7-112">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="976f7-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="976f7-113">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="976f7-113">XML Attribute</span></span>   | <span data-ttu-id="976f7-114">Dettagli</span><span class="sxs-lookup"><span data-stu-id="976f7-114">Details</span></span>                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="976f7-115">name</span><span class="sxs-lookup"><span data-stu-id="976f7-115">name</span></span><br/> | <span data-ttu-id="976f7-116">Include l'attributo Name dell'elemento ParameterDef a cui si fa riferimento nel contesto del documento corrente.</span><span class="sxs-lookup"><span data-stu-id="976f7-116">Holds the name attribute of the ParameterDef element that is referenced within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="976f7-117">Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="976f7-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="976f7-118">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="976f7-118">Element Information</span></span>

<span data-ttu-id="976f7-119">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="976f7-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="976f7-120">Category</span><span class="sxs-lookup"><span data-stu-id="976f7-120">Category</span></span>                   | <span data-ttu-id="976f7-121">Dettagli</span><span class="sxs-lookup"><span data-stu-id="976f7-121">Details</span></span>                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="976f7-122">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="976f7-122">Parent elements</span></span><br/> | <span data-ttu-id="976f7-123">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="976f7-123">ScoredProperty</span></span> <br/>                                                                        |
| <span data-ttu-id="976f7-124">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="976f7-124">Child elements</span></span><br/>  | <span data-ttu-id="976f7-125">Nessuno consentito.</span><span class="sxs-lookup"><span data-stu-id="976f7-125">None permitted.</span></span><br/>                                                                        |
| <span data-ttu-id="976f7-126">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="976f7-126">This element</span></span><br/>    | <span data-ttu-id="976f7-127">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="976f7-127">No character data is permitted.</span></span><br/> <span data-ttu-id="976f7-128">Gli elementi di pari livello figlio duplicati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="976f7-128">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="976f7-129">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="976f7-129">Configuration Dependencies</span></span>

<span data-ttu-id="976f7-130">Gli elementi ParameterRef non possono avere dipendenze di configurazione.</span><span class="sxs-lookup"><span data-stu-id="976f7-130">ParameterRef elements may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="976f7-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="976f7-131">Example</span></span>

<span data-ttu-id="976f7-132">Nell'esempio seguente viene illustrato come utilizzare gli elementi ParameterRef per consentire agli utenti di immettere parametri di dimensioni multimediali personalizzate.</span><span class="sxs-lookup"><span data-stu-id="976f7-132">The following example illustrates how to use ParameterRef elements to enable users to enter custom media size parameters.</span></span>

``` syntax
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
  <psf:Property name="psk:DisplayName">
    <psf:Value xsi:type="xs:string">Fabrikam User Custom</psf:Value>
  </psf:Property>
</psf:Option>
```

## <a name="related-topics"></a><span data-ttu-id="976f7-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="976f7-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="976f7-134">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="976f7-134">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




