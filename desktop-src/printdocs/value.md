---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Valore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a8f8c5bf9e2ec1696d6282b859fc99b7701159
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320880"
---
# <a name="value"></a><span data-ttu-id="da06d-104">Valore</span><span class="sxs-lookup"><span data-stu-id="da06d-104">Value</span></span>

<span data-ttu-id="da06d-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="da06d-105">This topic is not current.</span></span> <span data-ttu-id="da06d-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="da06d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="da06d-107">Un elemento Value associa un valore letterale a un tipo.</span><span class="sxs-lookup"><span data-stu-id="da06d-107">A Value element associates a literal with a type.</span></span>

## <a name="element-tag"></a><span data-ttu-id="da06d-108">Tag elemento</span><span class="sxs-lookup"><span data-stu-id="da06d-108">Element Tag</span></span>

<Value>

## <a name="xml-attributes"></a><span data-ttu-id="da06d-109">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="da06d-109">XML Attributes</span></span>

<span data-ttu-id="da06d-110">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="da06d-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="da06d-111">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="da06d-111">XML Attribute</span></span>       | <span data-ttu-id="da06d-112">Dettagli</span><span class="sxs-lookup"><span data-stu-id="da06d-112">Details</span></span>                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da06d-113">xsi:type</span><span class="sxs-lookup"><span data-stu-id="da06d-113">xsi:type</span></span><br/> | <span data-ttu-id="da06d-114">Specifica il tipo di dati di value, che deve essere uno dei seguenti tipi definiti da XSD: String, Integer, Decimal, QName.</span><span class="sxs-lookup"><span data-stu-id="da06d-114">Specifies the data type of Value, which must be one of the following XSD-defined types: string, integer, decimal, QName.</span></span> <span data-ttu-id="da06d-115">Se mancante, il tipo di dati predefinito è String.</span><span class="sxs-lookup"><span data-stu-id="da06d-115">If missing, the default data type is string.</span></span><br/> |



 

<span data-ttu-id="da06d-116">Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="da06d-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="da06d-117">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="da06d-117">Element Information</span></span>

<span data-ttu-id="da06d-118">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="da06d-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="da06d-119">Category</span><span class="sxs-lookup"><span data-stu-id="da06d-119">Category</span></span>                   | <span data-ttu-id="da06d-120">Dettagli</span><span class="sxs-lookup"><span data-stu-id="da06d-120">Details</span></span>                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da06d-121">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="da06d-121">Parent elements</span></span><br/> | <span data-ttu-id="da06d-122">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="da06d-122">ParameterInit</span></span> <br/> <span data-ttu-id="da06d-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="da06d-123">Property</span></span><br/> <span data-ttu-id="da06d-124">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="da06d-124">ScoredProperty</span></span><br/>                                                                                   |
| <span data-ttu-id="da06d-125">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="da06d-125">Child elements</span></span><br/>  | <span data-ttu-id="da06d-126">È consentito solo il contenuto di tipo carattere o Integer.</span><span class="sxs-lookup"><span data-stu-id="da06d-126">Only character or integer content is permitted.</span></span><br/>                                                                                                |
| <span data-ttu-id="da06d-127">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="da06d-127">This element</span></span><br/>    | <span data-ttu-id="da06d-128">Contenuto null consentito.</span><span class="sxs-lookup"><span data-stu-id="da06d-128">Null content is allowed.</span></span> <span data-ttu-id="da06d-129">Il contenuto carattere deve essere conforme alla sintassi definita dal tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="da06d-129">Character content must conform to syntax defined by data type.</span></span><br/> <span data-ttu-id="da06d-130">Gli elementi di pari livello figlio duplicati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="da06d-130">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="da06d-131">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="da06d-131">Configuration Dependencies</span></span>

<span data-ttu-id="da06d-132">Gli elementi valore visualizzati all'interno dell'elemento ScoredProperty non possono avere dipendenze di configurazione.</span><span class="sxs-lookup"><span data-stu-id="da06d-132">Value elements that appear within ScoredProperty element may not have any configuration dependencies.</span></span> <span data-ttu-id="da06d-133">Gli elementi valore visualizzati negli elementi Property possono avere dipendenze arbitrarie dalla configurazione.</span><span class="sxs-lookup"><span data-stu-id="da06d-133">Value elements that appear within Property elements may have arbitrary dependencies on the configuration.</span></span>

## <a name="element-usage"></a><span data-ttu-id="da06d-134">Utilizzo elementi</span><span class="sxs-lookup"><span data-stu-id="da06d-134">Element Usage</span></span>

<span data-ttu-id="da06d-135">Un elemento Value può essere visualizzato all'interno di una proprietà o di un elemento ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="da06d-135">A Value element may appear within a Property or ScoredProperty element.</span></span> <span data-ttu-id="da06d-136">Lo scopo dell'elemento value è rappresentare un valore come tipo di dati XML standard.</span><span class="sxs-lookup"><span data-stu-id="da06d-136">The purpose of the Value element is to represent a value as a standard XML data type.</span></span> <span data-ttu-id="da06d-137">Il tipo di dati viene specificato come attributo XML dell'elemento value, xsi: Type.</span><span class="sxs-lookup"><span data-stu-id="da06d-137">The data type is specified as an XML attribute of the Value element, xsi:type.</span></span> <span data-ttu-id="da06d-138">Si noti che non tutti i tipi definiti da XSD o XML sono supportati.</span><span class="sxs-lookup"><span data-stu-id="da06d-138">Note that not all XSD-defined or XML-defined types are supported.</span></span> <span data-ttu-id="da06d-139">Per un elenco dei tipi supportati, vedere [Riepilogo dei tipi di elemento](summary-of-element-types.md).</span><span class="sxs-lookup"><span data-stu-id="da06d-139">For a list of supported types, see [Summary of Element Types](summary-of-element-types.md).</span></span> <span data-ttu-id="da06d-140">Un elemento Value può contenere solo contenuto di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="da06d-140">A Value element can contain only character content.</span></span> <span data-ttu-id="da06d-141">Nessun altro elemento può apparire come contenuto in un elemento value.</span><span class="sxs-lookup"><span data-stu-id="da06d-141">Nothing else may appear as content in a Value element.</span></span>

> [!Note]  
> <span data-ttu-id="da06d-142">Alcuni elementi Property definito dallo schema di stampa e ScoredProperty non contengono un elemento value, perché il loro scopo è semplicemente quello di essere elementi padre delle sottoproprietà.</span><span class="sxs-lookup"><span data-stu-id="da06d-142">Some Print Schema-defined Property and ScoredProperty elements do not contain a Value element, because their purpose is simply to be parents of subproperties.</span></span> <span data-ttu-id="da06d-143">Non è necessario aggiungere un elemento value a tali proprietà, ovvero proprietà che non contengono un elemento value.</span><span class="sxs-lookup"><span data-stu-id="da06d-143">You should not add a Value element to such properties as these, properties that do not contain a Value element.</span></span>

 

<span data-ttu-id="da06d-144">Per essere conforme a Print Schema Framework, che richiede un elemento value o sottoelementi presenti negli elementi che supportano valori, un valore assente o non definito deve essere rappresentato presentando l'elemento value come elemento vuoto. ovvero come</span><span class="sxs-lookup"><span data-stu-id="da06d-144">To conform to the Print Schema Framework, which requires either a Value element or subelements be present in the elements that support values, an absent or undefined value should be represented by presenting the Value element as an empty element; that is, as</span></span> <Value></Value><span data-ttu-id="da06d-145">.</span><span class="sxs-lookup"><span data-stu-id="da06d-145">.</span></span>

## <a name="example"></a><span data-ttu-id="da06d-146">Esempio</span><span class="sxs-lookup"><span data-stu-id="da06d-146">Example</span></span>

<span data-ttu-id="da06d-147">Definire un valore di tipo Decimal e inizializzarlo su "128,5".</span><span class="sxs-lookup"><span data-stu-id="da06d-147">Define a Value of type decimal and initialize it to "128.5".</span></span>

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a><span data-ttu-id="da06d-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="da06d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da06d-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="da06d-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




