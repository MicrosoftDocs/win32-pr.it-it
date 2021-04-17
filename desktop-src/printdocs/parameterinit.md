---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cb985e746b400b1c804f21b5996352ae590e3b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234565"
---
# <a name="parameterinit"></a><span data-ttu-id="32500-104">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="32500-104">ParameterInit</span></span>

<span data-ttu-id="32500-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="32500-105">This topic is not current.</span></span> <span data-ttu-id="32500-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="32500-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="32500-107">Definisce un valore per un'istanza di un elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="32500-107">Defines a value for an instance of a ParameterDef element.</span></span> <span data-ttu-id="32500-108">Un elemento ParameterInit è la destinazione del riferimento eseguito da un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="32500-108">A ParameterInit element is the target of the reference made by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="32500-109">Tag elemento</span><span class="sxs-lookup"><span data-stu-id="32500-109">Element Tag</span></span>

<ParameterInit>

## <a name="xml-attributes"></a><span data-ttu-id="32500-110">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="32500-110">XML Attributes</span></span>

<span data-ttu-id="32500-111">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="32500-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="32500-112">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="32500-112">XML Attribute</span></span>   | <span data-ttu-id="32500-113">Dettagli</span><span class="sxs-lookup"><span data-stu-id="32500-113">Details</span></span>                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32500-114">name</span><span class="sxs-lookup"><span data-stu-id="32500-114">name</span></span><br/> | <span data-ttu-id="32500-115">Include l'attributo Name dell'elemento ParameterDef che deve essere inizializzato nel contesto del documento corrente.</span><span class="sxs-lookup"><span data-stu-id="32500-115">Holds the name attribute of the ParameterDef element that is to be initialized within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="32500-116">Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="32500-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="32500-117">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="32500-117">Element Information</span></span>

<span data-ttu-id="32500-118">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="32500-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="32500-119">Category</span><span class="sxs-lookup"><span data-stu-id="32500-119">Category</span></span>                   |                                                                                                   |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32500-120">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="32500-120">Parent elements</span></span><br/> | <span data-ttu-id="32500-121">PrintTicket (radice PrintTicket)</span><span class="sxs-lookup"><span data-stu-id="32500-121">PrintTicket (PrintTicket root)</span></span><br/>                                                         |
| <span data-ttu-id="32500-122">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="32500-122">Child elements</span></span><br/>  | <span data-ttu-id="32500-123">Valore (uno)</span><span class="sxs-lookup"><span data-stu-id="32500-123">Value (one)</span></span><br/>                                                                            |
| <span data-ttu-id="32500-124">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="32500-124">This element</span></span><br/>    | <span data-ttu-id="32500-125">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="32500-125">No character data is permitted.</span></span><br/> <span data-ttu-id="32500-126">Gli elementi di pari livello figlio duplicati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="32500-126">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="32500-127">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="32500-127">Configuration Dependencies</span></span>

<span data-ttu-id="32500-128">nessuno</span><span class="sxs-lookup"><span data-stu-id="32500-128">None</span></span>

## <a name="example"></a><span data-ttu-id="32500-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="32500-129">Example</span></span>

<span data-ttu-id="32500-130">Nell'esempio seguente viene inizializzato un parametro su 1.</span><span class="sxs-lookup"><span data-stu-id="32500-130">The following example initializes a parameter to 1.</span></span> <span data-ttu-id="32500-131">Nell'esempio in [ParameterDef](parameterdef.md) viene illustrato come impostare tutti gli elementi della proprietà necessari per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="32500-131">The example in [ParameterDef](parameterdef.md) demonstrates how to set all of the required Property elements for this parameter.</span></span>

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a><span data-ttu-id="32500-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="32500-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32500-133">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="32500-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




