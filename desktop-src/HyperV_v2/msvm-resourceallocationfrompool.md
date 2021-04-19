---
description: Associa un'istanza di un'allocazione di risorse al pool di risorse da cui viene allocata.
ms.assetid: A2B3996D-7886-4B5F-BC89-EFDC1A48249B
title: Classe Msvm_ResourceAllocationFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationFromPool
- Msvm_ResourceAllocationFromPool.Antecedent
- Msvm_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5bb3db9bce86731b12730966a7a2f6d1c9dc8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313849"
---
# <a name="msvm_resourceallocationfrompool-class"></a><span data-ttu-id="4b988-103">\_Classe MSVM ResourceAllocationFromPool</span><span class="sxs-lookup"><span data-stu-id="4b988-103">Msvm\_ResourceAllocationFromPool class</span></span>

<span data-ttu-id="4b988-104">Associa un'istanza di un'allocazione di risorse al pool di risorse da cui viene allocata.</span><span class="sxs-lookup"><span data-stu-id="4b988-104">Associates an instance of a resource allocation with the resource pool from which it is allocated.</span></span>

<span data-ttu-id="4b988-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4b988-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b988-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b988-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationFromPool : CIM_ResourceAllocationFromPool
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4b988-107">Members</span><span class="sxs-lookup"><span data-stu-id="4b988-107">Members</span></span>

<span data-ttu-id="4b988-108">La **classe \_ ResourceAllocationFromPool di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4b988-108">The **Msvm\_ResourceAllocationFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="4b988-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b988-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b988-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b988-110">Properties</span></span>

<span data-ttu-id="4b988-111">La **classe \_ ResourceAllocationFromPool di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4b988-111">The **Msvm\_ResourceAllocationFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b988-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="4b988-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b988-113">Tipo di dati: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="4b988-113">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="4b988-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b988-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b988-115">Qualificatori: **override**, **massimo** (1)</span><span class="sxs-lookup"><span data-stu-id="4b988-115">Qualifiers: **Override**, **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="4b988-116">Pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b988-116">The resource pool.</span></span> <span data-ttu-id="4b988-117">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4b988-117">This property is inherited from [**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4b988-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="4b988-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b988-119">Tipo di dati: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="4b988-119">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="4b988-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b988-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b988-121">Allocazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4b988-121">The resource allocation.</span></span> <span data-ttu-id="4b988-122">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4b988-122">This property is inherited from [**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b988-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b988-123">Remarks</span></span>

<span data-ttu-id="4b988-124">L'accesso alla **classe \_ ResourceAllocationFromPool di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="4b988-124">Access to the **Msvm\_ResourceAllocationFromPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4b988-125">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4b988-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b988-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b988-126">Requirements</span></span>



| <span data-ttu-id="4b988-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b988-127">Requirement</span></span> | <span data-ttu-id="4b988-128">Valore</span><span class="sxs-lookup"><span data-stu-id="4b988-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b988-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b988-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4b988-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4b988-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4b988-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b988-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4b988-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4b988-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4b988-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4b988-133">Namespace</span></span><br/>                | <span data-ttu-id="4b988-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4b988-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4b988-135">MOF</span><span class="sxs-lookup"><span data-stu-id="4b988-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b988-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b988-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b988-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4b988-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b988-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b988-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4b988-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b988-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b988-140">**\_RESOURCEALLOCATIONFROMPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="4b988-140">**CIM\_ResourceAllocationFromPool**</span></span>](cim-resourceallocationfrompool.md)
</dt> <dt>

<span data-ttu-id="4b988-141">[**\_RESOURCEALLOCATIONFROMPOOL CIM**](/previous-versions//cc150673(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4b988-141">[**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4b988-142">**MSVM \_ ResourceAllocationFromPool (V1)**</span><span class="sxs-lookup"><span data-stu-id="4b988-142">**Msvm\_ResourceAllocationFromPool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourceallocationfrompool)
</dt> <dt>

[<span data-ttu-id="4b988-143">Classi di gestione delle risorse</span><span class="sxs-lookup"><span data-stu-id="4b988-143">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

