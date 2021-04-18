---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d2e225eb38584e290db55c33594be80d0d7999
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321062"
---
# <a name="printticket"></a><span data-ttu-id="d3fe0-104">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="d3fe0-104">PrintTicket</span></span>

<span data-ttu-id="d3fe0-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-105">This topic is not current.</span></span> <span data-ttu-id="d3fe0-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d3fe0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d3fe0-107">Un elemento PrintTicket è l'elemento radice del documento PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-107">A PrintTicket element is the root element of the PrintTicket document.</span></span> <span data-ttu-id="d3fe0-108">Un elemento PrintTicket contiene tutte le informazioni di formattazione del processo necessarie per l'output di un processo.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-108">A PrintTicket element contains all job formatting information required to output a job.</span></span>

## <a name="element-tag"></a><span data-ttu-id="d3fe0-109">Tag elemento</span><span class="sxs-lookup"><span data-stu-id="d3fe0-109">Element Tag</span></span>

<PrintTicket>

## <a name="xml-attributes"></a><span data-ttu-id="d3fe0-110">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="d3fe0-110">XML Attributes</span></span>

<span data-ttu-id="d3fe0-111">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="d3fe0-112">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="d3fe0-112">XML Attribute</span></span>      | <span data-ttu-id="d3fe0-113">Dettagli</span><span class="sxs-lookup"><span data-stu-id="d3fe0-113">Details</span></span>                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3fe0-114">version</span><span class="sxs-lookup"><span data-stu-id="d3fe0-114">version</span></span><br/> | <span data-ttu-id="d3fe0-115">Specifica la versione dello schema che definisce i tipi di elemento e la relativa struttura, un valore letterale di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-115">Specifies the version of the schema that defines element types and their structure, a literal of type integer.</span></span> <span data-ttu-id="d3fe0-116">La versione dello schema corrente è "1".</span><span class="sxs-lookup"><span data-stu-id="d3fe0-116">The current schema version is "1".</span></span> <span data-ttu-id="d3fe0-117">Questo attributo è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-117">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="d3fe0-118">Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="d3fe0-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="d3fe0-119">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d3fe0-119">Element Information</span></span>

<span data-ttu-id="d3fe0-120">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="d3fe0-121">Category</span><span class="sxs-lookup"><span data-stu-id="d3fe0-121">Category</span></span>                   | <span data-ttu-id="d3fe0-122">Dettagli</span><span class="sxs-lookup"><span data-stu-id="d3fe0-122">Details</span></span>                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3fe0-123">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d3fe0-123">Parent elements</span></span><br/> | <span data-ttu-id="d3fe0-124">Solo radice del documento.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-124">Document root only.</span></span><br/>                                                                                     |
| <span data-ttu-id="d3fe0-125">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d3fe0-125">Child elements</span></span><br/>  | <span data-ttu-id="d3fe0-126">*Funzionalità* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="d3fe0-126">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="d3fe0-127">*ParameterInit* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="d3fe0-127">*ParameterInit* (zero or more)</span></span><br/> <span data-ttu-id="d3fe0-128">*Property* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="d3fe0-128">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="d3fe0-129">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="d3fe0-129">This element</span></span><br/>    | <span data-ttu-id="d3fe0-130">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-130">No character data is permitted.</span></span><br/> <span data-ttu-id="d3fe0-131">Gli elementi di pari livello figlio duplicati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-131">Duplicate child siblings are not permitted.</span></span><br/>                  |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="d3fe0-132">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="d3fe0-132">Configuration Dependencies</span></span>

<span data-ttu-id="d3fe0-133">Le dipendenze di configurazione sono applicabili solo agli elementi in un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-133">Configuration dependencies are applicable only to elements in a PrintCapabilities document.</span></span>

## <a name="example"></a><span data-ttu-id="d3fe0-134">Esempio</span><span class="sxs-lookup"><span data-stu-id="d3fe0-134">Example</span></span>

<span data-ttu-id="d3fe0-135">Vedere [esempio di PrintTicket](printticket-example.md).</span><span class="sxs-lookup"><span data-stu-id="d3fe0-135">See [PrintTicket Example](printticket-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3fe0-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d3fe0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3fe0-137">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="d3fe0-137">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




