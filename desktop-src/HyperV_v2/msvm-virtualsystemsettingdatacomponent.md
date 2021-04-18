---
description: Associazione generica utilizzata per stabilire parte delle relazioni tra un'istanza di CIM \_ VirtualSystemSettingData e una o più istanze di CIM \_ ResourceAllocationSettingData.
ms.assetid: 936B41E7-1B3B-4A7B-86F0-E2F4497CE610
title: Classe Msvm_VirtualSystemSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingDataComponent
- Msvm_VirtualSystemSettingDataComponent.GroupComponent
- Msvm_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfff3981d6fdb9fdb0368fa887c559026fc10af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305982"
---
# <a name="msvm_virtualsystemsettingdatacomponent-class"></a><span data-ttu-id="e9bf6-103">\_Classe MSVM VirtualSystemSettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="e9bf6-103">Msvm\_VirtualSystemSettingDataComponent class</span></span>

<span data-ttu-id="e9bf6-104">Associazione generica utilizzata per stabilire relazioni ' parte di ' tra un'istanza di [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) e una o più istanze di [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="e9bf6-104">A generic association used to establish 'part of' relationships between one instance of [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) and one or more instances of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="e9bf6-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9bf6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9bf6-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingDataComponent : CIM_VirtualSystemSettingDataComponent
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="e9bf6-107">Members</span><span class="sxs-lookup"><span data-stu-id="e9bf6-107">Members</span></span>

<span data-ttu-id="e9bf6-108">La **classe \_ VirtualSystemSettingDataComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e9bf6-108">The **Msvm\_VirtualSystemSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="e9bf6-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e9bf6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9bf6-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e9bf6-110">Properties</span></span>

<span data-ttu-id="e9bf6-111">La **classe \_ VirtualSystemSettingDataComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-111">The **Msvm\_VirtualSystemSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9bf6-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e9bf6-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9bf6-113">Tipo di dati: **[ **CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="e9bf6-113">Data type: **[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="e9bf6-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9bf6-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9bf6-115">Qualificatori: **override**, **min** (1), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="e9bf6-115">Qualifiers: **Override**, **Min** (1), **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="e9bf6-116">Elemento padre nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-116">The parent element in the association.</span></span> <span data-ttu-id="e9bf6-117">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e9bf6-117">This property is inherited from [**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e9bf6-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e9bf6-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9bf6-119">Tipo di dati: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="e9bf6-119">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="e9bf6-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9bf6-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9bf6-121">Elemento figlio nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-121">The child element in the association.</span></span> <span data-ttu-id="e9bf6-122">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e9bf6-122">This property is inherited from [**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9bf6-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9bf6-123">Remarks</span></span>

<span data-ttu-id="e9bf6-124">L'accesso alla **classe \_ VirtualSystemSettingDataComponent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-124">Access to the **Msvm\_VirtualSystemSettingDataComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e9bf6-125">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e9bf6-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9bf6-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9bf6-126">Requirements</span></span>



| <span data-ttu-id="e9bf6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9bf6-127">Requirement</span></span> | <span data-ttu-id="e9bf6-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e9bf6-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9bf6-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9bf6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e9bf6-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e9bf6-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e9bf6-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9bf6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e9bf6-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e9bf6-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e9bf6-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e9bf6-133">Namespace</span></span><br/>                | <span data-ttu-id="e9bf6-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e9bf6-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e9bf6-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e9bf6-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9bf6-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9bf6-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9bf6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e9bf6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9bf6-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e9bf6-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e9bf6-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9bf6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9bf6-140">**\_VIRTUALSYSTEMSETTINGDATACOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e9bf6-140">**CIM\_VirtualSystemSettingDataComponent**</span></span>](cim-virtualsystemsettingdatacomponent.md)
</dt> <dt>

<span data-ttu-id="e9bf6-141">[**\_VIRTUALSYSTEMSETTINGDATACOMPONENT CIM**](/previous-versions//cc150674(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9bf6-141">[**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e9bf6-142">Classi di sistema virtuali</span><span class="sxs-lookup"><span data-stu-id="e9bf6-142">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

