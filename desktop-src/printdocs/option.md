---
description: Ottiene informazioni sull'elemento Option. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Opzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ac4318e6a79a3d4daa77f15901d032c66134bdd
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549379"
---
# <a name="option"></a><span data-ttu-id="33ee4-105">Opzione</span><span class="sxs-lookup"><span data-stu-id="33ee4-105">Option</span></span>

<span data-ttu-id="33ee4-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="33ee4-106">This topic is not current.</span></span> <span data-ttu-id="33ee4-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="33ee4-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="33ee4-108">Un elemento Option contiene tutti gli elementi Property e ScoredProperty associati a questa opzione.</span><span class="sxs-lookup"><span data-stu-id="33ee4-108">An Option element contains all of the Property and ScoredProperty elements associated with this option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="33ee4-109">Element Tag</span><span class="sxs-lookup"><span data-stu-id="33ee4-109">Element Tag</span></span>

<Option>

## <a name="xml-attributes"></a><span data-ttu-id="33ee4-110">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="33ee4-110">XML Attributes</span></span>

<span data-ttu-id="33ee4-111">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="33ee4-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="33ee4-112">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="33ee4-112">XML Attribute</span></span>          | <span data-ttu-id="33ee4-113">Dettagli</span><span class="sxs-lookup"><span data-stu-id="33ee4-113">Details</span></span>                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33ee4-114">Vincolata</span><span class="sxs-lookup"><span data-stu-id="33ee4-114">constrained</span></span><br/> | <span data-ttu-id="33ee4-115">Questo attributo è facoltativo per un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="33ee4-115">This attribute is optional for a PrintCapabilities document.</span></span><br/> <span data-ttu-id="33ee4-116">Questo attributo indica se l'opzione è disponibile per la selezione o l'uso.</span><span class="sxs-lookup"><span data-stu-id="33ee4-116">This attribute indicates whether the Option is available for selection or use.</span></span> <span data-ttu-id="33ee4-117">Questo attributo XML può essere impostato su uno dei valori seguenti: None, PrintTicketSettings, AdminSetting o DeviceSettings.</span><span class="sxs-lookup"><span data-stu-id="33ee4-117">This XML attribute can be set to one of the following values: None, PrintTicketSettings, AdminSetting or DeviceSettings.</span></span> <br/> <span data-ttu-id="33ee4-118">Vedere [Attributi XML](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="33ee4-118">See [XML Attributes](xml-attributes.md)</span></span><br/> |
| <span data-ttu-id="33ee4-119">name</span><span class="sxs-lookup"><span data-stu-id="33ee4-119">name</span></span><br/>        | <span data-ttu-id="33ee4-120">Contiene il nome dell'opzione, un'opzione standard o un'opzione definita privatamente.</span><span class="sxs-lookup"><span data-stu-id="33ee4-120">Holds the name of the Option, either a standard Option or a privately-defined Option.</span></span> <span data-ttu-id="33ee4-121">L'attributo XML viene utilizzato in questo modo per distinguere le istanze option.</span><span class="sxs-lookup"><span data-stu-id="33ee4-121">The XML attribute is used this way in order to differentiate between Option instances.</span></span> <br/>                                                                                                                                                        |



 

<span data-ttu-id="33ee4-122">Per altre informazioni, vedere la [sezione Attributi](xml-attributes.md) XML.</span><span class="sxs-lookup"><span data-stu-id="33ee4-122">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="33ee4-123">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="33ee4-123">Element Information</span></span>

<span data-ttu-id="33ee4-124">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="33ee4-124">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="33ee4-125">Category</span><span class="sxs-lookup"><span data-stu-id="33ee4-125">Category</span></span>                   | <span data-ttu-id="33ee4-126">Dettagli</span><span class="sxs-lookup"><span data-stu-id="33ee4-126">Details</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33ee4-127">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="33ee4-127">Parent elements</span></span><br/> | <span data-ttu-id="33ee4-128">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="33ee4-128">Feature</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="33ee4-129">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="33ee4-129">Child elements</span></span><br/>  | <span data-ttu-id="33ee4-130">*Proprietà* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="33ee4-130">*Property* (zero or more)</span></span><br/> <span data-ttu-id="33ee4-131">*ScoredProperty* (zero o più per Options con attributo XML 'name'; una o più per Options che non utilizzano l'attributo XML \* 'name')</span><span class="sxs-lookup"><span data-stu-id="33ee4-131">*ScoredProperty* (zero or more for Options with XML Attribute 'name'; one or more for Options not utilizing XML Attribute 'name'\*)</span></span><br/> <span data-ttu-id="33ee4-132">\* solo le opzioni pubbliche definite nello schema di stampa non possono avere un attributo 'name', ad esempio DocumentNUp</span><span class="sxs-lookup"><span data-stu-id="33ee4-132">\* only public Options defined in Print Schema can have no 'name' attribute, such as DocumentNUp)</span></span><br/> |
| <span data-ttu-id="33ee4-133">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="33ee4-133">This element</span></span><br/>    | <span data-ttu-id="33ee4-134">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="33ee4-134">No character data is permitted.</span></span><br/> <span data-ttu-id="33ee4-135">Gli elementi di pari livello figlio duplicati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="33ee4-135">Duplicate child siblings are not permitted.</span></span><br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="33ee4-136">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="33ee4-136">Configuration Dependencies</span></span>

<span data-ttu-id="33ee4-137">Un elemento di definizione Option potrebbe non avere dipendenze di configurazione.</span><span class="sxs-lookup"><span data-stu-id="33ee4-137">An Option definition element may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="33ee4-138">Utilizzo degli elementi</span><span class="sxs-lookup"><span data-stu-id="33ee4-138">Element Usage</span></span>

<span data-ttu-id="33ee4-139">Lo scopo dell'elemento Option è quello di caratterizzare uno degli stati che un attributo di configurazione del dispositivo, rappresentato da un elemento Feature, può assumere.</span><span class="sxs-lookup"><span data-stu-id="33ee4-139">The purpose of the Option element is to characterize one of the states that a device configuration attribute, represented by a Feature element, can assume.</span></span> <span data-ttu-id="33ee4-140">Ogni definizione di elemento Option contiene uno o più elementi ScoredProperty che descrivono una caratteristica intrinseca o essenziale di tale opzione.</span><span class="sxs-lookup"><span data-stu-id="33ee4-140">Each Option element definition contains one or more ScoredProperty elements that describe an intrinsic or essential characteristic of that Option.</span></span> <span data-ttu-id="33ee4-141">Per facilitare la portabilità e la conservazione della finalità, lo schema di stampa definisce molti elementi feature comuni e un'ampia gamma di elementi Option per ogni funzionalità.</span><span class="sxs-lookup"><span data-stu-id="33ee4-141">To facilitate portability and preservation of intent, the Print Schema defines many common Feature elements and a variety of Option elements for each Feature.</span></span> <span data-ttu-id="33ee4-142">È quindi importante usare gli elementi Option definiti nello schema di stampa, se possibile, prima di creare definizioni di opzione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="33ee4-142">It is therefore important to use Print Schema-defined Option elements, if at all possible, before you create your own Option definitions.</span></span> <span data-ttu-id="33ee4-143">La comprensione del processo di definizione degli elementi Option offre informazioni utili sul modo in cui il documento PrintCapabilities e i PrintTicket vengono usati nell'architettura di stampa di Microsoft .NET Framework versione 3.0 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="33ee4-143">Understanding the process of defining Option elements provides useful insights into the way the PrintCapabilities document and PrintTickets are used in the Microsoft .NET Framework version 3.0 and Windows Vista printing architecture.</span></span>

## <a name="example"></a><span data-ttu-id="33ee4-144">Esempio</span><span class="sxs-lookup"><span data-stu-id="33ee4-144">Example</span></span>

<span data-ttu-id="33ee4-145">Nell'esempio seguente viene definito un nome per l'opzione .</span><span class="sxs-lookup"><span data-stu-id="33ee4-145">The following example defines a name for the Option.</span></span>

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a><span data-ttu-id="33ee4-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="33ee4-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33ee4-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="33ee4-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




