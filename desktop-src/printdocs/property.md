---
description: Informazioni sull'elemento Property nei documenti e nella stampa. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Proprietà (documenti e stampa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e43b52c054972ee0ee2b8a535021581c05e7d96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120296"
---
# <a name="property-documents-and-printing"></a><span data-ttu-id="c5c05-105">Proprietà (documenti e stampa)</span><span class="sxs-lookup"><span data-stu-id="c5c05-105">Property (Documents and Printing)</span></span>

<span data-ttu-id="c5c05-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="c5c05-106">This topic is not current.</span></span> <span data-ttu-id="c5c05-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c5c05-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c5c05-108">Un elemento Property dichiara un dispositivo, una formattazione del processo o un'altra proprietà pertinente il cui nome viene assegnato dal relativo attributo name.</span><span class="sxs-lookup"><span data-stu-id="c5c05-108">A Property element declares a device, job formatting, or other relevant property whose name is given by its name attribute.</span></span> <span data-ttu-id="c5c05-109">Un elemento Value viene usato per assegnare un valore alla proprietà .</span><span class="sxs-lookup"><span data-stu-id="c5c05-109">A Value element is used to assign a value to the Property.</span></span>

<span data-ttu-id="c5c05-110">Una proprietà può essere complessa, possibilmente contenente più sottoproprietà.</span><span class="sxs-lookup"><span data-stu-id="c5c05-110">A Property can be complex, possibly containing multiple subproperties.</span></span> <span data-ttu-id="c5c05-111">Le sottoproprietà sono rappresentate anche da elementi Property.</span><span class="sxs-lookup"><span data-stu-id="c5c05-111">Subproperties are also represented by Property elements.</span></span>

## <a name="element-tag"></a><span data-ttu-id="c5c05-112">Tag di elemento</span><span class="sxs-lookup"><span data-stu-id="c5c05-112">Element Tag</span></span>

<Property>

## <a name="xml-attributes"></a><span data-ttu-id="c5c05-113">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="c5c05-113">XML Attributes</span></span>

<span data-ttu-id="c5c05-114">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="c5c05-114">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="c5c05-115">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="c5c05-115">XML Attribute</span></span>   | <span data-ttu-id="c5c05-116">Dettagli</span><span class="sxs-lookup"><span data-stu-id="c5c05-116">Details</span></span>                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c05-117">name</span><span class="sxs-lookup"><span data-stu-id="c5c05-117">name</span></span><br/> | <span data-ttu-id="c5c05-118">Contiene l'attributo name della proprietà , che è una proprietà standard o una proprietà definita privatamente.</span><span class="sxs-lookup"><span data-stu-id="c5c05-118">Holds the name attribute of the Property, which is either a standard Property or a privately-defined Property.</span></span> <br/> |



 

<span data-ttu-id="c5c05-119">Per altre informazioni, vedere la [sezione Attributi XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="c5c05-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="c5c05-120">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c5c05-120">Element Information</span></span>

<span data-ttu-id="c5c05-121">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="c5c05-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="c5c05-122">Categoria</span><span class="sxs-lookup"><span data-stu-id="c5c05-122">Category</span></span>                   | <span data-ttu-id="c5c05-123">Dettagli</span><span class="sxs-lookup"><span data-stu-id="c5c05-123">Details</span></span>                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c05-124">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="c5c05-124">Parent elements</span></span><br/> | <span data-ttu-id="c5c05-125">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="c5c05-125">PrintCapabilities</span></span> <br/> <span data-ttu-id="c5c05-126">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="c5c05-126">Feature</span></span><br/> <span data-ttu-id="c5c05-127">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="c5c05-127">PrintTicket</span></span><br/> <span data-ttu-id="c5c05-128">Opzione</span><span class="sxs-lookup"><span data-stu-id="c5c05-128">Option</span></span><br/> <span data-ttu-id="c5c05-129">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c5c05-129">ParameterDef</span></span><br/> <span data-ttu-id="c5c05-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c5c05-130">Property</span></span><br/> <span data-ttu-id="c5c05-131">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="c5c05-131">ScoredProperty</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="c5c05-132">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c5c05-132">Child elements</span></span><br/>  | <span data-ttu-id="c5c05-133">Il sistema non assegna alcun significato all'ordinamento degli elementi.</span><span class="sxs-lookup"><span data-stu-id="c5c05-133">The system assigns no significance to the ordering of the elements.</span></span> <span data-ttu-id="c5c05-134">Se i client scelgono di attribuire un significato nell'ordinamento degli elementi, sono liberi di farlo.</span><span class="sxs-lookup"><span data-stu-id="c5c05-134">If clients choose to ascribe some significance in the ordering of the elements, they are free to do so.</span></span> <br/> <span data-ttu-id="c5c05-135">*Proprietà* (uno o più) *Valore* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="c5c05-135">*Property* (one or more) *Value* (zero or more)</span></span><br/> <span data-ttu-id="c5c05-136">oppure</span><span class="sxs-lookup"><span data-stu-id="c5c05-136">or</span></span> <br/> <span data-ttu-id="c5c05-137">*Proprietà* (zero o più) *Valore* (uno o più)</span><span class="sxs-lookup"><span data-stu-id="c5c05-137">*Property* (zero or more) *Value* (one or more)</span></span><br/> |
| <span data-ttu-id="c5c05-138">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="c5c05-138">This element</span></span><br/>    | <span data-ttu-id="c5c05-139">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="c5c05-139">No character data is permitted.</span></span><br/> <span data-ttu-id="c5c05-140">Sono consentiti elementi Value figlio duplicati di pari livello.</span><span class="sxs-lookup"><span data-stu-id="c5c05-140">Duplicate child Value elements that are siblings are permitted.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="c5c05-141">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="c5c05-141">Configuration Dependencies</span></span>

<span data-ttu-id="c5c05-142">Una proprietà può avere dipendenze di configurazione, tranne quando viene visualizzata all'interno di un elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="c5c05-142">A Property may have configuration dependencies, except when it appears within a ParameterDef element.</span></span>

## <a name="element-usage"></a><span data-ttu-id="c5c05-143">Utilizzo degli elementi</span><span class="sxs-lookup"><span data-stu-id="c5c05-143">Element Usage</span></span>

<span data-ttu-id="c5c05-144">Oltre a essere visualizzati all'interno degli elementi Feature e Option, gli elementi Property possono essere visualizzati al livello radice delle rispettive tecnologie sottostanti.</span><span class="sxs-lookup"><span data-stu-id="c5c05-144">In addition to appearing within Feature and Option elements, Property elements can appear at the root level of the respective underlying technologies.</span></span> <span data-ttu-id="c5c05-145">Lo schema di stampa definisce un set di elementi Property che possono essere usati per descrivere un dispositivo in modo portabile.</span><span class="sxs-lookup"><span data-stu-id="c5c05-145">The Print Schema defines a set of Property elements that can be used to describe a device in a portable manner.</span></span> <span data-ttu-id="c5c05-146">Tuttavia, se queste proprietà non sono sufficienti alle proprie esigenze come provider PrintCapabilities (in genere perché il dispositivo supportato presenta aspetti nuovi non previsti dallo schema di stampa), è possibile introdurre elementi Property privati.</span><span class="sxs-lookup"><span data-stu-id="c5c05-146">However, if these properties are insufficient to your needs as a PrintCapabilities provider (typically because the device being supported has novel aspects not anticipated by the Print Schema), you may introduce your own private Property elements.</span></span> <span data-ttu-id="c5c05-147">È possibile migliorare o elaborare le informazioni fornite da una proprietà pubblica aggiungendo una o più sottoproprietà private come contenuto dell'elemento della proprietà pubblica.</span><span class="sxs-lookup"><span data-stu-id="c5c05-147">You can enhance or elaborate the information provided by a public Property by adding one or more private subproperties as element content of the public Property.</span></span>

<span data-ttu-id="c5c05-148">Gli elementi proprietà vengono definiti usando un tag di elemento XML, <Property> .</span><span class="sxs-lookup"><span data-stu-id="c5c05-148">Property elements are defined by using an XML element tag, <Property>.</span></span> <span data-ttu-id="c5c05-149">A ogni proprietà viene assegnato un nome tramite il relativo attributo name.</span><span class="sxs-lookup"><span data-stu-id="c5c05-149">Each Property is assigned a name by means of its name attribute.</span></span> <span data-ttu-id="c5c05-150">Il nome deve essere un QName XML e deve essere conforme alla convenzione dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="c5c05-150">The name must be an XML QName and must conform to the Namespace Convention.</span></span> <span data-ttu-id="c5c05-151">Per informazioni dettagliate, vedere [Attributi XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="c5c05-151">For details, see [XML Attributes](xml-attributes.md).</span></span> <span data-ttu-id="c5c05-152">L'attributo Nome proprietà e la relativa posizione all'interno della gerarchia degli elementi Property padre (se si tratta di una sottoproprietà) identificano in modo univoco la proprietà all'interno del documento PrintCapabilities o PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="c5c05-152">The Property name attribute and its location within the hierarchy of parent Property elements (if it is a subproperty) uniquely identify the Property within the PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="c5c05-153">Una proprietà può contenere uno o più elementi Value oppure uno o più elementi Property figlio (denominati sottoproprietà) o una combinazione di entrambi.</span><span class="sxs-lookup"><span data-stu-id="c5c05-153">A Property may contain one or more Value elements, or one or more child Property elements (called subproperties), or a combination of both.</span></span> <span data-ttu-id="c5c05-154">Le sottoproprietà sono utili quando la proprietà stessa è costituita da più componenti.</span><span class="sxs-lookup"><span data-stu-id="c5c05-154">Subproperties are useful when the Property itself is composed of multiple components.</span></span> <span data-ttu-id="c5c05-155">Ad esempio, una proprietà "ConsumableColor" potrebbe avere componenti "C", "M" e "Y".</span><span class="sxs-lookup"><span data-stu-id="c5c05-155">For example, a "ConsumableColor" Property might have "C", "M", and "Y" components.</span></span>

## <a name="example"></a><span data-ttu-id="c5c05-156">Esempio</span><span class="sxs-lookup"><span data-stu-id="c5c05-156">Example</span></span>

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="c5c05-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5c05-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5c05-158">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="c5c05-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




