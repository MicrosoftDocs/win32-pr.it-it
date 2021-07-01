---
description: Trovare informazioni sull'elemento PrintTicket. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b279ff681704a63f6547738c73fb9192d6f8a65d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120076"
---
# <a name="printticket"></a><span data-ttu-id="ccae8-105">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="ccae8-105">PrintTicket</span></span>

<span data-ttu-id="ccae8-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="ccae8-106">This topic is not current.</span></span> <span data-ttu-id="ccae8-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ccae8-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ccae8-108">Un elemento PrintTicket è l'elemento radice del documento PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="ccae8-108">A PrintTicket element is the root element of the PrintTicket document.</span></span> <span data-ttu-id="ccae8-109">Un elemento PrintTicket contiene tutte le informazioni di formattazione del processo necessarie per l'output di un processo.</span><span class="sxs-lookup"><span data-stu-id="ccae8-109">A PrintTicket element contains all job formatting information required to output a job.</span></span>

## <a name="element-tag"></a><span data-ttu-id="ccae8-110">Element Tag</span><span class="sxs-lookup"><span data-stu-id="ccae8-110">Element Tag</span></span>

<PrintTicket>

## <a name="xml-attributes"></a><span data-ttu-id="ccae8-111">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="ccae8-111">XML Attributes</span></span>

<span data-ttu-id="ccae8-112">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="ccae8-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="ccae8-113">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="ccae8-113">XML Attribute</span></span>      | <span data-ttu-id="ccae8-114">Dettagli</span><span class="sxs-lookup"><span data-stu-id="ccae8-114">Details</span></span>                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccae8-115">version</span><span class="sxs-lookup"><span data-stu-id="ccae8-115">version</span></span><br/> | <span data-ttu-id="ccae8-116">Specifica la versione dello schema che definisce i tipi di elemento e la relativa struttura, un valore letterale di tipo integer.</span><span class="sxs-lookup"><span data-stu-id="ccae8-116">Specifies the version of the schema that defines element types and their structure, a literal of type integer.</span></span> <span data-ttu-id="ccae8-117">La versione corrente dello schema è "1".</span><span class="sxs-lookup"><span data-stu-id="ccae8-117">The current schema version is "1".</span></span> <span data-ttu-id="ccae8-118">Questo attributo è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ccae8-118">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="ccae8-119">Per altre informazioni, vedere la [sezione Attributi](xml-attributes.md) XML.</span><span class="sxs-lookup"><span data-stu-id="ccae8-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="ccae8-120">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ccae8-120">Element Information</span></span>

<span data-ttu-id="ccae8-121">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="ccae8-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="ccae8-122">Categoria</span><span class="sxs-lookup"><span data-stu-id="ccae8-122">Category</span></span>                   | <span data-ttu-id="ccae8-123">Dettagli</span><span class="sxs-lookup"><span data-stu-id="ccae8-123">Details</span></span>                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccae8-124">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="ccae8-124">Parent elements</span></span><br/> | <span data-ttu-id="ccae8-125">Solo radice del documento.</span><span class="sxs-lookup"><span data-stu-id="ccae8-125">Document root only.</span></span><br/>                                                                                     |
| <span data-ttu-id="ccae8-126">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ccae8-126">Child elements</span></span><br/>  | <span data-ttu-id="ccae8-127">*Funzionalità* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="ccae8-127">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="ccae8-128">*ParameterInit* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="ccae8-128">*ParameterInit* (zero or more)</span></span><br/> <span data-ttu-id="ccae8-129">*Proprietà* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="ccae8-129">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="ccae8-130">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="ccae8-130">This element</span></span><br/>    | <span data-ttu-id="ccae8-131">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="ccae8-131">No character data is permitted.</span></span><br/> <span data-ttu-id="ccae8-132">Gli elementi di pari livello figlio duplicati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="ccae8-132">Duplicate child siblings are not permitted.</span></span><br/>                  |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="ccae8-133">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="ccae8-133">Configuration Dependencies</span></span>

<span data-ttu-id="ccae8-134">Le dipendenze di configurazione sono applicabili solo agli elementi in un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="ccae8-134">Configuration dependencies are applicable only to elements in a PrintCapabilities document.</span></span>

## <a name="example"></a><span data-ttu-id="ccae8-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="ccae8-135">Example</span></span>

<span data-ttu-id="ccae8-136">Vedere [Esempio di PrintTicket.](printticket-example.md)</span><span class="sxs-lookup"><span data-stu-id="ccae8-136">See [PrintTicket Example](printticket-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccae8-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ccae8-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccae8-138">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ccae8-138">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




