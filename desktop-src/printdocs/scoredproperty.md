---
description: Trovare informazioni sull'elemento ScoredProperty. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb93fbdaeb6101cbd1ff75d6c0b3a829afe0d317
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119116"
---
# <a name="scoredproperty"></a><span data-ttu-id="f44e9-105">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="f44e9-105">ScoredProperty</span></span>

<span data-ttu-id="f44e9-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="f44e9-106">This topic is not current.</span></span> <span data-ttu-id="f44e9-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f44e9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f44e9-108">Un elemento ScoredProperty dichiara una proprietà intrinseca a una definizione option.</span><span class="sxs-lookup"><span data-stu-id="f44e9-108">A ScoredProperty element declares a property that is intrinsic to an Option definition.</span></span> <span data-ttu-id="f44e9-109">Tali proprietà devono essere confrontate quando si valuta quanto un'opzione richiesta corrisponde a un'opzione supportata dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f44e9-109">Such properties should be compared when evaluating how closely a requested Option matches a device-supported Option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="f44e9-110">Element Tag</span><span class="sxs-lookup"><span data-stu-id="f44e9-110">Element Tag</span></span>

<ScoredProperty>

## <a name="xml-attributes"></a><span data-ttu-id="f44e9-111">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="f44e9-111">XML Attributes</span></span>

<span data-ttu-id="f44e9-112">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="f44e9-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="f44e9-113">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="f44e9-113">XML Attribute</span></span>   | <span data-ttu-id="f44e9-114">Dettagli</span><span class="sxs-lookup"><span data-stu-id="f44e9-114">Details</span></span>                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f44e9-115">name</span><span class="sxs-lookup"><span data-stu-id="f44e9-115">name</span></span><br/> | <span data-ttu-id="f44e9-116">Contiene l'attributo name di ScoredProperty, una proprietà standard o una proprietà definita privatamente.</span><span class="sxs-lookup"><span data-stu-id="f44e9-116">Holds the name attribute of the ScoredProperty, either a standard property or a privately-defined property.</span></span> <br/> |



 

<span data-ttu-id="f44e9-117">Per altre informazioni, vedere la [sezione Attributi](xml-attributes.md) XML.</span><span class="sxs-lookup"><span data-stu-id="f44e9-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="f44e9-118">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f44e9-118">Element Information</span></span>

<span data-ttu-id="f44e9-119">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere figli di questo elemento ed eventuali restrizioni sull'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="f44e9-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="f44e9-120">Categoria</span><span class="sxs-lookup"><span data-stu-id="f44e9-120">Category</span></span>                   | <span data-ttu-id="f44e9-121">Dettagli</span><span class="sxs-lookup"><span data-stu-id="f44e9-121">Details</span></span>                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f44e9-122">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f44e9-122">Parent elements</span></span><br/> | <span data-ttu-id="f44e9-123">*Opzione*</span><span class="sxs-lookup"><span data-stu-id="f44e9-123">*Option*</span></span><br/> <span data-ttu-id="f44e9-124">*ScoredProperty*</span><span class="sxs-lookup"><span data-stu-id="f44e9-124">*ScoredProperty*</span></span><br/>                                                                                                                          |
| <span data-ttu-id="f44e9-125">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f44e9-125">Child elements</span></span><br/>  | <span data-ttu-id="f44e9-126">Prima o dopo</span><span class="sxs-lookup"><span data-stu-id="f44e9-126">Either</span></span><br/> <span data-ttu-id="f44e9-127">*ParameterRef* (uno)</span><span class="sxs-lookup"><span data-stu-id="f44e9-127">*ParameterRef* (one)</span></span><br/> <span data-ttu-id="f44e9-128">oppure</span><span class="sxs-lookup"><span data-stu-id="f44e9-128">or</span></span><br/> <span data-ttu-id="f44e9-129">*Valore* (uno)</span><span class="sxs-lookup"><span data-stu-id="f44e9-129">*Value* (one)</span></span><br/> <span data-ttu-id="f44e9-130">*Proprietà* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="f44e9-130">*Property* (zero or more)</span></span><br/> <span data-ttu-id="f44e9-131">*ScoredProperty* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="f44e9-131">*ScoredProperty* (zero or more)</span></span><br/> |
| <span data-ttu-id="f44e9-132">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="f44e9-132">This element</span></span><br/>    | <span data-ttu-id="f44e9-133">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="f44e9-133">No character data is permitted.</span></span><br/> <span data-ttu-id="f44e9-134">Gli elementi di pari livello figlio duplicati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="f44e9-134">Duplicate child siblings are not permitted.</span></span><br/>                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="f44e9-135">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="f44e9-135">Configuration Dependencies</span></span>

<span data-ttu-id="f44e9-136">Un elemento ScoredProperty potrebbe non avere dipendenze di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f44e9-136">A ScoredProperty element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="f44e9-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="f44e9-137">Example</span></span>

<span data-ttu-id="f44e9-138">Dichiarare un elemento ScoredProperty denominato MediaSizeWidth con valore 11.</span><span class="sxs-lookup"><span data-stu-id="f44e9-138">Declare a ScoredProperty element named MediaSizeWidth with a Value of 11.</span></span>

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a><span data-ttu-id="f44e9-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f44e9-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f44e9-140">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f44e9-140">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




