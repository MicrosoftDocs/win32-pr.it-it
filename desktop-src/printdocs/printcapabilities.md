---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c6dd8ce98b071f1eb239762544a9b72160035
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321064"
---
# <a name="printcapabilities"></a><span data-ttu-id="b6722-104">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="b6722-104">PrintCapabilities</span></span>

<span data-ttu-id="b6722-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="b6722-105">This topic is not current.</span></span> <span data-ttu-id="b6722-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b6722-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b6722-107">Un elemento PrintCapabilities rappresenta la radice del documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b6722-107">A PrintCapabilities element represents the root of the PrintCapabilities document.</span></span> <span data-ttu-id="b6722-108">Il documento PrintCapabilities contiene tutte le informazioni necessarie per descrivere gli attributi del dispositivo supportati, in base a una particolare configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6722-108">The PrintCapabilities document contains all of the information needed to describe the supported device attributes, given a particular device configuration.</span></span>

## <a name="element-tag"></a><span data-ttu-id="b6722-109">Tag elemento</span><span class="sxs-lookup"><span data-stu-id="b6722-109">Element Tag</span></span>

<PrintCapabilities>

## <a name="xml-attributes"></a><span data-ttu-id="b6722-110">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="b6722-110">XML Attributes</span></span>

<span data-ttu-id="b6722-111">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="b6722-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="b6722-112">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="b6722-112">XML Attribute</span></span>      | <span data-ttu-id="b6722-113">Dettagli</span><span class="sxs-lookup"><span data-stu-id="b6722-113">Details</span></span>                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6722-114">version</span><span class="sxs-lookup"><span data-stu-id="b6722-114">version</span></span><br/> | <span data-ttu-id="b6722-115">Specifica la versione dello schema che definisce i tipi di elemento e la relativa struttura.</span><span class="sxs-lookup"><span data-stu-id="b6722-115">Specifies the version of the schema that defines element types and their structure.</span></span> <span data-ttu-id="b6722-116">L'attributo Version è di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="b6722-116">The version attribute is of type integer.</span></span> <span data-ttu-id="b6722-117">La versione dello schema corrente è "1".</span><span class="sxs-lookup"><span data-stu-id="b6722-117">The current schema version is designated "1".</span></span> <span data-ttu-id="b6722-118">Questo attributo è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b6722-118">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="b6722-119">Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="b6722-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="b6722-120">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b6722-120">Element Information</span></span>

<span data-ttu-id="b6722-121">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="b6722-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="b6722-122">Category</span><span class="sxs-lookup"><span data-stu-id="b6722-122">Category</span></span>                   | <span data-ttu-id="b6722-123">Dettagli</span><span class="sxs-lookup"><span data-stu-id="b6722-123">Details</span></span>                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6722-124">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b6722-124">Parent elements</span></span><br/> | <span data-ttu-id="b6722-125">Solo radice del documento.</span><span class="sxs-lookup"><span data-stu-id="b6722-125">Document root only.</span></span><br/>                                                                                    |
| <span data-ttu-id="b6722-126">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b6722-126">Child elements</span></span><br/>  | <span data-ttu-id="b6722-127">*Funzionalità* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="b6722-127">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="b6722-128">*ParameterDef* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="b6722-128">*ParameterDef* (zero or more)</span></span><br/> <span data-ttu-id="b6722-129">*Property* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="b6722-129">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="b6722-130">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="b6722-130">This element</span></span><br/>    | <span data-ttu-id="b6722-131">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="b6722-131">No character data is permitted.</span></span><br/> <span data-ttu-id="b6722-132">Gli elementi di pari livello figlio duplicati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="b6722-132">Duplicate child siblings are not permitted.</span></span><br/>                 |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="b6722-133">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="b6722-133">Configuration Dependencies</span></span>

<span data-ttu-id="b6722-134">L'elemento radice non può avere dipendenze di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b6722-134">The root element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="b6722-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="b6722-135">Example</span></span>

<span data-ttu-id="b6722-136">Vedere [esempio di documento PrintCapabilities](printcapabilities-document-example.md).</span><span class="sxs-lookup"><span data-stu-id="b6722-136">See [PrintCapabilities Document Example](printcapabilities-document-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6722-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b6722-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6722-138">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b6722-138">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




