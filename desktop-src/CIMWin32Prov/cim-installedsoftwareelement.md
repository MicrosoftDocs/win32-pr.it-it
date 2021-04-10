---
description: La \_ classe CIM InstalledSoftwareElement associa un sistema di computer a un elemento software installato.
ms.assetid: b9a570ed-b4e0-4f73-82e3-6d2bd1708e16
ms.tgt_platform: multiple
title: Classe CIM_InstalledSoftwareElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledSoftwareElement
- CIM_InstalledSoftwareElement.Software
- CIM_InstalledSoftwareElement.System
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd082477b2e2ba194163784b74883872b1edb6a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126959"
---
# <a name="cim_installedsoftwareelement-class"></a><span data-ttu-id="ee8a7-103">CIM \_ InstalledSoftwareElement (classe)</span><span class="sxs-lookup"><span data-stu-id="ee8a7-103">CIM\_InstalledSoftwareElement class</span></span>

<span data-ttu-id="ee8a7-104">La classe **CIM \_ InstalledSoftwareElement** associa un sistema di computer a un elemento software installato.</span><span class="sxs-lookup"><span data-stu-id="ee8a7-104">The **CIM\_InstalledSoftwareElement** class associates a computer system with an installed software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee8a7-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ee8a7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ee8a7-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ee8a7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ee8a7-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ee8a7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ee8a7-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ee8a7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee8a7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee8a7-109">Syntax</span></span>

``` syntax
[UUID("{A7B05028-DB2A-11d2-85FC-0000F8102E5F}"), Association, Abstract, AMENDMENT]
class CIM_InstalledSoftwareElement
{
  CIM_SoftwareElement REF Software;
  CIM_ComputerSystem  REF System;
};
```

## <a name="members"></a><span data-ttu-id="ee8a7-110">Members</span><span class="sxs-lookup"><span data-stu-id="ee8a7-110">Members</span></span>

<span data-ttu-id="ee8a7-111">La classe **CIM \_ InstalledSoftwareElement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ee8a7-111">The **CIM\_InstalledSoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="ee8a7-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee8a7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee8a7-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee8a7-113">Properties</span></span>

<span data-ttu-id="ee8a7-114">La classe **CIM \_ InstalledSoftwareElement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee8a7-114">The **CIM\_InstalledSoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee8a7-115">**Software**</span><span class="sxs-lookup"><span data-stu-id="ee8a7-115">**Software**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee8a7-116">Tipo di dati: **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="ee8a7-116">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="ee8a7-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee8a7-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee8a7-118">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)</span><span class="sxs-lookup"><span data-stu-id="ee8a7-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE)</span></span>
</dt> </dl>

<span data-ttu-id="ee8a7-119">Riferimento all'elemento software installato nel computer.</span><span class="sxs-lookup"><span data-stu-id="ee8a7-119">Reference to the software element that is installed on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="ee8a7-120">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="ee8a7-120">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee8a7-121">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="ee8a7-121">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="ee8a7-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee8a7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee8a7-123">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)</span><span class="sxs-lookup"><span data-stu-id="ee8a7-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE)</span></span>
</dt> </dl>

<span data-ttu-id="ee8a7-124">Riferimento al sistema del computer che ospita un particolare elemento software.</span><span class="sxs-lookup"><span data-stu-id="ee8a7-124">Reference to the computer system hosting a particular software element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee8a7-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee8a7-125">Remarks</span></span>

<span data-ttu-id="ee8a7-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ee8a7-126">WMI does not implement this class.</span></span> <span data-ttu-id="ee8a7-127">Per le classi derivate da **CIM \_ InstalledSoftwareElement**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ee8a7-127">For classes derived from **CIM\_InstalledSoftwareElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ee8a7-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ee8a7-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ee8a7-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ee8a7-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee8a7-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee8a7-130">Requirements</span></span>



| <span data-ttu-id="ee8a7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee8a7-131">Requirement</span></span> | <span data-ttu-id="ee8a7-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ee8a7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8a7-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee8a7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ee8a7-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee8a7-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ee8a7-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee8a7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ee8a7-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee8a7-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ee8a7-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ee8a7-137">Namespace</span></span><br/>                | <span data-ttu-id="ee8a7-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ee8a7-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ee8a7-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ee8a7-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee8a7-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee8a7-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee8a7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ee8a7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee8a7-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee8a7-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

