---
description: La tabella ModuleComponents contiene un elenco dei componenti trovati nel modulo merge.
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: Tabella ModuleComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea2f47418b0387c7fa9d289d156fb0369f53adf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316746"
---
# <a name="modulecomponents-table"></a><span data-ttu-id="0649f-103">Tabella ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="0649f-103">ModuleComponents Table</span></span>

<span data-ttu-id="0649f-104">La tabella ModuleComponents contiene un elenco dei componenti trovati nel modulo merge.</span><span class="sxs-lookup"><span data-stu-id="0649f-104">The ModuleComponents table contains a list of the components found in the merge module.</span></span>

<span data-ttu-id="0649f-105">La tabella ModuleComponents include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="0649f-105">The ModuleComponents table has the following columns.</span></span>



| <span data-ttu-id="0649f-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="0649f-106">Column</span></span>    | <span data-ttu-id="0649f-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="0649f-107">Type</span></span>                         | <span data-ttu-id="0649f-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="0649f-108">Key</span></span> | <span data-ttu-id="0649f-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="0649f-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="0649f-110">Componente</span><span class="sxs-lookup"><span data-stu-id="0649f-110">Component</span></span> | [<span data-ttu-id="0649f-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="0649f-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="0649f-112">S</span><span class="sxs-lookup"><span data-stu-id="0649f-112">Y</span></span>   | <span data-ttu-id="0649f-113">N</span><span class="sxs-lookup"><span data-stu-id="0649f-113">N</span></span>        |
| <span data-ttu-id="0649f-114">ModuleID</span><span class="sxs-lookup"><span data-stu-id="0649f-114">ModuleID</span></span>  | [<span data-ttu-id="0649f-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="0649f-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="0649f-116">S</span><span class="sxs-lookup"><span data-stu-id="0649f-116">Y</span></span>   | <span data-ttu-id="0649f-117">N</span><span class="sxs-lookup"><span data-stu-id="0649f-117">N</span></span>        |
| <span data-ttu-id="0649f-118">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="0649f-118">Language</span></span>  | [<span data-ttu-id="0649f-119">Integer</span><span class="sxs-lookup"><span data-stu-id="0649f-119">Integer</span></span>](integer.md)       | <span data-ttu-id="0649f-120">S</span><span class="sxs-lookup"><span data-stu-id="0649f-120">Y</span></span>   | <span data-ttu-id="0649f-121">N</span><span class="sxs-lookup"><span data-stu-id="0649f-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0649f-122">Colonne</span><span class="sxs-lookup"><span data-stu-id="0649f-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0649f-123"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Componente</span><span class="sxs-lookup"><span data-stu-id="0649f-123"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Component</span></span>
</dt> <dd>

<span data-ttu-id="0649f-124">Identificatore che fa riferimento a un componente nel modulo merge.</span><span class="sxs-lookup"><span data-stu-id="0649f-124">An identifier referring to a component in the merge module.</span></span> <span data-ttu-id="0649f-125">La colonna Component è una chiave esterna della [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="0649f-125">The Component column is a foreign key to the [Component table](component-table.md).</span></span> <span data-ttu-id="0649f-126">La voce nella colonna componente deve seguire la convenzione di denominazione per la [denominazione delle chiavi primarie nei database del modulo merge](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="0649f-126">The entry in the Component column must follow the naming convention in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="0649f-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="0649f-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="0649f-128">Identificatore per il modulo unione.</span><span class="sxs-lookup"><span data-stu-id="0649f-128">The identifier for the merge module.</span></span> <span data-ttu-id="0649f-129">Si tratta di una chiave esterna per la [tabella ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="0649f-129">This is a foreign key to the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="0649f-130"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Linguaggio</span><span class="sxs-lookup"><span data-stu-id="0649f-130"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="0649f-131">L'identificatore della lingua descrive la lingua predefinita per il modulo unione.</span><span class="sxs-lookup"><span data-stu-id="0649f-131">The Language identifier describes the default language for the merge module.</span></span> <span data-ttu-id="0649f-132">L'identificatore di lingua è in formato decimale, ad esempio l'inglese (Stati Uniti) è 1033.</span><span class="sxs-lookup"><span data-stu-id="0649f-132">The language identifier is in decimal format, for example, U.S. English is 1033.</span></span> <span data-ttu-id="0649f-133">Chiave esterna per la [tabella ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="0649f-133">Foreign key to the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0649f-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="0649f-134">Remarks</span></span>

<span data-ttu-id="0649f-135">Le trasformazioni del linguaggio devono essere in grado di aggiornare questa tabella se il modulo merge supporta più lingue.</span><span class="sxs-lookup"><span data-stu-id="0649f-135">Language transforms must be able to update this table if the merge module supports multiple languages.</span></span>

 

 



