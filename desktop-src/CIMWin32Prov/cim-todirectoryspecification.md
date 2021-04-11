---
description: L' \_ associazione CIM ToDirectorySpecification identifica la directory di destinazione per l'azione del file.
ms.assetid: ab31101f-1948-4b3d-baef-0d61d5898b21
ms.tgt_platform: multiple
title: Classe CIM_ToDirectorySpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectorySpecification
- CIM_ToDirectorySpecification.DestinationDirectory
- CIM_ToDirectorySpecification.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0728f605e02195a6bf2bd4beb0ca67fe8744e12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127770"
---
# <a name="cim_todirectoryspecification-class"></a><span data-ttu-id="c712a-103">CIM \_ ToDirectorySpecification (classe)</span><span class="sxs-lookup"><span data-stu-id="c712a-103">CIM\_ToDirectorySpecification class</span></span>

<span data-ttu-id="c712a-104">L'associazione **CIM \_ ToDirectorySpecification** identifica la directory di destinazione per l'azione del file.</span><span class="sxs-lookup"><span data-stu-id="c712a-104">The **CIM\_ToDirectorySpecification** association identifies the target directory for the file action.</span></span> <span data-ttu-id="c712a-105">Quando si utilizza questa associazione, si presuppone che la directory di destinazione esista già.</span><span class="sxs-lookup"><span data-stu-id="c712a-105">When this association is used, it is assumed that the target directory already existed.</span></span> <span data-ttu-id="c712a-106">Questa associazione non può esistere con un'associazione [**CIM \_ ToDirectoryAction**](cim-todirectoryaction.md) poiché un'azione file può coinvolgere solo una singola directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c712a-106">This association cannot exist with a [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) association since a file action can only involve a single target directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c712a-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="c712a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c712a-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c712a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c712a-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c712a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c712a-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="c712a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c712a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c712a-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{C3E25A3C-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectorySpecification
{
  CIM_DirectorySpecification REF DestinationDirectory;
  CIM_CopyFileAction         REF FileName;
};
```

## <a name="members"></a><span data-ttu-id="c712a-112">Members</span><span class="sxs-lookup"><span data-stu-id="c712a-112">Members</span></span>

<span data-ttu-id="c712a-113">La classe **CIM \_ ToDirectorySpecification** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c712a-113">The **CIM\_ToDirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="c712a-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c712a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c712a-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c712a-115">Properties</span></span>

<span data-ttu-id="c712a-116">La classe **CIM \_ ToDirectorySpecification** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c712a-116">The **CIM\_ToDirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c712a-117">**DestinationDirectory**</span><span class="sxs-lookup"><span data-stu-id="c712a-117">**DestinationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c712a-118">Tipo di dati: **CIM \_ DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="c712a-118">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="c712a-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c712a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c712a-120">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="c712a-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="c712a-121">Riferimento alla directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c712a-121">Reference to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="c712a-122">**FileName**</span><span class="sxs-lookup"><span data-stu-id="c712a-122">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c712a-123">Tipo di dati: **CIM \_ CopyFileAction**</span><span class="sxs-lookup"><span data-stu-id="c712a-123">Data type: **CIM\_CopyFileAction**</span></span>
</dt> <dt>

<span data-ttu-id="c712a-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c712a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c712a-125">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="c712a-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="c712a-126">Riferimento al nome del file.</span><span class="sxs-lookup"><span data-stu-id="c712a-126">Reference to the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c712a-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="c712a-127">Remarks</span></span>

<span data-ttu-id="c712a-128">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="c712a-128">WMI does not implement this class.</span></span>

<span data-ttu-id="c712a-129">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="c712a-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c712a-130">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="c712a-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c712a-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c712a-131">Requirements</span></span>



| <span data-ttu-id="c712a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c712a-132">Requirement</span></span> | <span data-ttu-id="c712a-133">Valore</span><span class="sxs-lookup"><span data-stu-id="c712a-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c712a-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c712a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c712a-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c712a-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c712a-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c712a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c712a-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c712a-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c712a-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c712a-138">Namespace</span></span><br/>                | <span data-ttu-id="c712a-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c712a-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c712a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c712a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c712a-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c712a-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c712a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c712a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c712a-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c712a-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

