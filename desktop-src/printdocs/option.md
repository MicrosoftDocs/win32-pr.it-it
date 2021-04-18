---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Opzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379834d12cd01847c95783d727be5dcdc6c575bf
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321050"
---
# <a name="option"></a><span data-ttu-id="f1701-104">Opzione</span><span class="sxs-lookup"><span data-stu-id="f1701-104">Option</span></span>

<span data-ttu-id="f1701-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f1701-105">This topic is not current.</span></span> <span data-ttu-id="f1701-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f1701-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f1701-107">Un elemento option contiene tutti gli elementi Property e ScoredProperty associati a questa opzione.</span><span class="sxs-lookup"><span data-stu-id="f1701-107">An Option element contains all of the Property and ScoredProperty elements associated with this option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="f1701-108">Tag elemento</span><span class="sxs-lookup"><span data-stu-id="f1701-108">Element Tag</span></span>

<Option>

## <a name="xml-attributes"></a><span data-ttu-id="f1701-109">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="f1701-109">XML Attributes</span></span>

<span data-ttu-id="f1701-110">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="f1701-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="f1701-111">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="f1701-111">XML Attribute</span></span>          | <span data-ttu-id="f1701-112">Dettagli</span><span class="sxs-lookup"><span data-stu-id="f1701-112">Details</span></span>                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1701-113">vincolata</span><span class="sxs-lookup"><span data-stu-id="f1701-113">constrained</span></span><br/> | <span data-ttu-id="f1701-114">Questo attributo è facoltativo per un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="f1701-114">This attribute is optional for a PrintCapabilities document.</span></span><br/> <span data-ttu-id="f1701-115">Questo attributo indica se l'opzione è disponibile per la selezione o l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="f1701-115">This attribute indicates whether the Option is available for selection or use.</span></span> <span data-ttu-id="f1701-116">Questo attributo XML può essere impostato su uno dei valori seguenti: None, PrintTicketSettings, AdminSetting o DeviceSettings.</span><span class="sxs-lookup"><span data-stu-id="f1701-116">This XML attribute can be set to one of the following values: None, PrintTicketSettings, AdminSetting or DeviceSettings.</span></span> <br/> <span data-ttu-id="f1701-117">Vedere [attributi XML](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="f1701-117">See [XML Attributes](xml-attributes.md)</span></span><br/> |
| <span data-ttu-id="f1701-118">name</span><span class="sxs-lookup"><span data-stu-id="f1701-118">name</span></span><br/>        | <span data-ttu-id="f1701-119">Include il nome dell'opzione, ovvero un'opzione standard o un'opzione definita privatamente.</span><span class="sxs-lookup"><span data-stu-id="f1701-119">Holds the name of the Option, either a standard Option or a privately-defined Option.</span></span> <span data-ttu-id="f1701-120">L'attributo XML viene usato in questo modo per distinguere le istanze di opzioni.</span><span class="sxs-lookup"><span data-stu-id="f1701-120">The XML attribute is used this way in order to differentiate between Option instances.</span></span> <br/>                                                                                                                                                        |



 

<span data-ttu-id="f1701-121">Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="f1701-121">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="f1701-122">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f1701-122">Element Information</span></span>

<span data-ttu-id="f1701-123">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="f1701-123">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="f1701-124">Category</span><span class="sxs-lookup"><span data-stu-id="f1701-124">Category</span></span>                   | <span data-ttu-id="f1701-125">Dettagli</span><span class="sxs-lookup"><span data-stu-id="f1701-125">Details</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1701-126">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f1701-126">Parent elements</span></span><br/> | <span data-ttu-id="f1701-127">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="f1701-127">Feature</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f1701-128">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f1701-128">Child elements</span></span><br/>  | <span data-ttu-id="f1701-129">*Property* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="f1701-129">*Property* (zero or more)</span></span><br/> <span data-ttu-id="f1701-130">*ScoredProperty* (zero o più opzioni con l'attributo XML ' name '; una o più opzioni per l'utilizzo dell'attributo XML ' name ' \* )</span><span class="sxs-lookup"><span data-stu-id="f1701-130">*ScoredProperty* (zero or more for Options with XML Attribute 'name'; one or more for Options not utilizing XML Attribute 'name'\*)</span></span><br/> <span data-ttu-id="f1701-131">\* solo le opzioni pubbliche definite nello schema di stampa non possono avere un attributo ' name ', ad esempio DocumentNUp</span><span class="sxs-lookup"><span data-stu-id="f1701-131">\* only public Options defined in Print Schema can have no 'name' attribute, such as DocumentNUp)</span></span><br/> |
| <span data-ttu-id="f1701-132">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="f1701-132">This element</span></span><br/>    | <span data-ttu-id="f1701-133">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="f1701-133">No character data is permitted.</span></span><br/> <span data-ttu-id="f1701-134">Gli elementi di pari livello figlio duplicati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="f1701-134">Duplicate child siblings are not permitted.</span></span><br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="f1701-135">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="f1701-135">Configuration Dependencies</span></span>

<span data-ttu-id="f1701-136">Un elemento di definizione di opzione non può avere dipendenze di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f1701-136">An Option definition element may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="f1701-137">Utilizzo elementi</span><span class="sxs-lookup"><span data-stu-id="f1701-137">Element Usage</span></span>

<span data-ttu-id="f1701-138">Lo scopo dell'elemento option è quello di caratterizzare uno degli Stati che un attributo di configurazione del dispositivo, rappresentato da un elemento Feature, può assumere.</span><span class="sxs-lookup"><span data-stu-id="f1701-138">The purpose of the Option element is to characterize one of the states that a device configuration attribute, represented by a Feature element, can assume.</span></span> <span data-ttu-id="f1701-139">Ogni definizione di elemento option contiene uno o più elementi ScoredProperty che descrivono una caratteristica intrinseca o essenziale di tale opzione.</span><span class="sxs-lookup"><span data-stu-id="f1701-139">Each Option element definition contains one or more ScoredProperty elements that describe an intrinsic or essential characteristic of that Option.</span></span> <span data-ttu-id="f1701-140">Per facilitare la portabilità e la conservazione dello scopo, lo schema di stampa definisce molti elementi di funzionalità comuni e una varietà di elementi option per ciascuna funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f1701-140">To facilitate portability and preservation of intent, the Print Schema defines many common Feature elements and a variety of Option elements for each Feature.</span></span> <span data-ttu-id="f1701-141">È quindi importante usare gli elementi delle opzioni di stampa definiti dallo schema, se possibile, prima di creare definizioni di opzioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="f1701-141">It is therefore important to use Print Schema-defined Option elements, if at all possible, before you create your own Option definitions.</span></span> <span data-ttu-id="f1701-142">La comprensione del processo di definizione degli elementi delle opzioni fornisce informazioni utili sul modo in cui il documento PrintCapabilities e gli PrintTicket vengono utilizzati nella versione di Microsoft .NET Framework 3,0 e nell'architettura di stampa di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f1701-142">Understanding the process of defining Option elements provides useful insights into the way the PrintCapabilities document and PrintTickets are used in the Microsoft .NET Framework version 3.0 and Windows Vista printing architecture.</span></span>

## <a name="example"></a><span data-ttu-id="f1701-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="f1701-143">Example</span></span>

<span data-ttu-id="f1701-144">Nell'esempio seguente viene definito un nome per l'opzione.</span><span class="sxs-lookup"><span data-stu-id="f1701-144">The following example defines a name for the Option.</span></span>

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a><span data-ttu-id="f1701-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1701-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1701-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f1701-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




