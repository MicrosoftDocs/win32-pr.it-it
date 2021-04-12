---
description: La tabella CreateFolder contiene riferimenti a cartelle che devono essere create in modo esplicito per un determinato componente.
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: Tabella CreateFolder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc286b32b48e0db9e5b991ab10af663c51538bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232681"
---
# <a name="createfolder-table"></a><span data-ttu-id="d291e-103">Tabella CreateFolder</span><span class="sxs-lookup"><span data-stu-id="d291e-103">CreateFolder Table</span></span>

<span data-ttu-id="d291e-104">La tabella CreateFolder contiene riferimenti a cartelle che devono essere create in modo esplicito per un determinato componente.</span><span class="sxs-lookup"><span data-stu-id="d291e-104">The CreateFolder table contains references to folders that need to be created explicitly for a particular component.</span></span>

<span data-ttu-id="d291e-105">La tabella CreateFolder include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="d291e-105">The CreateFolder table has the following columns.</span></span>



| <span data-ttu-id="d291e-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="d291e-106">Column</span></span>      | <span data-ttu-id="d291e-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="d291e-107">Type</span></span>                         | <span data-ttu-id="d291e-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="d291e-108">Key</span></span> | <span data-ttu-id="d291e-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="d291e-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="d291e-110">Directory\_</span><span class="sxs-lookup"><span data-stu-id="d291e-110">Directory\_</span></span> | [<span data-ttu-id="d291e-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="d291e-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="d291e-112">S</span><span class="sxs-lookup"><span data-stu-id="d291e-112">Y</span></span>   | <span data-ttu-id="d291e-113">N</span><span class="sxs-lookup"><span data-stu-id="d291e-113">N</span></span>        |
| <span data-ttu-id="d291e-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="d291e-114">Component\_</span></span> | [<span data-ttu-id="d291e-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="d291e-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="d291e-116">S</span><span class="sxs-lookup"><span data-stu-id="d291e-116">Y</span></span>   | <span data-ttu-id="d291e-117">N</span><span class="sxs-lookup"><span data-stu-id="d291e-117">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d291e-118">Colonne</span><span class="sxs-lookup"><span data-stu-id="d291e-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d291e-119"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span><span class="sxs-lookup"><span data-stu-id="d291e-119"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="d291e-120">Chiave esterna nella prima colonna della tabella di [directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="d291e-120">External key into the first column of the [Directory table](directory-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="d291e-121"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="d291e-121"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="d291e-122">Chiave esterna nella prima colonna della tabella dei [componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="d291e-122">External key into the first column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d291e-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d291e-123">Remarks</span></span>

<span data-ttu-id="d291e-124">Le cartelle in questa tabella vengono create quando viene installato il componente.</span><span class="sxs-lookup"><span data-stu-id="d291e-124">The folders in this table are created when the component is installed.</span></span> <span data-ttu-id="d291e-125">Si è tentato di rimuovere queste cartelle solo quando il componente è stato disinstallato o spostato nell'origine.</span><span class="sxs-lookup"><span data-stu-id="d291e-125">An attempt is made to remove these folders only when the component is uninstalled or moved to run-from-source.</span></span> <span data-ttu-id="d291e-126">Non viene attivata alcuna rimozione automatica se le cartelle diventano vuote.</span><span class="sxs-lookup"><span data-stu-id="d291e-126">No automatic removal is triggered if the folders become empty.</span></span> <span data-ttu-id="d291e-127">Al contrario, le cartelle create dal programma di installazione ma non elencate in questa tabella vengono rimosse quando diventano vuote.</span><span class="sxs-lookup"><span data-stu-id="d291e-127">In contrast, folders created by the installer but not listed in this table are removed when they become empty.</span></span>

<span data-ttu-id="d291e-128">Poiché le cartelle create dal programma di installazione vengono eliminate quando diventano vuote, è necessario creare una voce nella tabella CreateFolder per installare un componente costituito da una cartella vuota.</span><span class="sxs-lookup"><span data-stu-id="d291e-128">Because folders created by the installer are deleted when they become empty, you must author an entry into the CreateFolder table to install a component that consists of an empty folder.</span></span>

<span data-ttu-id="d291e-129">Questa tabella viene definita quando viene chiamata l'azione [CreateFolders](createfolders-action.md) o [RemoveFolders](removefolders-action.md) .</span><span class="sxs-lookup"><span data-stu-id="d291e-129">This table is referred to when the [CreateFolders](createfolders-action.md) action or the [RemoveFolders](removefolders-action.md) action is called.</span></span>

<span data-ttu-id="d291e-130">Per informazioni su come proteggere una cartella, vedere la [tabella MsiLockPermissionsEx](msilockpermissionsex-table.md) e la [tabella LockPermissions](lockpermissions-table.md).</span><span class="sxs-lookup"><span data-stu-id="d291e-130">For information on how to secure a folder see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) and [LockPermissions Table](lockpermissions-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="d291e-131">Convalida</span><span class="sxs-lookup"><span data-stu-id="d291e-131">Validation</span></span>

<dl>

[<span data-ttu-id="d291e-132">ICE03</span><span class="sxs-lookup"><span data-stu-id="d291e-132">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d291e-133">ICE06</span><span class="sxs-lookup"><span data-stu-id="d291e-133">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d291e-134">ICE18</span><span class="sxs-lookup"><span data-stu-id="d291e-134">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="d291e-135">ICE32</span><span class="sxs-lookup"><span data-stu-id="d291e-135">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d291e-136">ICE55</span><span class="sxs-lookup"><span data-stu-id="d291e-136">ICE55</span></span>](ice55.md)  
</dl>

 

 



