---
description: Associa un servizio al relativo computer di hosting.
ms.assetid: 888ABA71-6D67-4933-89E6-40F731AA7153
title: Classe Msvm_HostedService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedService
- Msvm_HostedService.Antecedent
- Msvm_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 284254d32e788e374d56b3822f5c00868552e1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307902"
---
# <a name="msvm_hostedservice-class"></a><span data-ttu-id="3bb42-103">\_Classe MSVM servizio ospitato</span><span class="sxs-lookup"><span data-stu-id="3bb42-103">Msvm\_HostedService class</span></span>

<span data-ttu-id="3bb42-104">Associa un servizio al relativo computer di hosting.</span><span class="sxs-lookup"><span data-stu-id="3bb42-104">Associates a service with its hosting computer system.</span></span> <span data-ttu-id="3bb42-105">Le istanze di [**MSVM \_ VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) possono essere individuate tramite la relativa associazione a un host.</span><span class="sxs-lookup"><span data-stu-id="3bb42-105">Instances of [**Msvm\_VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) can be discovered through their association with a host.</span></span>

<span data-ttu-id="3bb42-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3bb42-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bb42-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3bb42-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedService : CIM_HostedService
{
  CIM_ManagedElement REF Antecedent;
  CIM_Service        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3bb42-108">Members</span><span class="sxs-lookup"><span data-stu-id="3bb42-108">Members</span></span>

<span data-ttu-id="3bb42-109">La **classe \_ servizio ospitato di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3bb42-109">The **Msvm\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="3bb42-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3bb42-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3bb42-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3bb42-111">Properties</span></span>

<span data-ttu-id="3bb42-112">La **classe \_ servizio ospitato di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3bb42-112">The **Msvm\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3bb42-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3bb42-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bb42-114">Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="3bb42-114">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="3bb42-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3bb42-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3bb42-116">Riferimento al sistema del computer host.</span><span class="sxs-lookup"><span data-stu-id="3bb42-116">A reference to the hosting computer system.</span></span> <span data-ttu-id="3bb42-117">Questa proprietà viene ereditata da [**CIM \_ servizio ospitato**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span><span class="sxs-lookup"><span data-stu-id="3bb42-117">This property is inherited from [**CIM\_HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span></span>

</dd> <dt>

<span data-ttu-id="3bb42-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="3bb42-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bb42-119">Tipo di dati: **[ **\_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="3bb42-119">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="3bb42-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3bb42-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3bb42-121">Riferimento al servizio ospitato.</span><span class="sxs-lookup"><span data-stu-id="3bb42-121">A reference to the service being hosted.</span></span> <span data-ttu-id="3bb42-122">Questa proprietà viene ereditata da [**CIM \_ servizio ospitato**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span><span class="sxs-lookup"><span data-stu-id="3bb42-122">This property is inherited from [**CIM\_HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3bb42-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="3bb42-123">Remarks</span></span>

<span data-ttu-id="3bb42-124">L'accesso alla **classe \_ servizio ospitato di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="3bb42-124">Access to the **Msvm\_HostedService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3bb42-125">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3bb42-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="3bb42-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="3bb42-126">Examples</span></span>

<span data-ttu-id="3bb42-127">Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3bb42-127">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bb42-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bb42-128">Requirements</span></span>



| <span data-ttu-id="3bb42-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bb42-129">Requirement</span></span> | <span data-ttu-id="3bb42-130">Valore</span><span class="sxs-lookup"><span data-stu-id="3bb42-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb42-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bb42-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3bb42-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3bb42-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3bb42-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bb42-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3bb42-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3bb42-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3bb42-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3bb42-135">Namespace</span></span><br/>                | <span data-ttu-id="3bb42-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3bb42-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3bb42-137">MOF</span><span class="sxs-lookup"><span data-stu-id="3bb42-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bb42-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3bb42-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3bb42-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3bb42-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bb42-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3bb42-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3bb42-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bb42-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bb42-142">**\_Servizio ospitato CIM**</span><span class="sxs-lookup"><span data-stu-id="3bb42-142">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dt>

[<span data-ttu-id="3bb42-143">**\_Servizio ospitato CIM**</span><span class="sxs-lookup"><span data-stu-id="3bb42-143">**CIM\_HostedService**</span></span>](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> <dt>

[<span data-ttu-id="3bb42-144">Classi di gestione del sistema virtuale</span><span class="sxs-lookup"><span data-stu-id="3bb42-144">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

