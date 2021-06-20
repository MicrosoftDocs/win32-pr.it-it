---
description: Informazioni sull'elemento ParameterInit, che definisce un valore per un'istanza di un elemento ParameterDef.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e211fcad2c53824c7786850a7fc78c6825c219a7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407264"
---
# <a name="parameterinit"></a><span data-ttu-id="4176a-103">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="4176a-103">ParameterInit</span></span>

<span data-ttu-id="4176a-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="4176a-104">This topic is not current.</span></span> <span data-ttu-id="4176a-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4176a-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4176a-106">Definisce un valore per un'istanza di un elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="4176a-106">Defines a value for an instance of a ParameterDef element.</span></span> <span data-ttu-id="4176a-107">Un elemento ParameterInit è la destinazione del riferimento effettuato da un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="4176a-107">A ParameterInit element is the target of the reference made by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="4176a-108">Element Tag</span><span class="sxs-lookup"><span data-stu-id="4176a-108">Element Tag</span></span>

<ParameterInit>

## <a name="xml-attributes"></a><span data-ttu-id="4176a-109">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="4176a-109">XML Attributes</span></span>

<span data-ttu-id="4176a-110">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="4176a-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="4176a-111">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="4176a-111">XML Attribute</span></span>   | <span data-ttu-id="4176a-112">Dettagli</span><span class="sxs-lookup"><span data-stu-id="4176a-112">Details</span></span>                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4176a-113">name</span><span class="sxs-lookup"><span data-stu-id="4176a-113">name</span></span><br/> | <span data-ttu-id="4176a-114">Contiene l'attributo name dell'elemento ParameterDef che deve essere inizializzato nel contesto del documento corrente.</span><span class="sxs-lookup"><span data-stu-id="4176a-114">Holds the name attribute of the ParameterDef element that is to be initialized within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="4176a-115">Per altre informazioni, vedere la [sezione Attributi](xml-attributes.md) XML.</span><span class="sxs-lookup"><span data-stu-id="4176a-115">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="4176a-116">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4176a-116">Element Information</span></span>

<span data-ttu-id="4176a-117">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="4176a-117">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="4176a-118">Categoria</span><span class="sxs-lookup"><span data-stu-id="4176a-118">Category</span></span>                   |                                                                                                   |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4176a-119">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="4176a-119">Parent elements</span></span><br/> | <span data-ttu-id="4176a-120">PrintTicket (radice PrintTicket)</span><span class="sxs-lookup"><span data-stu-id="4176a-120">PrintTicket (PrintTicket root)</span></span><br/>                                                         |
| <span data-ttu-id="4176a-121">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="4176a-121">Child elements</span></span><br/>  | <span data-ttu-id="4176a-122">Valore (uno)</span><span class="sxs-lookup"><span data-stu-id="4176a-122">Value (one)</span></span><br/>                                                                            |
| <span data-ttu-id="4176a-123">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="4176a-123">This element</span></span><br/>    | <span data-ttu-id="4176a-124">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="4176a-124">No character data is permitted.</span></span><br/> <span data-ttu-id="4176a-125">Gli elementi di pari livello figlio duplicati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="4176a-125">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="4176a-126">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="4176a-126">Configuration Dependencies</span></span>

<span data-ttu-id="4176a-127">nessuno</span><span class="sxs-lookup"><span data-stu-id="4176a-127">None</span></span>

## <a name="example"></a><span data-ttu-id="4176a-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="4176a-128">Example</span></span>

<span data-ttu-id="4176a-129">Nell'esempio seguente viene inizializzato un parametro su 1.</span><span class="sxs-lookup"><span data-stu-id="4176a-129">The following example initializes a parameter to 1.</span></span> <span data-ttu-id="4176a-130">L'esempio in [ParameterDef](parameterdef.md) illustra come impostare tutti gli elementi Property necessari per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="4176a-130">The example in [ParameterDef](parameterdef.md) demonstrates how to set all of the required Property elements for this parameter.</span></span>

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a><span data-ttu-id="4176a-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4176a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4176a-132">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="4176a-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




