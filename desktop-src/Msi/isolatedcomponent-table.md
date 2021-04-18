---
description: Ogni record della tabella IsolatedComponent associa il componente specificato nella \_ colonna applicazione componente (in genere un file con estensione exe) con il componente specificato nella \_ colonna condivisa componente (in genere una DLL condivisa).
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: Tabella IsolatedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3e6c5bdba6efc546a36e77fa793c0b397f6d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307261"
---
# <a name="isolatedcomponent-table"></a><span data-ttu-id="8df0d-103">Tabella IsolatedComponent</span><span class="sxs-lookup"><span data-stu-id="8df0d-103">IsolatedComponent Table</span></span>

<span data-ttu-id="8df0d-104">Ogni record della tabella IsolatedComponent associa il componente specificato nella \_ colonna applicazione componente (in genere un file con estensione exe) con il componente specificato nella \_ colonna condivisa componente (in genere una DLL condivisa).</span><span class="sxs-lookup"><span data-stu-id="8df0d-104">Each record of the IsolatedComponent table associates the component specified in the Component\_Application column (commonly an .exe) with the component specified in the Component\_Shared column (commonly a shared DLL).</span></span> <span data-ttu-id="8df0d-105">L' [azione IsolateComponents](isolatecomponents-action.md) installa una copia del componente \_ condiviso in una posizione privata per l'uso da parte \_ dell'applicazione componente.</span><span class="sxs-lookup"><span data-stu-id="8df0d-105">The [IsolateComponents action](isolatecomponents-action.md) installs a copy of Component\_Shared into a private location for use by Component\_Application.</span></span> <span data-ttu-id="8df0d-106">In questo modo l' \_ applicazione componente viene isolata da altre copie di componenti \_ condivisi che possono essere installate in un percorso condiviso nel computer.</span><span class="sxs-lookup"><span data-stu-id="8df0d-106">This isolates the Component\_Application from other copies of Component\_Shared that may be installed to a shared location on the computer.</span></span> <span data-ttu-id="8df0d-107">Vedere [componenti isolati](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="8df0d-107">See [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="8df0d-108">Per collegare un componente \_ condiviso a più \_ applicazioni componente, includere un record separato per ogni coppia nella tabella IsolatedComponents.</span><span class="sxs-lookup"><span data-stu-id="8df0d-108">To link one Component\_Shared to multiple Component\_Application, include a separate record for each pair in the IsolatedComponents table.</span></span> <span data-ttu-id="8df0d-109">Il programma di installazione copia i file di componente \_ condivisi nella directory di ogni \_ applicazione componente installata.</span><span class="sxs-lookup"><span data-stu-id="8df0d-109">The installer copies the files of Component\_Shared into the directory of each Component\_Application that is installed.</span></span>

<span data-ttu-id="8df0d-110">La tabella IsolatedComponent include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="8df0d-110">The IsolatedComponent table has the following columns.</span></span>



| <span data-ttu-id="8df0d-111">Colonna</span><span class="sxs-lookup"><span data-stu-id="8df0d-111">Column</span></span>                 | <span data-ttu-id="8df0d-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="8df0d-112">Type</span></span>                         | <span data-ttu-id="8df0d-113">Chiave</span><span class="sxs-lookup"><span data-stu-id="8df0d-113">Key</span></span> | <span data-ttu-id="8df0d-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="8df0d-114">Nullable</span></span> |
|------------------------|------------------------------|-----|----------|
| <span data-ttu-id="8df0d-115">Componente \_ condiviso</span><span class="sxs-lookup"><span data-stu-id="8df0d-115">Component\_Shared</span></span>      | [<span data-ttu-id="8df0d-116">Identificatore</span><span class="sxs-lookup"><span data-stu-id="8df0d-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="8df0d-117">S</span><span class="sxs-lookup"><span data-stu-id="8df0d-117">Y</span></span>   | <span data-ttu-id="8df0d-118">N</span><span class="sxs-lookup"><span data-stu-id="8df0d-118">N</span></span>        |
| <span data-ttu-id="8df0d-119">\_Applicazione componente</span><span class="sxs-lookup"><span data-stu-id="8df0d-119">Component\_Application</span></span> | [<span data-ttu-id="8df0d-120">Identificatore</span><span class="sxs-lookup"><span data-stu-id="8df0d-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="8df0d-121">S</span><span class="sxs-lookup"><span data-stu-id="8df0d-121">Y</span></span>   | <span data-ttu-id="8df0d-122">N</span><span class="sxs-lookup"><span data-stu-id="8df0d-122">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8df0d-123">Colonne</span><span class="sxs-lookup"><span data-stu-id="8df0d-123">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8df0d-124"><span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Componente \_ condiviso</span><span class="sxs-lookup"><span data-stu-id="8df0d-124"><span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Component\_Shared</span></span>
</dt> <dd>

<span data-ttu-id="8df0d-125">Chiave esterna nella [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8df0d-125">Foreign key into the [Component table](component-table.md).</span></span> <span data-ttu-id="8df0d-126">Componente che contiene il file condiviso, in genere una DLL.</span><span class="sxs-lookup"><span data-stu-id="8df0d-126">The component that contains the shared file, usually a DLL.</span></span> <span data-ttu-id="8df0d-127">La DLL deve essere il file di chiave per questo componente.</span><span class="sxs-lookup"><span data-stu-id="8df0d-127">The DLL should be the key file for this component.</span></span> <span data-ttu-id="8df0d-128">Deve trattarsi di un componente diverso da quello elencato nella \_ colonna applicazione componente.</span><span class="sxs-lookup"><span data-stu-id="8df0d-128">This must be a different component than listed in the Component\_Application column.</span></span>

<span data-ttu-id="8df0d-129">Il componente condiviso controlla la registrazione per tutte le copie isolate del componente ed è necessario impostare il flag **msidbComponentAttributesSharedDllRefCount** nella colonna attributi della tabella dei componenti.</span><span class="sxs-lookup"><span data-stu-id="8df0d-129">The shared component controls the registration for all the isolated copies of the component and must have the **msidbComponentAttributesSharedDllRefCount** flag set in the Attributes column of the Component table.</span></span> <span data-ttu-id="8df0d-130">Ciò garantisce che il programma di installazione possa gestire la durata del componente condiviso.</span><span class="sxs-lookup"><span data-stu-id="8df0d-130">This ensures that the installer can manage the life of the shared component.</span></span>

</dd> <dt>

<span data-ttu-id="8df0d-131"><span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>\_Applicazione componente</span><span class="sxs-lookup"><span data-stu-id="8df0d-131"><span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Component\_Application</span></span>
</dt> <dd>

<span data-ttu-id="8df0d-132">Chiave esterna nella [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8df0d-132">Foreign key into the [Component table](component-table.md).</span></span> <span data-ttu-id="8df0d-133">Componente che contiene il file con estensione exe che carica il file condiviso.</span><span class="sxs-lookup"><span data-stu-id="8df0d-133">The component that contains the .exe which loads the shared file.</span></span> <span data-ttu-id="8df0d-134">Il file con estensione exe deve essere il file di chiave per questo componente.</span><span class="sxs-lookup"><span data-stu-id="8df0d-134">The .exe should be the key file for this component.</span></span> <span data-ttu-id="8df0d-135">Deve trattarsi di un componente diverso da quello elencato nella \_ colonna Shared Component.</span><span class="sxs-lookup"><span data-stu-id="8df0d-135">This must be a different component than listed in the Component\_Shared column.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="8df0d-136">Convalida</span><span class="sxs-lookup"><span data-stu-id="8df0d-136">Validation</span></span>

<dl>

[<span data-ttu-id="8df0d-137">ICE03</span><span class="sxs-lookup"><span data-stu-id="8df0d-137">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8df0d-138">ICE06</span><span class="sxs-lookup"><span data-stu-id="8df0d-138">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8df0d-139">ICE32</span><span class="sxs-lookup"><span data-stu-id="8df0d-139">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="8df0d-140">ICE62</span><span class="sxs-lookup"><span data-stu-id="8df0d-140">ICE62</span></span>](ice62.md)  
[<span data-ttu-id="8df0d-141">ICE66</span><span class="sxs-lookup"><span data-stu-id="8df0d-141">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="8df0d-142">ICE97</span><span class="sxs-lookup"><span data-stu-id="8df0d-142">ICE97</span></span>](ice97.md)  
</dl>

 

 



