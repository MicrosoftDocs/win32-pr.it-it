---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1605d173e0ab311841a6fcc37a46a0ba3b59b005
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321038"
---
# <a name="scoredproperty"></a><span data-ttu-id="65be6-104">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="65be6-104">ScoredProperty</span></span>

<span data-ttu-id="65be6-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="65be6-105">This topic is not current.</span></span> <span data-ttu-id="65be6-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="65be6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="65be6-107">Un elemento ScoredProperty dichiara una proprietà intrinseca a una definizione di opzione.</span><span class="sxs-lookup"><span data-stu-id="65be6-107">A ScoredProperty element declares a property that is intrinsic to an Option definition.</span></span> <span data-ttu-id="65be6-108">È necessario confrontare tali proprietà quando si valuta il modo in cui un'opzione richiesta corrisponde a un'opzione supportata dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="65be6-108">Such properties should be compared when evaluating how closely a requested Option matches a device-supported Option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="65be6-109">Tag elemento</span><span class="sxs-lookup"><span data-stu-id="65be6-109">Element Tag</span></span>

<ScoredProperty>

## <a name="xml-attributes"></a><span data-ttu-id="65be6-110">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="65be6-110">XML Attributes</span></span>

<span data-ttu-id="65be6-111">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="65be6-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="65be6-112">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="65be6-112">XML Attribute</span></span>   | <span data-ttu-id="65be6-113">Dettagli</span><span class="sxs-lookup"><span data-stu-id="65be6-113">Details</span></span>                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65be6-114">name</span><span class="sxs-lookup"><span data-stu-id="65be6-114">name</span></span><br/> | <span data-ttu-id="65be6-115">Include l'attributo Name di ScoredProperty, ovvero una proprietà standard o una proprietà definita privatamente.</span><span class="sxs-lookup"><span data-stu-id="65be6-115">Holds the name attribute of the ScoredProperty, either a standard property or a privately-defined property.</span></span> <br/> |



 

<span data-ttu-id="65be6-116">Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="65be6-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="65be6-117">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="65be6-117">Element Information</span></span>

<span data-ttu-id="65be6-118">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="65be6-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="65be6-119">Category</span><span class="sxs-lookup"><span data-stu-id="65be6-119">Category</span></span>                   | <span data-ttu-id="65be6-120">Dettagli</span><span class="sxs-lookup"><span data-stu-id="65be6-120">Details</span></span>                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65be6-121">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="65be6-121">Parent elements</span></span><br/> | <span data-ttu-id="65be6-122">*Opzione*</span><span class="sxs-lookup"><span data-stu-id="65be6-122">*Option*</span></span><br/> <span data-ttu-id="65be6-123">*ScoredProperty*</span><span class="sxs-lookup"><span data-stu-id="65be6-123">*ScoredProperty*</span></span><br/>                                                                                                                          |
| <span data-ttu-id="65be6-124">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="65be6-124">Child elements</span></span><br/>  | <span data-ttu-id="65be6-125">Prima o dopo</span><span class="sxs-lookup"><span data-stu-id="65be6-125">Either</span></span><br/> <span data-ttu-id="65be6-126">*ParameterRef* (uno)</span><span class="sxs-lookup"><span data-stu-id="65be6-126">*ParameterRef* (one)</span></span><br/> <span data-ttu-id="65be6-127">oppure</span><span class="sxs-lookup"><span data-stu-id="65be6-127">or</span></span><br/> <span data-ttu-id="65be6-128">*Valore* (uno)</span><span class="sxs-lookup"><span data-stu-id="65be6-128">*Value* (one)</span></span><br/> <span data-ttu-id="65be6-129">*Property* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="65be6-129">*Property* (zero or more)</span></span><br/> <span data-ttu-id="65be6-130">*ScoredProperty* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="65be6-130">*ScoredProperty* (zero or more)</span></span><br/> |
| <span data-ttu-id="65be6-131">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="65be6-131">This element</span></span><br/>    | <span data-ttu-id="65be6-132">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="65be6-132">No character data is permitted.</span></span><br/> <span data-ttu-id="65be6-133">Gli elementi di pari livello figlio duplicati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="65be6-133">Duplicate child siblings are not permitted.</span></span><br/>                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="65be6-134">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="65be6-134">Configuration Dependencies</span></span>

<span data-ttu-id="65be6-135">Un elemento ScoredProperty non può avere dipendenze di configurazione.</span><span class="sxs-lookup"><span data-stu-id="65be6-135">A ScoredProperty element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="65be6-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="65be6-136">Example</span></span>

<span data-ttu-id="65be6-137">Dichiarare un elemento ScoredProperty denominato MediaSizeWidth con un valore pari a 11.</span><span class="sxs-lookup"><span data-stu-id="65be6-137">Declare a ScoredProperty element named MediaSizeWidth with a Value of 11.</span></span>

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a><span data-ttu-id="65be6-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65be6-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65be6-139">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="65be6-139">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




