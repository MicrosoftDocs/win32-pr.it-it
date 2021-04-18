---
description: Associazione che connette un servizio di commutazione virtuale a un servizio di bridging trasparente.
ms.assetid: 4DFD73CA-38F0-4C06-BEBE-C684590E50E8
title: Classe Msvm_HostedSwitchService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedSwitchService
- Msvm_HostedSwitchService.Antecedent
- Msvm_HostedSwitchService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0b7319dbe58649ac7abce2d36201f3984c1b807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306038"
---
# <a name="msvm_hostedswitchservice-class"></a><span data-ttu-id="857f4-103">\_Classe MSVM HostedSwitchService</span><span class="sxs-lookup"><span data-stu-id="857f4-103">Msvm\_HostedSwitchService class</span></span>

<span data-ttu-id="857f4-104">Associazione che connette un servizio di commutazione virtuale a un servizio di bridging trasparente.</span><span class="sxs-lookup"><span data-stu-id="857f4-104">An association that connects a virtual switch service to a transparent bridging service.</span></span>

<span data-ttu-id="857f4-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="857f4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="857f4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="857f4-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedSwitchService : CIM_HostedService
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  CIM_Service                REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="857f4-107">Members</span><span class="sxs-lookup"><span data-stu-id="857f4-107">Members</span></span>

<span data-ttu-id="857f4-108">La **classe \_ HostedSwitchService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="857f4-108">The **Msvm\_HostedSwitchService** class has these types of members:</span></span>

-   [<span data-ttu-id="857f4-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="857f4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="857f4-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="857f4-110">Properties</span></span>

<span data-ttu-id="857f4-111">La **classe \_ HostedSwitchService di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="857f4-111">The **Msvm\_HostedSwitchService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="857f4-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="857f4-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857f4-113">Tipo di dati: **[ **MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span><span class="sxs-lookup"><span data-stu-id="857f4-113">Data type: **[**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span></span>
</dt> <dt>

<span data-ttu-id="857f4-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="857f4-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857f4-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="857f4-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="857f4-116">Riferimento a un'istanza della classe [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) che rappresenta il Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="857f4-116">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="857f4-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="857f4-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857f4-118">Tipo di dati: **[ **\_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="857f4-118">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="857f4-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="857f4-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857f4-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="857f4-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="857f4-121">Riferimento a un'istanza della classe [**MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) che rappresenta il servizio di bridging.</span><span class="sxs-lookup"><span data-stu-id="857f4-121">A reference to an instance of the [**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md) class that represents the bridging service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="857f4-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="857f4-122">Remarks</span></span>

<span data-ttu-id="857f4-123">L'accesso alla **classe \_ HostedSwitchService di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="857f4-123">Access to the **Msvm\_HostedSwitchService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="857f4-124">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="857f4-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="857f4-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="857f4-125">Requirements</span></span>



| <span data-ttu-id="857f4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="857f4-126">Requirement</span></span> | <span data-ttu-id="857f4-127">Valore</span><span class="sxs-lookup"><span data-stu-id="857f4-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="857f4-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="857f4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="857f4-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="857f4-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="857f4-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="857f4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="857f4-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="857f4-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="857f4-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="857f4-132">Namespace</span></span><br/>                | <span data-ttu-id="857f4-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="857f4-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="857f4-134">MOF</span><span class="sxs-lookup"><span data-stu-id="857f4-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="857f4-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="857f4-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="857f4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="857f4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="857f4-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="857f4-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="857f4-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="857f4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="857f4-139">**\_Servizio ospitato CIM**</span><span class="sxs-lookup"><span data-stu-id="857f4-139">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dt>

[<span data-ttu-id="857f4-140">**\_Servizio ospitato CIM**</span><span class="sxs-lookup"><span data-stu-id="857f4-140">**CIM\_HostedService**</span></span>](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> </dl>

 

