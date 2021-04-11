---
description: La \_ classe CIM AllocatedResource rappresenta un'associazione tra dispositivi logici e risorse di sistema e indica che la risorsa è assegnata al dispositivo.
ms.assetid: e1702635-32f5-4280-8c02-3940fd858106
ms.tgt_platform: multiple
title: Classe CIM_AllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocatedResource
- CIM_AllocatedResource.Dependent
- CIM_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4191315b76553a8c23b94c04d9649cceb131855
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127218"
---
# <a name="cim_allocatedresource-class"></a><span data-ttu-id="aba1e-103">CIM \_ AllocatedResource (classe)</span><span class="sxs-lookup"><span data-stu-id="aba1e-103">CIM\_AllocatedResource class</span></span>

<span data-ttu-id="aba1e-104">La classe **CIM \_ AllocatedResource** rappresenta un'associazione tra dispositivi logici e risorse di sistema e indica che la risorsa è assegnata al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aba1e-104">The **CIM\_AllocatedResource** class represents an association between logical devices and system resources and indicates that the resource is assigned to the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aba1e-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="aba1e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aba1e-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="aba1e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aba1e-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="aba1e-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aba1e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aba1e-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C579-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="aba1e-109">Members</span><span class="sxs-lookup"><span data-stu-id="aba1e-109">Members</span></span>

<span data-ttu-id="aba1e-110">La classe **CIM \_ AllocatedResource** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="aba1e-110">The **CIM\_AllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="aba1e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aba1e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aba1e-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aba1e-112">Properties</span></span>

<span data-ttu-id="aba1e-113">La classe **CIM \_ AllocatedResource** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="aba1e-113">The **CIM\_AllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aba1e-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="aba1e-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aba1e-115">Tipo di dati: **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="aba1e-115">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="aba1e-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aba1e-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aba1e-117">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="aba1e-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="aba1e-118">[**\_ SystemResource CIM**](cim-systemresource.md) che descrive la risorsa.</span><span class="sxs-lookup"><span data-stu-id="aba1e-118">A [**CIM\_SystemResource**](cim-systemresource.md) that describes the resource.</span></span>

</dd> <dt>

<span data-ttu-id="aba1e-119">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="aba1e-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aba1e-120">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="aba1e-120">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="aba1e-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aba1e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aba1e-122">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="aba1e-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="aba1e-123">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che contiene il dispositivo logico a cui è assegnata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="aba1e-123">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device to which the resource is assigned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aba1e-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="aba1e-124">Remarks</span></span>

<span data-ttu-id="aba1e-125">La classe **CIM \_ AllocatedResource** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="aba1e-125">The **CIM\_AllocatedResource** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="aba1e-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="aba1e-126">WMI does not implement this class.</span></span> <span data-ttu-id="aba1e-127">Per ulteriori informazioni sulle classi derivate da **CIM \_ AllocatedResource**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="aba1e-127">For more information about classes derived from **CIM\_AllocatedResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="aba1e-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="aba1e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aba1e-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="aba1e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aba1e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aba1e-130">Requirements</span></span>



| <span data-ttu-id="aba1e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="aba1e-131">Requirement</span></span> | <span data-ttu-id="aba1e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="aba1e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aba1e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aba1e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="aba1e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aba1e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aba1e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aba1e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="aba1e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aba1e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aba1e-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aba1e-137">Namespace</span></span><br/>                | <span data-ttu-id="aba1e-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="aba1e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aba1e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="aba1e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aba1e-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aba1e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aba1e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="aba1e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aba1e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aba1e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aba1e-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aba1e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba1e-144">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="aba1e-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

