---
description: L' \_ associazione CIM ToDirectoryAction identifica la directory di destinazione per l'azione del file.
ms.assetid: f4dcd99c-4da8-447d-b6f7-7e3da63ca9c4
ms.tgt_platform: multiple
title: Classe CIM_ToDirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectoryAction
- CIM_ToDirectoryAction.DestinationDirectory
- CIM_ToDirectoryAction.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10ed2f7c2e2b46e63e2cc02cc8e6ce09ab2688e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749050"
---
# <a name="cim_todirectoryaction-class"></a><span data-ttu-id="c55a5-103">CIM \_ ToDirectoryAction (classe)</span><span class="sxs-lookup"><span data-stu-id="c55a5-103">CIM\_ToDirectoryAction class</span></span>

<span data-ttu-id="c55a5-104">L'associazione **CIM \_ ToDirectoryAction** identifica la directory di destinazione per l'azione del file.</span><span class="sxs-lookup"><span data-stu-id="c55a5-104">The **CIM\_ToDirectoryAction** association identifies the target directory for the file action.</span></span> <span data-ttu-id="c55a5-105">Quando si utilizza questa associazione, si presuppone che la directory di destinazione sia stata creata da un'azione precedente.</span><span class="sxs-lookup"><span data-stu-id="c55a5-105">When this association is used, it is assumed that the target directory was created by a previous action.</span></span> <span data-ttu-id="c55a5-106">Questa associazione non può esistere con un'associazione [**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md) poiché un'azione file può coinvolgere solo una singola directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c55a5-106">This association cannot exist with a [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) association since a file action can only involve a single target directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c55a5-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="c55a5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c55a5-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c55a5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c55a5-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c55a5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c55a5-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="c55a5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c55a5-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c55a5-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{B58D172E-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectoryAction
{
  CIM_DirectoryAction REF DestinationDirectory;
  CIM_CopyFileAction  REF FileName;
};
```

## <a name="members"></a><span data-ttu-id="c55a5-112">Members</span><span class="sxs-lookup"><span data-stu-id="c55a5-112">Members</span></span>

<span data-ttu-id="c55a5-113">La classe **CIM \_ ToDirectoryAction** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c55a5-113">The **CIM\_ToDirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="c55a5-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c55a5-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c55a5-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c55a5-115">Properties</span></span>

<span data-ttu-id="c55a5-116">La classe **CIM \_ ToDirectoryAction** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c55a5-116">The **CIM\_ToDirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c55a5-117">**DestinationDirectory**</span><span class="sxs-lookup"><span data-stu-id="c55a5-117">**DestinationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c55a5-118">Tipo di dati: **CIM \_ DirectoryAction**</span><span class="sxs-lookup"><span data-stu-id="c55a5-118">Data type: **CIM\_DirectoryAction**</span></span>
</dt> <dt>

<span data-ttu-id="c55a5-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c55a5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c55a5-120">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="c55a5-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="c55a5-121">Riferimento alla directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c55a5-121">Reference to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="c55a5-122">**FileName**</span><span class="sxs-lookup"><span data-stu-id="c55a5-122">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c55a5-123">Tipo di dati: **CIM \_ CopyFileAction**</span><span class="sxs-lookup"><span data-stu-id="c55a5-123">Data type: **CIM\_CopyFileAction**</span></span>
</dt> <dt>

<span data-ttu-id="c55a5-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c55a5-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c55a5-125">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="c55a5-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="c55a5-126">Riferimento al nome del file.</span><span class="sxs-lookup"><span data-stu-id="c55a5-126">Reference to the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c55a5-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="c55a5-127">Remarks</span></span>

<span data-ttu-id="c55a5-128">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="c55a5-128">WMI does not implement this class.</span></span>

<span data-ttu-id="c55a5-129">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="c55a5-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c55a5-130">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="c55a5-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c55a5-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c55a5-131">Requirements</span></span>



| <span data-ttu-id="c55a5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c55a5-132">Requirement</span></span> | <span data-ttu-id="c55a5-133">Valore</span><span class="sxs-lookup"><span data-stu-id="c55a5-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c55a5-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c55a5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c55a5-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c55a5-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c55a5-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c55a5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c55a5-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c55a5-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c55a5-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c55a5-138">Namespace</span></span><br/>                | <span data-ttu-id="c55a5-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c55a5-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c55a5-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c55a5-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c55a5-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c55a5-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c55a5-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c55a5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c55a5-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c55a5-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

