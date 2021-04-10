---
description: L' \_ associazione CIM HostedFileSystem rappresenta un collegamento tra il computer e i file System ospitati nel computer.
ms.assetid: 1027fc6b-588b-4da8-8b3f-0c4c3328534a
ms.tgt_platform: multiple
title: Classe CIM_HostedFileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedFileSystem
- CIM_HostedFileSystem.PartComponent
- CIM_HostedFileSystem.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eef90ea3f1ed743ec5bee0eefa5afebc8c340077
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126966"
---
# <a name="cim_hostedfilesystem-class"></a><span data-ttu-id="a320e-103">CIM \_ HostedFileSystem (classe)</span><span class="sxs-lookup"><span data-stu-id="a320e-103">CIM\_HostedFileSystem class</span></span>

<span data-ttu-id="a320e-104">L'associazione **CIM \_ HostedFileSystem** rappresenta un collegamento tra il computer e i file System ospitati nel computer.</span><span class="sxs-lookup"><span data-stu-id="a320e-104">The **CIM\_HostedFileSystem** association represents a link between the computer system and the file system hosted on the computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a320e-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a320e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a320e-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a320e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a320e-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a320e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a320e-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a320e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a320e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a320e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC898-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_HostedFileSystem : CIM_SystemComponent
{
  CIM_FileSystem     REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="a320e-110">Members</span><span class="sxs-lookup"><span data-stu-id="a320e-110">Members</span></span>

<span data-ttu-id="a320e-111">La classe **CIM \_ HostedFileSystem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a320e-111">The **CIM\_HostedFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="a320e-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a320e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a320e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a320e-113">Properties</span></span>

<span data-ttu-id="a320e-114">La classe **CIM \_ HostedFileSystem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a320e-114">The **CIM\_HostedFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a320e-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a320e-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a320e-116">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="a320e-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a320e-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a320e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a320e-118">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="a320e-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="a320e-119">Un [**\_ ComputerSystem CIM**](cim-computersystem.md) che descrive il computer.</span><span class="sxs-lookup"><span data-stu-id="a320e-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="a320e-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a320e-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a320e-121">Tipo di dati **: \_ file System CIM**</span><span class="sxs-lookup"><span data-stu-id="a320e-121">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a320e-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a320e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a320e-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a320e-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a320e-124">Un [**\_ file System CIM**](cim-filesystem.md) che descrive il file System di proprietà del computer.</span><span class="sxs-lookup"><span data-stu-id="a320e-124">A [**CIM\_FileSystem**](cim-filesystem.md) that describes the file system owned by the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a320e-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="a320e-125">Remarks</span></span>

<span data-ttu-id="a320e-126">La classe **CIM \_ HostedFileSystem** è derivata da [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="a320e-126">The **CIM\_HostedFileSystem** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="a320e-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a320e-127">WMI does not implement this class.</span></span>

<span data-ttu-id="a320e-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a320e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a320e-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a320e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a320e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a320e-130">Requirements</span></span>



| <span data-ttu-id="a320e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a320e-131">Requirement</span></span> | <span data-ttu-id="a320e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="a320e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a320e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a320e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a320e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a320e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a320e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a320e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a320e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a320e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a320e-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a320e-137">Namespace</span></span><br/>                | <span data-ttu-id="a320e-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a320e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a320e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a320e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a320e-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a320e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a320e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a320e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a320e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a320e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a320e-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a320e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a320e-144">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="a320e-144">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

