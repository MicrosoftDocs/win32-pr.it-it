---
description: Per consentire a un client di costruire un PrintTicket, il documento PrintCapabilities deve fornire le proprietà delle istanze feature e option nella funzionalità.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Istanze di proprietà importanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4691b73b1206ee092c171b213a3815925b7f53c6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409124"
---
# <a name="important-property-instances"></a><span data-ttu-id="07a0d-103">Istanze di proprietà importanti</span><span class="sxs-lookup"><span data-stu-id="07a0d-103">Important Property Instances</span></span>

<span data-ttu-id="07a0d-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="07a0d-104">This topic is not current.</span></span> <span data-ttu-id="07a0d-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="07a0d-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="07a0d-106">Per consentire a un client PrintCapabilities di costruire un PrintTicket ragionevole, il documento PrintCapabilities deve fornire determinate proprietà delle istanze di Feature e delle istanze Option all'interno di Feature.</span><span class="sxs-lookup"><span data-stu-id="07a0d-106">In order for a PrintCapabilities client to be able to construct a reasonable PrintTicket, the PrintCapabilities document must provide certain properties of Feature instances as well as Option instances within the Feature.</span></span> <span data-ttu-id="07a0d-107">Un modulo di interfaccia utente generica richiede tali informazioni per costruire un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="07a0d-107">A generic user interface (UI) module requires such information to construct a UI.</span></span> <span data-ttu-id="07a0d-108">A sua volta, è necessario che le parole chiave dello schema di stampa definiranno alcune istanze di Proprietà che vengono visualizzate come elementi figlio degli elementi Feature e Option.</span><span class="sxs-lookup"><span data-stu-id="07a0d-108">This in turn requires that the Print Schema Keywords define a few Property instances that appear as children of Feature and Option elements.</span></span>

<span data-ttu-id="07a0d-109">Gli elementi della funzionalità possono contenere la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="07a0d-109">Feature elements can contain the following Property.</span></span>



| <span data-ttu-id="07a0d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07a0d-110">Property</span></span>                  | <span data-ttu-id="07a0d-111">Valori</span><span class="sxs-lookup"><span data-stu-id="07a0d-111">Values</span></span>                                 | <span data-ttu-id="07a0d-112">Scopo</span><span class="sxs-lookup"><span data-stu-id="07a0d-112">Purpose</span></span>                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07a0d-113">Tipo di selezione</span><span class="sxs-lookup"><span data-stu-id="07a0d-113">SelectionType</span></span> <br/> | <span data-ttu-id="07a0d-114">PickOne</span><span class="sxs-lookup"><span data-stu-id="07a0d-114">PickOne</span></span><br/> <span data-ttu-id="07a0d-115">PickMany</span><span class="sxs-lookup"><span data-stu-id="07a0d-115">PickMany</span></span><br/> | <span data-ttu-id="07a0d-116">Specifica il numero di opzioni che è possibile selezionare per questa funzionalità in un determinato momento, una (PickOne) o più di una (PickMany).</span><span class="sxs-lookup"><span data-stu-id="07a0d-116">Specifies the number of Options that can be selected for this Feature at a given time, either one (PickOne), or more than one (PickMany).</span></span> <span data-ttu-id="07a0d-117">Il client può usare queste informazioni per costruire un PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="07a0d-117">The client can use this information to construct a PrintTicket.</span></span> <span data-ttu-id="07a0d-118">Queste informazioni influiscono sul comportamento dell'interfaccia utente e sulla convalida PrintTicket da parte del provider.</span><span class="sxs-lookup"><span data-stu-id="07a0d-118">This information affects UI behavior, as well as PrintTicket validation by the provider.</span></span><br/> |



 

<span data-ttu-id="07a0d-119">Gli elementi Option possono contenere la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="07a0d-119">Option elements can contain the following Property.</span></span>



| <span data-ttu-id="07a0d-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07a0d-120">Property</span></span>                   | <span data-ttu-id="07a0d-121">Valori</span><span class="sxs-lookup"><span data-stu-id="07a0d-121">Values</span></span>                           | <span data-ttu-id="07a0d-122">Scopo</span><span class="sxs-lookup"><span data-stu-id="07a0d-122">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07a0d-123">IdentityOption</span><span class="sxs-lookup"><span data-stu-id="07a0d-123">IdentityOption</span></span> <br/> | <span data-ttu-id="07a0d-124">Vero</span><span class="sxs-lookup"><span data-stu-id="07a0d-124">True</span></span><br/> <span data-ttu-id="07a0d-125">Falso</span><span class="sxs-lookup"><span data-stu-id="07a0d-125">False</span></span><br/> | <span data-ttu-id="07a0d-126">La selezione della proprietà IdentityOption viene interpretata come "disabilita questa funzionalità".</span><span class="sxs-lookup"><span data-stu-id="07a0d-126">Selecting the IdentityOption Property is interpreted to mean "disable this feature".</span></span> <span data-ttu-id="07a0d-127">Un elemento Feature che contiene una proprietà SelectionType il cui valore è PickMany deve contenere anche un elemento Option con una proprietà IdentityOption.</span><span class="sxs-lookup"><span data-stu-id="07a0d-127">A Feature that contains a SelectionType Property whose value is PickMany must also contain an Option that has an IdentityOption Property.</span></span> <span data-ttu-id="07a0d-128">Il codice dell'interfaccia utente (o il client che costruisce un PrintTicket) deve deselezionare qualsiasi altra opzione se è selezionata la proprietà IdentityOption.</span><span class="sxs-lookup"><span data-stu-id="07a0d-128">The UI code (or client constructing a PrintTicket) must deselect any other Option if the IdentityOption Property is selected.</span></span><br/> |



 

<span data-ttu-id="07a0d-129">Gli elementi Feature, Option e ParameterDef possono contenere la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="07a0d-129">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="07a0d-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07a0d-130">Property</span></span>              | <span data-ttu-id="07a0d-131">Valori</span><span class="sxs-lookup"><span data-stu-id="07a0d-131">Values</span></span>                          | <span data-ttu-id="07a0d-132">Scopo</span><span class="sxs-lookup"><span data-stu-id="07a0d-132">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07a0d-133">DisplayUI</span><span class="sxs-lookup"><span data-stu-id="07a0d-133">DisplayUI</span></span> <br/> | <span data-ttu-id="07a0d-134">Mostra</span><span class="sxs-lookup"><span data-stu-id="07a0d-134">Show</span></span><br/> <span data-ttu-id="07a0d-135">Nascondi</span><span class="sxs-lookup"><span data-stu-id="07a0d-135">Hide</span></span><br/> | <span data-ttu-id="07a0d-136">Specifica se l'elemento padre deve essere visualizzato nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="07a0d-136">Specifies whether the parent element should be displayed in the UI.</span></span> <span data-ttu-id="07a0d-137">Show indica che l'elemento deve essere visualizzato nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="07a0d-137">Show indicates that the element should be displayed in the UI.</span></span> <span data-ttu-id="07a0d-138">Nascondi indica che l'elemento non deve essere visualizzato nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="07a0d-138">Hide indicates that the element should not be displayed in the UI.</span></span> <span data-ttu-id="07a0d-139">Se questa proprietà non è definita per un elemento, l'interpretazione predefinita è Show, ovvero l'elemento viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="07a0d-139">If this Property is not defined for an element, the default interpretation is Show, meaning that the element is displayed.</span></span><br/> |



 

<span data-ttu-id="07a0d-140">Gli elementi Feature, Option e ParameterDef possono contenere la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="07a0d-140">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="07a0d-141">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07a0d-141">Property</span></span>                | <span data-ttu-id="07a0d-142">valore</span><span class="sxs-lookup"><span data-stu-id="07a0d-142">Value</span></span>             | <span data-ttu-id="07a0d-143">Scopo</span><span class="sxs-lookup"><span data-stu-id="07a0d-143">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07a0d-144">DisplayName</span><span class="sxs-lookup"><span data-stu-id="07a0d-144">DisplayName</span></span> <br/> | <span data-ttu-id="07a0d-145">Stringa</span><span class="sxs-lookup"><span data-stu-id="07a0d-145">String</span></span><br/> | <span data-ttu-id="07a0d-146">Specifica la stringa di visualizzazione per l'elemento padre, eseguendo l'override del nome visualizzato predefinito.</span><span class="sxs-lookup"><span data-stu-id="07a0d-146">Specifies the display string for the parent element, overriding the default display name.</span></span> <span data-ttu-id="07a0d-147">Può essere usato dai provider PrintCapabilities per presentare un nome visualizzato localizzato e descrittivo.</span><span class="sxs-lookup"><span data-stu-id="07a0d-147">Can be used by PrintCapabilities providers to present a localized and user friendly display name.</span></span> <span data-ttu-id="07a0d-148">Il valore predefinito del nome visualizzato è l'attributo name per l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="07a0d-148">The default display name value is the name attribute for the parent element.</span></span> <br/> <span data-ttu-id="07a0d-149">Nel caso degli elementi Option, se non viene specificato l'attributo name, la proprietà DisplayName deve essere presente.</span><span class="sxs-lookup"><span data-stu-id="07a0d-149">In the case of Option elements, if the name attribute is not provided, then the DisplayName Property must be present.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="07a0d-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="07a0d-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07a0d-151">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="07a0d-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




