---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Proprietà (documenti e stampa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fb4a057b2cf7795262b595c59f9da0343fdf12
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351866"
---
# <a name="property-documents-and-printing"></a><span data-ttu-id="ad945-104">Proprietà (documenti e stampa)</span><span class="sxs-lookup"><span data-stu-id="ad945-104">Property (Documents and Printing)</span></span>

<span data-ttu-id="ad945-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="ad945-105">This topic is not current.</span></span> <span data-ttu-id="ad945-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ad945-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ad945-107">Un elemento Property dichiara un dispositivo, una formattazione del processo o un'altra proprietà pertinente il cui nome è fornito dall'attributo Name.</span><span class="sxs-lookup"><span data-stu-id="ad945-107">A Property element declares a device, job formatting, or other relevant property whose name is given by its name attribute.</span></span> <span data-ttu-id="ad945-108">Un elemento value viene usato per assegnare un valore alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="ad945-108">A Value element is used to assign a value to the Property.</span></span>

<span data-ttu-id="ad945-109">Una proprietà può essere complessa, possibilmente contenente più sottoproprietà.</span><span class="sxs-lookup"><span data-stu-id="ad945-109">A Property can be complex, possibly containing multiple subproperties.</span></span> <span data-ttu-id="ad945-110">Le sottoproprietà sono rappresentate anche dagli elementi della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ad945-110">Subproperties are also represented by Property elements.</span></span>

## <a name="element-tag"></a><span data-ttu-id="ad945-111">Tag elemento</span><span class="sxs-lookup"><span data-stu-id="ad945-111">Element Tag</span></span>

<Property>

## <a name="xml-attributes"></a><span data-ttu-id="ad945-112">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="ad945-112">XML Attributes</span></span>

<span data-ttu-id="ad945-113">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="ad945-113">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="ad945-114">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="ad945-114">XML Attribute</span></span>   | <span data-ttu-id="ad945-115">Dettagli</span><span class="sxs-lookup"><span data-stu-id="ad945-115">Details</span></span>                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad945-116">name</span><span class="sxs-lookup"><span data-stu-id="ad945-116">name</span></span><br/> | <span data-ttu-id="ad945-117">Include l'attributo Name della proprietà, che può essere una proprietà standard o una proprietà definita privatamente.</span><span class="sxs-lookup"><span data-stu-id="ad945-117">Holds the name attribute of the Property, which is either a standard Property or a privately-defined Property.</span></span> <br/> |



 

<span data-ttu-id="ad945-118">Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="ad945-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="ad945-119">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ad945-119">Element Information</span></span>

<span data-ttu-id="ad945-120">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="ad945-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="ad945-121">Category</span><span class="sxs-lookup"><span data-stu-id="ad945-121">Category</span></span>                   | <span data-ttu-id="ad945-122">Dettagli</span><span class="sxs-lookup"><span data-stu-id="ad945-122">Details</span></span>                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad945-123">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="ad945-123">Parent elements</span></span><br/> | <span data-ttu-id="ad945-124">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="ad945-124">PrintCapabilities</span></span> <br/> <span data-ttu-id="ad945-125">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="ad945-125">Feature</span></span><br/> <span data-ttu-id="ad945-126">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="ad945-126">PrintTicket</span></span><br/> <span data-ttu-id="ad945-127">Opzione</span><span class="sxs-lookup"><span data-stu-id="ad945-127">Option</span></span><br/> <span data-ttu-id="ad945-128">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ad945-128">ParameterDef</span></span><br/> <span data-ttu-id="ad945-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ad945-129">Property</span></span><br/> <span data-ttu-id="ad945-130">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="ad945-130">ScoredProperty</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="ad945-131">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ad945-131">Child elements</span></span><br/>  | <span data-ttu-id="ad945-132">Il sistema non assegna alcun significato all'ordine degli elementi.</span><span class="sxs-lookup"><span data-stu-id="ad945-132">The system assigns no significance to the ordering of the elements.</span></span> <span data-ttu-id="ad945-133">Se i client scelgono di attribuire una certa importanza nell'ordinamento degli elementi, è possibile farlo liberamente.</span><span class="sxs-lookup"><span data-stu-id="ad945-133">If clients choose to ascribe some significance in the ordering of the elements, they are free to do so.</span></span> <br/> <span data-ttu-id="ad945-134">*Proprietà* (uno o più) *valore* (zero o più)</span><span class="sxs-lookup"><span data-stu-id="ad945-134">*Property* (one or more) *Value* (zero or more)</span></span><br/> <span data-ttu-id="ad945-135">oppure</span><span class="sxs-lookup"><span data-stu-id="ad945-135">or</span></span> <br/> <span data-ttu-id="ad945-136">*Valore* *Property* (zero o più) (uno o più)</span><span class="sxs-lookup"><span data-stu-id="ad945-136">*Property* (zero or more) *Value* (one or more)</span></span><br/> |
| <span data-ttu-id="ad945-137">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="ad945-137">This element</span></span><br/>    | <span data-ttu-id="ad945-138">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="ad945-138">No character data is permitted.</span></span><br/> <span data-ttu-id="ad945-139">Sono consentiti elementi figlio duplicati di pari livello.</span><span class="sxs-lookup"><span data-stu-id="ad945-139">Duplicate child Value elements that are siblings are permitted.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="ad945-140">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="ad945-140">Configuration Dependencies</span></span>

<span data-ttu-id="ad945-141">Una proprietà può avere dipendenze di configurazione, tranne quando viene visualizzata all'interno di un elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="ad945-141">A Property may have configuration dependencies, except when it appears within a ParameterDef element.</span></span>

## <a name="element-usage"></a><span data-ttu-id="ad945-142">Utilizzo elementi</span><span class="sxs-lookup"><span data-stu-id="ad945-142">Element Usage</span></span>

<span data-ttu-id="ad945-143">Oltre a essere visualizzati all'interno degli elementi Feature e Option, gli elementi Property possono essere visualizzati a livello di radice delle rispettive tecnologie sottostanti.</span><span class="sxs-lookup"><span data-stu-id="ad945-143">In addition to appearing within Feature and Option elements, Property elements can appear at the root level of the respective underlying technologies.</span></span> <span data-ttu-id="ad945-144">Lo schema di stampa definisce un set di elementi proprietà che possono essere usati per descrivere un dispositivo in modo portatile.</span><span class="sxs-lookup"><span data-stu-id="ad945-144">The Print Schema defines a set of Property elements that can be used to describe a device in a portable manner.</span></span> <span data-ttu-id="ad945-145">Tuttavia, se queste proprietà non sono sufficienti per le proprie esigenze come provider PrintCapabilities, in genere perché il dispositivo supportato presenta aspetti nuovi non previsti dallo schema di stampa, è possibile introdurre elementi della proprietà privata.</span><span class="sxs-lookup"><span data-stu-id="ad945-145">However, if these properties are insufficient to your needs as a PrintCapabilities provider (typically because the device being supported has novel aspects not anticipated by the Print Schema), you may introduce your own private Property elements.</span></span> <span data-ttu-id="ad945-146">È possibile migliorare o elaborare le informazioni fornite da una proprietà pubblica aggiungendo una o più sottoproprietà private come contenuto dell'elemento della proprietà Public.</span><span class="sxs-lookup"><span data-stu-id="ad945-146">You can enhance or elaborate the information provided by a public Property by adding one or more private subproperties as element content of the public Property.</span></span>

<span data-ttu-id="ad945-147">Gli elementi della proprietà vengono definiti tramite un tag di elemento XML, <Property> .</span><span class="sxs-lookup"><span data-stu-id="ad945-147">Property elements are defined by using an XML element tag, <Property>.</span></span> <span data-ttu-id="ad945-148">A ogni proprietà viene assegnato un nome mediante l'attributo Name.</span><span class="sxs-lookup"><span data-stu-id="ad945-148">Each Property is assigned a name by means of its name attribute.</span></span> <span data-ttu-id="ad945-149">Il nome deve essere un QName XML e deve essere conforme alla convenzione dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ad945-149">The name must be an XML QName and must conform to the Namespace Convention.</span></span> <span data-ttu-id="ad945-150">Per informazioni dettagliate, vedere [attributi XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="ad945-150">For details, see [XML Attributes](xml-attributes.md).</span></span> <span data-ttu-id="ad945-151">L'attributo del nome della proprietà e la relativa posizione all'interno della gerarchia degli elementi della proprietà padre (se si tratta di una sottoproprietà) identificano in modo univoco la proprietà all'interno del documento PrintCapabilities o PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="ad945-151">The Property name attribute and its location within the hierarchy of parent Property elements (if it is a subproperty) uniquely identify the Property within the PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="ad945-152">Una proprietà può contenere uno o più elementi value oppure uno o più elementi di proprietà figlio (detti sottoproprietà) o una combinazione di entrambi.</span><span class="sxs-lookup"><span data-stu-id="ad945-152">A Property may contain one or more Value elements, or one or more child Property elements (called subproperties), or a combination of both.</span></span> <span data-ttu-id="ad945-153">Le sottoproprietà sono utili quando la proprietà stessa è costituita da più componenti.</span><span class="sxs-lookup"><span data-stu-id="ad945-153">Subproperties are useful when the Property itself is composed of multiple components.</span></span> <span data-ttu-id="ad945-154">Una proprietà "ConsumableColor", ad esempio, può includere i componenti "C", "M" e "Y".</span><span class="sxs-lookup"><span data-stu-id="ad945-154">For example, a "ConsumableColor" Property might have "C", "M", and "Y" components.</span></span>

## <a name="example"></a><span data-ttu-id="ad945-155">Esempio</span><span class="sxs-lookup"><span data-stu-id="ad945-155">Example</span></span>

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="ad945-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad945-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad945-157">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ad945-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




