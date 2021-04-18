---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Istanze di proprietà importanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad3f58c099913b129ee7be0337ecab3343a5e5e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320972"
---
# <a name="important-property-instances"></a><span data-ttu-id="c1d9f-104">Istanze di proprietà importanti</span><span class="sxs-lookup"><span data-stu-id="c1d9f-104">Important Property Instances</span></span>

<span data-ttu-id="c1d9f-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-105">This topic is not current.</span></span> <span data-ttu-id="c1d9f-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c1d9f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c1d9f-107">Affinché un client PrintCapabilities sia in grado di costruire un oggetto PrintTicket ragionevole, è necessario che il documento PrintCapabilities fornisca determinate proprietà delle istanze delle funzionalità, nonché le istanze delle opzioni all'interno della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-107">In order for a PrintCapabilities client to be able to construct a reasonable PrintTicket, the PrintCapabilities document must provide certain properties of Feature instances as well as Option instances within the Feature.</span></span> <span data-ttu-id="c1d9f-108">Un modulo dell'interfaccia utente generico richiede tali informazioni per costruire un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-108">A generic user interface (UI) module requires such information to construct a UI.</span></span> <span data-ttu-id="c1d9f-109">Questa operazione richiede a sua volta che le parole chiave dello schema di stampa definiscano alcune istanze di proprietà che vengono visualizzate come elementi figlio degli elementi Feature e Option.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-109">This in turn requires that the Print Schema Keywords define a few Property instances that appear as children of Feature and Option elements.</span></span>

<span data-ttu-id="c1d9f-110">Gli elementi Feature possono contenere la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-110">Feature elements can contain the following Property.</span></span>



| <span data-ttu-id="c1d9f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c1d9f-111">Property</span></span>                  | <span data-ttu-id="c1d9f-112">Valori</span><span class="sxs-lookup"><span data-stu-id="c1d9f-112">Values</span></span>                                 | <span data-ttu-id="c1d9f-113">Scopo</span><span class="sxs-lookup"><span data-stu-id="c1d9f-113">Purpose</span></span>                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d9f-114">SelectionType</span><span class="sxs-lookup"><span data-stu-id="c1d9f-114">SelectionType</span></span> <br/> | <span data-ttu-id="c1d9f-115">PickOne</span><span class="sxs-lookup"><span data-stu-id="c1d9f-115">PickOne</span></span><br/> <span data-ttu-id="c1d9f-116">PickMany</span><span class="sxs-lookup"><span data-stu-id="c1d9f-116">PickMany</span></span><br/> | <span data-ttu-id="c1d9f-117">Specifica il numero di opzioni che è possibile selezionare per questa funzionalità in un determinato momento, ovvero una (PickOne) o più di una (PickMany).</span><span class="sxs-lookup"><span data-stu-id="c1d9f-117">Specifies the number of Options that can be selected for this Feature at a given time, either one (PickOne), or more than one (PickMany).</span></span> <span data-ttu-id="c1d9f-118">Il client può utilizzare queste informazioni per costruire un oggetto PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-118">The client can use this information to construct a PrintTicket.</span></span> <span data-ttu-id="c1d9f-119">Queste informazioni influiscono sul comportamento dell'interfaccia utente e sulla convalida PrintTicket da parte del provider.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-119">This information affects UI behavior, as well as PrintTicket validation by the provider.</span></span><br/> |



 

<span data-ttu-id="c1d9f-120">Gli elementi option possono contenere la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-120">Option elements can contain the following Property.</span></span>



| <span data-ttu-id="c1d9f-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c1d9f-121">Property</span></span>                   | <span data-ttu-id="c1d9f-122">Valori</span><span class="sxs-lookup"><span data-stu-id="c1d9f-122">Values</span></span>                           | <span data-ttu-id="c1d9f-123">Scopo</span><span class="sxs-lookup"><span data-stu-id="c1d9f-123">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d9f-124">IdentityOption</span><span class="sxs-lookup"><span data-stu-id="c1d9f-124">IdentityOption</span></span> <br/> | <span data-ttu-id="c1d9f-125">Vero</span><span class="sxs-lookup"><span data-stu-id="c1d9f-125">True</span></span><br/> <span data-ttu-id="c1d9f-126">Falso</span><span class="sxs-lookup"><span data-stu-id="c1d9f-126">False</span></span><br/> | <span data-ttu-id="c1d9f-127">La selezione della proprietà IdentityOption viene interpretata in modo da indicare che la funzionalità è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-127">Selecting the IdentityOption Property is interpreted to mean "disable this feature".</span></span> <span data-ttu-id="c1d9f-128">Una funzionalità che contiene una proprietà SelectionType il cui valore è PickMany deve contenere anche un'opzione con una proprietà IdentityOption.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-128">A Feature that contains a SelectionType Property whose value is PickMany must also contain an Option that has an IdentityOption Property.</span></span> <span data-ttu-id="c1d9f-129">Il codice dell'interfaccia utente (o il client che costruisce un oggetto PrintTicket) deve deselezionare qualsiasi altra opzione se è selezionata la proprietà IdentityOption.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-129">The UI code (or client constructing a PrintTicket) must deselect any other Option if the IdentityOption Property is selected.</span></span><br/> |



 

<span data-ttu-id="c1d9f-130">Gli elementi Feature, Option e ParameterDef possono contenere la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-130">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="c1d9f-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c1d9f-131">Property</span></span>              | <span data-ttu-id="c1d9f-132">Valori</span><span class="sxs-lookup"><span data-stu-id="c1d9f-132">Values</span></span>                          | <span data-ttu-id="c1d9f-133">Scopo</span><span class="sxs-lookup"><span data-stu-id="c1d9f-133">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d9f-134">DisplayUI</span><span class="sxs-lookup"><span data-stu-id="c1d9f-134">DisplayUI</span></span> <br/> | <span data-ttu-id="c1d9f-135">Mostra</span><span class="sxs-lookup"><span data-stu-id="c1d9f-135">Show</span></span><br/> <span data-ttu-id="c1d9f-136">Nascondi</span><span class="sxs-lookup"><span data-stu-id="c1d9f-136">Hide</span></span><br/> | <span data-ttu-id="c1d9f-137">Specifica se l'elemento padre deve essere visualizzato nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-137">Specifies whether the parent element should be displayed in the UI.</span></span> <span data-ttu-id="c1d9f-138">Mostra indica che l'elemento deve essere visualizzato nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-138">Show indicates that the element should be displayed in the UI.</span></span> <span data-ttu-id="c1d9f-139">Hide indica che l'elemento non deve essere visualizzato nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-139">Hide indicates that the element should not be displayed in the UI.</span></span> <span data-ttu-id="c1d9f-140">Se questa proprietà non è definita per un elemento, l'interpretazione predefinita è Show, ovvero viene visualizzato l'elemento.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-140">If this Property is not defined for an element, the default interpretation is Show, meaning that the element is displayed.</span></span><br/> |



 

<span data-ttu-id="c1d9f-141">Gli elementi Feature, Option e ParameterDef possono contenere la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-141">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="c1d9f-142">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c1d9f-142">Property</span></span>                | <span data-ttu-id="c1d9f-143">valore</span><span class="sxs-lookup"><span data-stu-id="c1d9f-143">Value</span></span>             | <span data-ttu-id="c1d9f-144">Scopo</span><span class="sxs-lookup"><span data-stu-id="c1d9f-144">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d9f-145">DisplayName</span><span class="sxs-lookup"><span data-stu-id="c1d9f-145">DisplayName</span></span> <br/> | <span data-ttu-id="c1d9f-146">string</span><span class="sxs-lookup"><span data-stu-id="c1d9f-146">String</span></span><br/> | <span data-ttu-id="c1d9f-147">Specifica la stringa di visualizzazione per l'elemento padre, eseguendo l'override del nome visualizzato predefinito.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-147">Specifies the display string for the parent element, overriding the default display name.</span></span> <span data-ttu-id="c1d9f-148">Può essere utilizzato dai provider PrintCapabilities per presentare un nome visualizzato localizzato e descrittivo dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-148">Can be used by PrintCapabilities providers to present a localized and user friendly display name.</span></span> <span data-ttu-id="c1d9f-149">Il valore predefinito del nome visualizzato è l'attributo Name dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-149">The default display name value is the name attribute for the parent element.</span></span> <br/> <span data-ttu-id="c1d9f-150">Nel caso di elementi option, se l'attributo name non viene specificato, è necessario che la proprietà DisplayName sia presente.</span><span class="sxs-lookup"><span data-stu-id="c1d9f-150">In the case of Option elements, if the name attribute is not provided, then the DisplayName Property must be present.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c1d9f-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c1d9f-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1d9f-152">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="c1d9f-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




