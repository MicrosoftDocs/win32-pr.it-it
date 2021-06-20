---
description: Informazioni sull'elemento PrintCapabilities, che rappresenta la radice del documento PrintCapabilities.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2158fd651849df2e4ea24c640065f1041569741a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407024"
---
# <a name="printcapabilities"></a><span data-ttu-id="ef874-103">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="ef874-103">PrintCapabilities</span></span>

<span data-ttu-id="ef874-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="ef874-104">This topic is not current.</span></span> <span data-ttu-id="ef874-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ef874-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ef874-106">Un elemento PrintCapabilities rappresenta la radice del documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="ef874-106">A PrintCapabilities element represents the root of the PrintCapabilities document.</span></span> <span data-ttu-id="ef874-107">Il documento PrintCapabilities contiene tutte le informazioni necessarie per descrivere gli attributi del dispositivo supportati, data una particolare configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef874-107">The PrintCapabilities document contains all of the information needed to describe the supported device attributes, given a particular device configuration.</span></span>

## <a name="element-tag"></a><span data-ttu-id="ef874-108">Element Tag</span><span class="sxs-lookup"><span data-stu-id="ef874-108">Element Tag</span></span>

<PrintCapabilities>

## <a name="xml-attributes"></a><span data-ttu-id="ef874-109">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="ef874-109">XML Attributes</span></span>

<span data-ttu-id="ef874-110">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="ef874-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="ef874-111">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="ef874-111">XML Attribute</span></span>      | <span data-ttu-id="ef874-112">Dettagli</span><span class="sxs-lookup"><span data-stu-id="ef874-112">Details</span></span>                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef874-113">version</span><span class="sxs-lookup"><span data-stu-id="ef874-113">version</span></span><br/> | <span data-ttu-id="ef874-114">Specifica la versione dello schema che definisce i tipi di elemento e la relativa struttura.</span><span class="sxs-lookup"><span data-stu-id="ef874-114">Specifies the version of the schema that defines element types and their structure.</span></span> <span data-ttu-id="ef874-115">L'attributo version è di tipo integer.</span><span class="sxs-lookup"><span data-stu-id="ef874-115">The version attribute is of type integer.</span></span> <span data-ttu-id="ef874-116">La versione corrente dello schema è definita "1".</span><span class="sxs-lookup"><span data-stu-id="ef874-116">The current schema version is designated "1".</span></span> <span data-ttu-id="ef874-117">Questo attributo è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ef874-117">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="ef874-118">Per altre informazioni, vedere la [sezione Attributi](xml-attributes.md) XML.</span><span class="sxs-lookup"><span data-stu-id="ef874-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="ef874-119">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ef874-119">Element Information</span></span>

<span data-ttu-id="ef874-120">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="ef874-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="ef874-121">Categoria</span><span class="sxs-lookup"><span data-stu-id="ef874-121">Category</span></span>                   | <span data-ttu-id="ef874-122">Dettagli</span><span class="sxs-lookup"><span data-stu-id="ef874-122">Details</span></span>                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef874-123">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="ef874-123">Parent elements</span></span><br/> | <span data-ttu-id="ef874-124">Solo radice del documento.</span><span class="sxs-lookup"><span data-stu-id="ef874-124">Document root only.</span></span><br/>                                                                                    |
| <span data-ttu-id="ef874-125">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ef874-125">Child elements</span></span><br/>  | <span data-ttu-id="ef874-126">*Funzionalità* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="ef874-126">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="ef874-127">*ParameterDef* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="ef874-127">*ParameterDef* (zero or more)</span></span><br/> <span data-ttu-id="ef874-128">*Proprietà* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="ef874-128">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="ef874-129">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="ef874-129">This element</span></span><br/>    | <span data-ttu-id="ef874-130">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="ef874-130">No character data is permitted.</span></span><br/> <span data-ttu-id="ef874-131">Gli elementi di pari livello figlio duplicati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="ef874-131">Duplicate child siblings are not permitted.</span></span><br/>                 |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="ef874-132">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="ef874-132">Configuration Dependencies</span></span>

<span data-ttu-id="ef874-133">L'elemento radice potrebbe non avere dipendenze di configurazione.</span><span class="sxs-lookup"><span data-stu-id="ef874-133">The root element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="ef874-134">Esempio</span><span class="sxs-lookup"><span data-stu-id="ef874-134">Example</span></span>

<span data-ttu-id="ef874-135">Vedere [Esempio di documento PrintCapabilities.](printcapabilities-document-example.md)</span><span class="sxs-lookup"><span data-stu-id="ef874-135">See [PrintCapabilities Document Example](printcapabilities-document-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef874-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ef874-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef874-137">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ef874-137">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




