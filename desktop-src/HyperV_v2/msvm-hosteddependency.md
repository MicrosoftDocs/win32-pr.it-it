---
description: Associa un'istanza di macchina virtuale all'oggetto di sistema del computer che rappresenta il sistema di hosting fisico.
ms.assetid: 755624D7-04D0-47EA-8623-DEDE6B1D5CBC
title: Classe Msvm_HostedDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedDependency
- Msvm_HostedDependency.Antecedent
- Msvm_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ce580e6b478dbdf320377c2738708d0eb7689fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878717"
---
# <a name="msvm_hosteddependency-class"></a><span data-ttu-id="ff3ed-103">\_Classe MSVM HostedDependency</span><span class="sxs-lookup"><span data-stu-id="ff3ed-103">Msvm\_HostedDependency class</span></span>

<span data-ttu-id="ff3ed-104">Associa un'istanza di macchina virtuale all'oggetto di sistema del computer che rappresenta il sistema di hosting fisico.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-104">Associates a virtual machine instance with the computer system object that represents the physical, hosting system.</span></span>

<span data-ttu-id="ff3ed-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff3ed-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff3ed-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedDependency : CIM_HostedDependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="ff3ed-107">Members</span><span class="sxs-lookup"><span data-stu-id="ff3ed-107">Members</span></span>

<span data-ttu-id="ff3ed-108">La **classe \_ HostedDependency di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ff3ed-108">The **Msvm\_HostedDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="ff3ed-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ff3ed-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ff3ed-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ff3ed-110">Properties</span></span>

<span data-ttu-id="ff3ed-111">La **classe \_ HostedDependency di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-111">The **Msvm\_HostedDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ff3ed-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="ff3ed-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff3ed-113">Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="ff3ed-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="ff3ed-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ff3ed-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff3ed-115">Riferimento al sistema del computer host.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-115">A reference to the hosting computer system.</span></span> <span data-ttu-id="ff3ed-116">Questa proprietà viene ereditata da [**CIM \_ HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ff3ed-116">This property is inherited from [**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ff3ed-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="ff3ed-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff3ed-118">Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="ff3ed-118">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="ff3ed-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ff3ed-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff3ed-120">Riferimento alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-120">A reference to the virtual machine.</span></span> <span data-ttu-id="ff3ed-121">Questa proprietà viene ereditata da [**CIM \_ HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ff3ed-121">This property is inherited from [**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff3ed-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff3ed-122">Remarks</span></span>

<span data-ttu-id="ff3ed-123">L'accesso alla **classe \_ HostedDependency di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-123">Access to the **Msvm\_HostedDependency** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ff3ed-124">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ff3ed-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff3ed-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff3ed-125">Requirements</span></span>



| <span data-ttu-id="ff3ed-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff3ed-126">Requirement</span></span> | <span data-ttu-id="ff3ed-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ff3ed-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff3ed-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff3ed-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ff3ed-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ff3ed-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ff3ed-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff3ed-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ff3ed-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ff3ed-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ff3ed-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ff3ed-132">Namespace</span></span><br/>                | <span data-ttu-id="ff3ed-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ff3ed-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ff3ed-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ff3ed-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff3ed-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff3ed-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff3ed-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ff3ed-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff3ed-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ff3ed-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ff3ed-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff3ed-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff3ed-139">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="ff3ed-139">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> <dt>

<span data-ttu-id="ff3ed-140">[**\_HOSTEDDEPENDENCY CIM**](/previous-versions//cc136861(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ff3ed-140">[**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ff3ed-141">Classi di gestione del sistema virtuale</span><span class="sxs-lookup"><span data-stu-id="ff3ed-141">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

