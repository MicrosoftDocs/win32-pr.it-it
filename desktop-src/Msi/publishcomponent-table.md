---
description: La tabella PublishComponent associa i componenti elencati nella tabella Component con una stringa di testo qualificatore e un GUID ID categoria.
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: Tabella PublishComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb0edfd811873242629c36257fdce5a80fe9d91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311731"
---
# <a name="publishcomponent-table"></a><span data-ttu-id="8a24f-103">Tabella PublishComponent</span><span class="sxs-lookup"><span data-stu-id="8a24f-103">PublishComponent Table</span></span>

<span data-ttu-id="8a24f-104">La tabella PublishComponent associa i componenti elencati nella [tabella Component](component-table.md) con una stringa di testo qualificatore e un GUID ID categoria.</span><span class="sxs-lookup"><span data-stu-id="8a24f-104">The PublishComponent table associates components listed in the [Component table](component-table.md) with a qualifier text-string and a category ID GUID.</span></span> <span data-ttu-id="8a24f-105">I componenti con funzionalità parallele raggruppate in questo modo vengono definiti componenti qualificati.</span><span class="sxs-lookup"><span data-stu-id="8a24f-105">Components with parallel functionality that have been grouped together in this way are referred to as qualified components.</span></span> <span data-ttu-id="8a24f-106">Vedere [componenti qualificati](qualified-components.md).</span><span class="sxs-lookup"><span data-stu-id="8a24f-106">See [Qualified Components](qualified-components.md).</span></span> <span data-ttu-id="8a24f-107">Questa operazione fornisce al programma di installazione un metodo per il reindirizzamento a livello singolo quando si fa riferimento ai componenti.</span><span class="sxs-lookup"><span data-stu-id="8a24f-107">This provides the installer with a method for single-level indirection when referring to components.</span></span> <span data-ttu-id="8a24f-108">Vedere [uso di componenti qualificati](using-qualified-components.md).</span><span class="sxs-lookup"><span data-stu-id="8a24f-108">See [Using Qualified Components](using-qualified-components.md).</span></span>

<span data-ttu-id="8a24f-109">La tabella PublishComponent include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="8a24f-109">The PublishComponent table has the following columns.</span></span>



| <span data-ttu-id="8a24f-110">Colonna</span><span class="sxs-lookup"><span data-stu-id="8a24f-110">Column</span></span>      | <span data-ttu-id="8a24f-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a24f-111">Type</span></span>                         | <span data-ttu-id="8a24f-112">Chiave</span><span class="sxs-lookup"><span data-stu-id="8a24f-112">Key</span></span> | <span data-ttu-id="8a24f-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="8a24f-113">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="8a24f-114">ComponentId</span><span class="sxs-lookup"><span data-stu-id="8a24f-114">ComponentId</span></span> | [<span data-ttu-id="8a24f-115">GUID</span><span class="sxs-lookup"><span data-stu-id="8a24f-115">GUID</span></span>](guid.md)             | <span data-ttu-id="8a24f-116">S</span><span class="sxs-lookup"><span data-stu-id="8a24f-116">Y</span></span>   | <span data-ttu-id="8a24f-117">N</span><span class="sxs-lookup"><span data-stu-id="8a24f-117">N</span></span>        |
| <span data-ttu-id="8a24f-118">Qualifier</span><span class="sxs-lookup"><span data-stu-id="8a24f-118">Qualifier</span></span>   | [<span data-ttu-id="8a24f-119">Text</span><span class="sxs-lookup"><span data-stu-id="8a24f-119">Text</span></span>](text.md)             | <span data-ttu-id="8a24f-120">S</span><span class="sxs-lookup"><span data-stu-id="8a24f-120">Y</span></span>   | <span data-ttu-id="8a24f-121">N</span><span class="sxs-lookup"><span data-stu-id="8a24f-121">N</span></span>        |
| <span data-ttu-id="8a24f-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="8a24f-122">Component\_</span></span> | [<span data-ttu-id="8a24f-123">Identificatore</span><span class="sxs-lookup"><span data-stu-id="8a24f-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="8a24f-124">S</span><span class="sxs-lookup"><span data-stu-id="8a24f-124">Y</span></span>   | <span data-ttu-id="8a24f-125">N</span><span class="sxs-lookup"><span data-stu-id="8a24f-125">N</span></span>        |
| <span data-ttu-id="8a24f-126">AppData</span><span class="sxs-lookup"><span data-stu-id="8a24f-126">AppData</span></span>     | [<span data-ttu-id="8a24f-127">Text</span><span class="sxs-lookup"><span data-stu-id="8a24f-127">Text</span></span>](text.md)             | <span data-ttu-id="8a24f-128">N</span><span class="sxs-lookup"><span data-stu-id="8a24f-128">N</span></span>   | <span data-ttu-id="8a24f-129">S</span><span class="sxs-lookup"><span data-stu-id="8a24f-129">Y</span></span>        |
| <span data-ttu-id="8a24f-130">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="8a24f-130">Feature\_</span></span>   | [<span data-ttu-id="8a24f-131">Identificatore</span><span class="sxs-lookup"><span data-stu-id="8a24f-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="8a24f-132">N</span><span class="sxs-lookup"><span data-stu-id="8a24f-132">N</span></span>   | <span data-ttu-id="8a24f-133">N</span><span class="sxs-lookup"><span data-stu-id="8a24f-133">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8a24f-134">Colonne</span><span class="sxs-lookup"><span data-stu-id="8a24f-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8a24f-135"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span><span class="sxs-lookup"><span data-stu-id="8a24f-135"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span></span>
</dt> <dd>

<span data-ttu-id="8a24f-136">[GUID](guid.md) di stringa che rappresenta la categoria di componenti raggruppati.</span><span class="sxs-lookup"><span data-stu-id="8a24f-136">A string [GUID](guid.md) that represents the category of components being grouped together.</span></span> <span data-ttu-id="8a24f-137">Si noti che il titolo di questa colonna è fuorviante.</span><span class="sxs-lookup"><span data-stu-id="8a24f-137">Note that this column's title is misleading.</span></span> <span data-ttu-id="8a24f-138">Si tratta del GUID per la categoria di componenti qualificati e non è lo stesso GUID visualizzato nella colonna ComponentId della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8a24f-138">This is the GUID for the category of qualified components and is not the same GUID appearing in the ComponentId column of the [Component table](component-table.md).</span></span> <span data-ttu-id="8a24f-139">Qui si riferisce a un server che fornisce la funzionalità di un componente ai client esterni anziché al componente stesso.</span><span class="sxs-lookup"><span data-stu-id="8a24f-139">Here it refers to a server that provides the functionality of a component to external clients rather than the component itself.</span></span>

</dd> <dt>

<span data-ttu-id="8a24f-140"><span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualificatore</span><span class="sxs-lookup"><span data-stu-id="8a24f-140"><span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualifier</span></span>
</dt> <dd>

<span data-ttu-id="8a24f-141">Stringa di testo che qualifica il valore nella colonna ComponentId.</span><span class="sxs-lookup"><span data-stu-id="8a24f-141">A text string that qualifies the value in the ComponentId column.</span></span> <span data-ttu-id="8a24f-142">Un qualificatore viene utilizzato per distinguere più forme dello stesso componente, ad esempio un componente implementato in più lingue.</span><span class="sxs-lookup"><span data-stu-id="8a24f-142">A qualifier is used to distinguish multiple forms of the same component, such as a component that is implemented in multiple languages.</span></span> <span data-ttu-id="8a24f-143">Queste sono le stringhe di testo qualificatore restituite da [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="8a24f-143">These are the qualifier text-strings returned by [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

</dd> <dt>

<span data-ttu-id="8a24f-144"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="8a24f-144"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="8a24f-145">Chiave esterna nella colonna uno della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8a24f-145">External key into column one of the [Component table](component-table.md).</span></span> <span data-ttu-id="8a24f-146">Questo identificatore fa riferimento al record del componente completo nella tabella dei componenti.</span><span class="sxs-lookup"><span data-stu-id="8a24f-146">This identifier refers to the qualified component's record in the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="8a24f-147"><span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData</span><span class="sxs-lookup"><span data-stu-id="8a24f-147"><span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData</span></span>
</dt> <dd>

<span data-ttu-id="8a24f-148">Testo localizzabile facoltativo che descrive il componente completo di questo record.</span><span class="sxs-lookup"><span data-stu-id="8a24f-148">An optional localizable text describing the qualified component of this record.</span></span> <span data-ttu-id="8a24f-149">La stringa viene comunemente analizzata dall'applicazione e può essere visualizzata all'utente.</span><span class="sxs-lookup"><span data-stu-id="8a24f-149">The string is commonly parsed by the application and can be displayed to the user.</span></span> <span data-ttu-id="8a24f-150">Dovrebbe descrivere il componente completo.</span><span class="sxs-lookup"><span data-stu-id="8a24f-150">It should describe the qualified component.</span></span> <span data-ttu-id="8a24f-151">Questa operazione può essere recuperata con [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="8a24f-151">This can be retrieved with [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

</dd> <dt>

<span data-ttu-id="8a24f-152"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="8a24f-152"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="8a24f-153">Chiave esterna nella colonna uno della [tabella delle funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8a24f-153">External key into column one of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="8a24f-154">Questa è la funzionalità che usa questo componente qualificato.</span><span class="sxs-lookup"><span data-stu-id="8a24f-154">This is the feature using this qualified component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a24f-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a24f-155">Remarks</span></span>

<span data-ttu-id="8a24f-156">Questa tabella viene definita quando viene eseguita l'azione [PublishComponents](publishcomponents-action.md) o [UnpublishComponents](unpublishcomponents-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8a24f-156">This table is referred to when the [PublishComponents action](publishcomponents-action.md) or the [UnpublishComponents action](unpublishcomponents-action.md) is executed.</span></span>

<span data-ttu-id="8a24f-157">Si noti che il nome di questa tabella è fuorviante.</span><span class="sxs-lookup"><span data-stu-id="8a24f-157">Note that the name of this table is misleading.</span></span> <span data-ttu-id="8a24f-158">Questa tabella non è necessaria per creare un annuncio pubblicitario.</span><span class="sxs-lookup"><span data-stu-id="8a24f-158">This table is not required in order to author advertisement.</span></span> <span data-ttu-id="8a24f-159">Per informazioni su come impostare lo stato di installazione dei componenti da pubblicizzare, vedere la colonna attributi della [tabella](component-table.md) dei componenti e della [tabella delle funzionalità](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="8a24f-159">See the Attributes column of the [Component table](component-table.md) and [Feature table](feature-table.md) for information on how to set the installation state of components to advertise.</span></span>

## <a name="validation"></a><span data-ttu-id="8a24f-160">Convalida</span><span class="sxs-lookup"><span data-stu-id="8a24f-160">Validation</span></span>

<dl>

[<span data-ttu-id="8a24f-161">ICE03</span><span class="sxs-lookup"><span data-stu-id="8a24f-161">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8a24f-162">ICE06</span><span class="sxs-lookup"><span data-stu-id="8a24f-162">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8a24f-163">ICE19</span><span class="sxs-lookup"><span data-stu-id="8a24f-163">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="8a24f-164">ICE22</span><span class="sxs-lookup"><span data-stu-id="8a24f-164">ICE22</span></span>](ice22.md)  
[<span data-ttu-id="8a24f-165">ICE32</span><span class="sxs-lookup"><span data-stu-id="8a24f-165">ICE32</span></span>](ice32.md)  
</dl>

 

 



