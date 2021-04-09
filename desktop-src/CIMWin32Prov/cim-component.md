---
description: L' \_ associazione componente CIM rappresenta le parti di una relazione tra mses.
ms.assetid: a074e2f7-b092-4d3c-be5e-2069b643431b
ms.tgt_platform: multiple
title: Classe CIM_Component (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b516118bc0cd6f12285933b1c15e7f2801ad40d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877981"
---
# <a name="cim_component-class-cimwin32-wmi-providers"></a><span data-ttu-id="83586-103">Classe CIM_Component (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="83586-103">CIM_Component class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="83586-104">L' **associazione \_ componente CIM** rappresenta le parti di una relazione tra mses.</span><span class="sxs-lookup"><span data-stu-id="83586-104">The **CIM\_Component** association represents the parts of a relationship between MSEs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83586-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="83586-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="83586-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="83586-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="83586-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="83586-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="83586-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="83586-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="83586-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83586-109">Syntax</span></span>

``` syntax
[Association, Abstract, Aggregation, UUID("{8502C573-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="83586-110">Members</span><span class="sxs-lookup"><span data-stu-id="83586-110">Members</span></span>

<span data-ttu-id="83586-111">La classe del **\_ componente CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="83586-111">The **CIM\_Component** class has these types of members:</span></span>

-   [<span data-ttu-id="83586-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="83586-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83586-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="83586-113">Properties</span></span>

<span data-ttu-id="83586-114">La classe del **\_ componente CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="83586-114">The **CIM\_Component** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83586-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="83586-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83586-116">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="83586-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="83586-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83586-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83586-118">Qualificatori: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="83586-118">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="83586-119">[**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) che descrive l'elemento padre nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="83586-119">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="83586-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="83586-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83586-121">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="83586-121">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="83586-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83586-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83586-123">[**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) che descrive l'elemento figlio nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="83586-123">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element in the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83586-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="83586-124">Remarks</span></span>

<span data-ttu-id="83586-125">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="83586-125">WMI does not implement this class.</span></span> <span data-ttu-id="83586-126">Per ulteriori informazioni sulle classi derivate dal **\_ componente CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="83586-126">For more information about classes derived from **CIM\_Component**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="83586-127">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="83586-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="83586-128">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="83586-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="83586-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83586-129">Requirements</span></span>



| <span data-ttu-id="83586-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="83586-130">Requirement</span></span> | <span data-ttu-id="83586-131">Valore</span><span class="sxs-lookup"><span data-stu-id="83586-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83586-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83586-132">Minimum supported client</span></span><br/> | <span data-ttu-id="83586-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83586-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83586-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83586-134">Minimum supported server</span></span><br/> | <span data-ttu-id="83586-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83586-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83586-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="83586-136">Namespace</span></span><br/>                | <span data-ttu-id="83586-137">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="83586-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="83586-138">MOF</span><span class="sxs-lookup"><span data-stu-id="83586-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83586-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83586-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="83586-140">DLL</span><span class="sxs-lookup"><span data-stu-id="83586-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83586-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83586-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

