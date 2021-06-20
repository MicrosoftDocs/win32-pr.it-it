---
description: Informazioni sull'elemento ParameterRef, che definisce un riferimento a un elemento ParameterInit e sul suo funzionamento con ScoredProperty.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff3b0e16f53e8399a5bbbb5974a05fd6886cdd2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407184"
---
# <a name="parameterref"></a><span data-ttu-id="ee8d5-103">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="ee8d5-103">ParameterRef</span></span>

<span data-ttu-id="ee8d5-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="ee8d5-104">This topic is not current.</span></span> <span data-ttu-id="ee8d5-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ee8d5-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ee8d5-106">Un elemento ParameterRef definisce un riferimento a un elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="ee8d5-106">A ParameterRef element defines a reference to a ParameterInit element.</span></span> <span data-ttu-id="ee8d5-107">Un elemento ScoredProperty che contiene un elemento ParameterRef non ha un elemento Value impostato in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="ee8d5-107">A ScoredProperty element that contains a ParameterRef element does not have an explicitly-set Value element.</span></span> <span data-ttu-id="ee8d5-108">L'elemento ScoredProperty riceve invece il valore dall'elemento ParameterInit a cui fa riferimento un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="ee8d5-108">Instead, the ScoredProperty element receives its value from the ParameterInit element referenced by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="ee8d5-109">Element Tag</span><span class="sxs-lookup"><span data-stu-id="ee8d5-109">Element Tag</span></span>

<ParameterRef>

## <a name="xml-attributes"></a><span data-ttu-id="ee8d5-110">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="ee8d5-110">XML Attributes</span></span>

<span data-ttu-id="ee8d5-111">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="ee8d5-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="ee8d5-112">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="ee8d5-112">XML Attribute</span></span>   | <span data-ttu-id="ee8d5-113">Dettagli</span><span class="sxs-lookup"><span data-stu-id="ee8d5-113">Details</span></span>                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8d5-114">name</span><span class="sxs-lookup"><span data-stu-id="ee8d5-114">name</span></span><br/> | <span data-ttu-id="ee8d5-115">Contiene l'attributo name dell'elemento ParameterDef a cui viene fatto riferimento nel contesto del documento corrente.</span><span class="sxs-lookup"><span data-stu-id="ee8d5-115">Holds the name attribute of the ParameterDef element that is referenced within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="ee8d5-116">Per altre informazioni, vedere la [sezione Attributi](xml-attributes.md) XML.</span><span class="sxs-lookup"><span data-stu-id="ee8d5-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="ee8d5-117">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ee8d5-117">Element Information</span></span>

<span data-ttu-id="ee8d5-118">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="ee8d5-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="ee8d5-119">Categoria</span><span class="sxs-lookup"><span data-stu-id="ee8d5-119">Category</span></span>                   | <span data-ttu-id="ee8d5-120">Dettagli</span><span class="sxs-lookup"><span data-stu-id="ee8d5-120">Details</span></span>                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8d5-121">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="ee8d5-121">Parent elements</span></span><br/> | <span data-ttu-id="ee8d5-122">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="ee8d5-122">ScoredProperty</span></span> <br/>                                                                        |
| <span data-ttu-id="ee8d5-123">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ee8d5-123">Child elements</span></span><br/>  | <span data-ttu-id="ee8d5-124">Non consentito.</span><span class="sxs-lookup"><span data-stu-id="ee8d5-124">None permitted.</span></span><br/>                                                                        |
| <span data-ttu-id="ee8d5-125">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="ee8d5-125">This element</span></span><br/>    | <span data-ttu-id="ee8d5-126">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="ee8d5-126">No character data is permitted.</span></span><br/> <span data-ttu-id="ee8d5-127">Gli elementi di pari livello figlio duplicati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="ee8d5-127">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="ee8d5-128">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="ee8d5-128">Configuration Dependencies</span></span>

<span data-ttu-id="ee8d5-129">Gli elementi ParameterRef potrebbero non avere dipendenze di configurazione.</span><span class="sxs-lookup"><span data-stu-id="ee8d5-129">ParameterRef elements may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="ee8d5-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="ee8d5-130">Example</span></span>

<span data-ttu-id="ee8d5-131">L'esempio seguente illustra come usare gli elementi ParameterRef per consentire agli utenti di immettere parametri personalizzati per le dimensioni dei supporti.</span><span class="sxs-lookup"><span data-stu-id="ee8d5-131">The following example illustrates how to use ParameterRef elements to enable users to enter custom media size parameters.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ee8d5-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee8d5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee8d5-133">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ee8d5-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




