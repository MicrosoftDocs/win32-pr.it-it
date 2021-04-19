---
description: L'oggetto ConfigurableItem rappresenta una singola riga della tabella ModuleConfiguration.
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: Oggetto ConfigurableItem (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem
- IMsmConfigurableItem
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4436be457adcca37ba40f15bbe0ecd6b0445fb2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332625"
---
# <a name="configurableitem-object"></a><span data-ttu-id="3fbf5-103">Oggetto ConfigurableItem</span><span class="sxs-lookup"><span data-stu-id="3fbf5-103">ConfigurableItem object</span></span>

<span data-ttu-id="3fbf5-104">L' **oggetto ConfigurableItem** rappresenta una singola riga della [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="3fbf5-104">The **ConfigurableItem object** represents a single row from the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="3fbf5-105">Si tratta di un singolo "attributo" configurabile del modulo.</span><span class="sxs-lookup"><span data-stu-id="3fbf5-105">This is a single configurable "attribute" from the module.</span></span> <span data-ttu-id="3fbf5-106">L'interfaccia è costituita da proprietà di sola lettura, una per ogni colonna nella tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3fbf5-106">The interface consists read-only properties, one for each column in the ModuleConfiguration table.</span></span> <span data-ttu-id="3fbf5-107">La definizione dell'interfaccia è la seguente.</span><span class="sxs-lookup"><span data-stu-id="3fbf5-107">The Interface definition is as follows.</span></span>

## <a name="members"></a><span data-ttu-id="3fbf5-108">Membri</span><span class="sxs-lookup"><span data-stu-id="3fbf5-108">Members</span></span>

<span data-ttu-id="3fbf5-109">L'oggetto **ConfigurableItem** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3fbf5-109">The **ConfigurableItem** object has these types of members:</span></span>

-   [<span data-ttu-id="3fbf5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3fbf5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3fbf5-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3fbf5-111">Properties</span></span>

<span data-ttu-id="3fbf5-112">L'oggetto **ConfigurableItem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3fbf5-112">The **ConfigurableItem** object has these properties.</span></span>



| <span data-ttu-id="3fbf5-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3fbf5-113">Property</span></span>                                                         | <span data-ttu-id="3fbf5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fbf5-114">Description</span></span>                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fbf5-115">**Attributi**</span><span class="sxs-lookup"><span data-stu-id="3fbf5-115">**Attributes**</span></span>](configurableitem-attributes.md)<br/>     | <span data-ttu-id="3fbf5-116">Restituisce il valore nel campo attributi del record di questo oggetto nella tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3fbf5-116">Returns the value in the Attributes field of this object's record in the ModuleConfiguration table.</span></span><br/>                            |
| [<span data-ttu-id="3fbf5-117">**Context**</span><span class="sxs-lookup"><span data-stu-id="3fbf5-117">**Context**</span></span>](configurableitem-context.md)<br/>           | <span data-ttu-id="3fbf5-118">Restituisce il valore nel campo di contesto del record di questo oggetto nella tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3fbf5-118">Returns the value in the Context field of this object's record in the ModuleConfiguration table.</span></span><br/>                               |
| [<span data-ttu-id="3fbf5-119">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="3fbf5-119">**DefaultValue**</span></span>](configurableitem-defaultvalue.md)<br/> | <span data-ttu-id="3fbf5-120">Restituisce il valore nel campo DefaultValue del record di questo oggetto nella tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3fbf5-120">Returns the value in the DefaultValue field of this object's record in the ModuleConfiguration table.</span></span><br/>                          |
| [<span data-ttu-id="3fbf5-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="3fbf5-121">**Description**</span></span>](configurableitem-description.md)<br/>   | <span data-ttu-id="3fbf5-122">Restituisce il valore nel campo Descrizione del record di questo oggetto nella tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3fbf5-122">Returns the value in the Description field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="3fbf5-123">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="3fbf5-123">**DisplayName**</span></span>](configurableitem-displayname.md)<br/>   | <span data-ttu-id="3fbf5-124">Restituisce il valore nel campo DisplayName del record di questo oggetto nella tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3fbf5-124">Returns the value in the DisplayName field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="3fbf5-125">**Formato**</span><span class="sxs-lookup"><span data-stu-id="3fbf5-125">**Format**</span></span>](configurableitem-format.md)<br/>             | <span data-ttu-id="3fbf5-126">Restituisce il valore nel campo formato del record di questo oggetto nella tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3fbf5-126">Returns the value in the Format field of this object's record in the ModuleConfiguration table.</span></span><br/>                                |
| [<span data-ttu-id="3fbf5-127">**HelpKeyword**</span><span class="sxs-lookup"><span data-stu-id="3fbf5-127">**HelpKeyword**</span></span>](configurableitem-helpkeyword.md)<br/>   | <span data-ttu-id="3fbf5-128">Restituisce il valore nel campo HelpKeyword del record di questo oggetto nella tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3fbf5-128">Returns the value in the HelpKeyword field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="3fbf5-129">**HelpLocation**</span><span class="sxs-lookup"><span data-stu-id="3fbf5-129">**HelpLocation**</span></span>](configurableitem-helplocation.md)<br/> | <span data-ttu-id="3fbf5-130">Restituisce il valore nel campo HelpLocation del record di questo oggetto nella tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3fbf5-130">Returns the value in the HelpLocation field of this object's record in the ModuleConfiguration table.</span></span><br/>                          |
| [<span data-ttu-id="3fbf5-131">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3fbf5-131">**Name**</span></span>](configurableitem-name.md)<br/>                 | <span data-ttu-id="3fbf5-132">Restituisce il valore nel campo nome del record di questo oggetto nella [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="3fbf5-132">Returns the value in the Name field of this object's record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span><br/> |
| [<span data-ttu-id="3fbf5-133">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3fbf5-133">**Type**</span></span>](configurableitem-type.md)<br/>                 | <span data-ttu-id="3fbf5-134">Restituisce il valore nel campo tipo del record di questo oggetto nella tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3fbf5-134">Returns the value in the Type field of this object's record in the ModuleConfiguration table.</span></span><br/>                                  |



 

## <a name="c"></a><span data-ttu-id="3fbf5-135">C++</span><span class="sxs-lookup"><span data-stu-id="3fbf5-135">C++</span></span>

<span data-ttu-id="3fbf5-136">interfaccia **IMsmConfigurableItem: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="3fbf5-136">interface **IMsmConfigurableItem : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="3fbf5-137">ID interfaccia</span><span class="sxs-lookup"><span data-stu-id="3fbf5-137">Interface ID</span></span>



| <span data-ttu-id="3fbf5-138">Costante</span><span class="sxs-lookup"><span data-stu-id="3fbf5-138">Constant</span></span>                      | <span data-ttu-id="3fbf5-139">Valore</span><span class="sxs-lookup"><span data-stu-id="3fbf5-139">Value</span></span>                                  |
|-------------------------------|----------------------------------------|
| <span data-ttu-id="3fbf5-140">**\_IMSMCONFIGURABLEITEM IID**</span><span class="sxs-lookup"><span data-stu-id="3fbf5-140">**IID\_IMsmConfigurableItem**</span></span> | <span data-ttu-id="3fbf5-141">{4D6E6284-D21D-401E-84F6-909E00B50F71}</span><span class="sxs-lookup"><span data-stu-id="3fbf5-141">{4D6E6284-D21D-401E-84F6-909E00B50F71}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="3fbf5-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fbf5-142">Requirements</span></span>



| <span data-ttu-id="3fbf5-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fbf5-143">Requirement</span></span> | <span data-ttu-id="3fbf5-144">Valore</span><span class="sxs-lookup"><span data-stu-id="3fbf5-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fbf5-145">Versione</span><span class="sxs-lookup"><span data-stu-id="3fbf5-145">Version</span></span><br/> | <span data-ttu-id="3fbf5-146">Mergemod.dll 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3fbf5-146">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="3fbf5-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fbf5-147">Header</span></span><br/>  | <dl> <span data-ttu-id="3fbf5-148"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fbf5-148"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="3fbf5-149">DLL</span><span class="sxs-lookup"><span data-stu-id="3fbf5-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="3fbf5-150"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fbf5-150"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




