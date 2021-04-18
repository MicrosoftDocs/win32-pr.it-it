---
description: Associa un'istanza di una risorsa allocata al pool di risorse da cui è stata allocata.
ms.assetid: BA3168C7-E4F1-414B-827B-1A811069F223
title: Classe Msvm_ElementAllocatedFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromPool
- Msvm_ElementAllocatedFromPool.Antecedent
- Msvm_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4d798c31fbcd8429007c53f3b156fc7c5922e7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314833"
---
# <a name="msvm_elementallocatedfrompool-class"></a><span data-ttu-id="5c621-103">\_Classe MSVM ElementAllocatedFromPool</span><span class="sxs-lookup"><span data-stu-id="5c621-103">Msvm\_ElementAllocatedFromPool class</span></span>

<span data-ttu-id="5c621-104">Associa un'istanza di una risorsa allocata al pool di risorse da cui è stata allocata.</span><span class="sxs-lookup"><span data-stu-id="5c621-104">Associates an instance of an allocated resource with the resource pool from which it was allocated.</span></span>

<span data-ttu-id="5c621-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5c621-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c621-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c621-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromPool : CIM_ElementAllocatedFromPool
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5c621-107">Members</span><span class="sxs-lookup"><span data-stu-id="5c621-107">Members</span></span>

<span data-ttu-id="5c621-108">La **classe \_ ElementAllocatedFromPool di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5c621-108">The **Msvm\_ElementAllocatedFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="5c621-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c621-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c621-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c621-110">Properties</span></span>

<span data-ttu-id="5c621-111">La **classe \_ ElementAllocatedFromPool di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5c621-111">The **Msvm\_ElementAllocatedFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c621-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="5c621-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c621-113">Tipo di dati: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="5c621-113">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="5c621-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c621-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c621-115">Qualificatori: **override**, **massimo** (1)</span><span class="sxs-lookup"><span data-stu-id="5c621-115">Qualifiers: **Override**, **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="5c621-116">Pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="5c621-116">The resource pool.</span></span> <span data-ttu-id="5c621-117">Questa proprietà viene ereditata da [**CIM \_ ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c621-117">This property is inherited from [**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5c621-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="5c621-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c621-119">Tipo di dati: **[ **\_ LogicalElement CIM**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span><span class="sxs-lookup"><span data-stu-id="5c621-119">Data type: **[**CIM\_LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span></span>
</dt> <dt>

<span data-ttu-id="5c621-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c621-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c621-121">Risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="5c621-121">The allocated resource.</span></span> <span data-ttu-id="5c621-122">Questa proprietà viene ereditata da [**CIM \_ ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c621-122">This property is inherited from [**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c621-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c621-123">Remarks</span></span>

<span data-ttu-id="5c621-124">L'accesso alla **classe \_ ElementAllocatedFromPool di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="5c621-124">Access to the **Msvm\_ElementAllocatedFromPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5c621-125">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5c621-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c621-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c621-126">Requirements</span></span>



| <span data-ttu-id="5c621-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c621-127">Requirement</span></span> | <span data-ttu-id="5c621-128">Valore</span><span class="sxs-lookup"><span data-stu-id="5c621-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c621-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c621-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5c621-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5c621-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5c621-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c621-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5c621-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5c621-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5c621-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5c621-133">Namespace</span></span><br/>                | <span data-ttu-id="5c621-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5c621-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5c621-135">MOF</span><span class="sxs-lookup"><span data-stu-id="5c621-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c621-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c621-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c621-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5c621-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c621-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5c621-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5c621-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c621-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c621-140">**\_ELEMENTALLOCATEDFROMPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="5c621-140">**CIM\_ElementAllocatedFromPool**</span></span>](cim-elementallocatedfrompool.md)
</dt> <dt>

<span data-ttu-id="5c621-141">[**\_ELEMENTALLOCATEDFROMPOOL CIM**](/previous-versions//cc150668(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c621-141">[**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5c621-142">**MSVM \_ ElementAllocatedFromPool (V1)**</span><span class="sxs-lookup"><span data-stu-id="5c621-142">**Msvm\_ElementAllocatedFromPool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-elementallocatedfrompool)
</dt> <dt>

[<span data-ttu-id="5c621-143">Classi di gestione delle risorse</span><span class="sxs-lookup"><span data-stu-id="5c621-143">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

