---
description: Connette una porta di commutazione a una voce di avanzamento dinamico (indirizzo MAC appreso).
ms.assetid: 70687D56-1282-46C7-AB4E-60E32B9DBA14
title: Classe Msvm_SwitchPortDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SwitchPortDynamicForwarding
- Msvm_SwitchPortDynamicForwarding.Antecedent
- Msvm_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e6dda46302e9e8c58710bad1f4221e14e2c3f4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310530"
---
# <a name="msvm_switchportdynamicforwarding-class"></a><span data-ttu-id="cf574-103">\_Classe MSVM SwitchPortDynamicForwarding</span><span class="sxs-lookup"><span data-stu-id="cf574-103">Msvm\_SwitchPortDynamicForwarding class</span></span>

<span data-ttu-id="cf574-104">Connette una porta di commutazione a una voce di avanzamento dinamico (indirizzo MAC appreso).</span><span class="sxs-lookup"><span data-stu-id="cf574-104">Connects a switch port to a dynamic forward entry (learned MAC address).</span></span> <span data-ttu-id="cf574-105">Questa operazione è utile per trovare tutti gli indirizzi MAC appresi per una porta specificata.</span><span class="sxs-lookup"><span data-stu-id="cf574-105">This is useful in finding all of the learned MAC addresses for a specified port.</span></span>

<span data-ttu-id="cf574-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cf574-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf574-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf574-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SwitchPortDynamicForwarding : CIM_SwitchPortDynamicForwarding
{
  Msvm_EthernetSwitchPort     REF Antecedent;
  Msvm_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="cf574-108">Members</span><span class="sxs-lookup"><span data-stu-id="cf574-108">Members</span></span>

<span data-ttu-id="cf574-109">La **classe \_ SwitchPortDynamicForwarding di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cf574-109">The **Msvm\_SwitchPortDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="cf574-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cf574-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf574-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cf574-111">Properties</span></span>

<span data-ttu-id="cf574-112">La **classe \_ SwitchPortDynamicForwarding di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cf574-112">The **Msvm\_SwitchPortDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf574-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="cf574-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf574-114">Tipo di dati: **[ **MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md)**</span><span class="sxs-lookup"><span data-stu-id="cf574-114">Data type: **[**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="cf574-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf574-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf574-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="cf574-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="cf574-117">Riferimento a un'istanza della classe [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) che rappresenta la porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="cf574-117">A reference to an instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class that represents the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="cf574-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="cf574-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf574-119">Tipo di dati: **[ **MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span><span class="sxs-lookup"><span data-stu-id="cf574-119">Data type: **[**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span></span>
</dt> <dt>

<span data-ttu-id="cf574-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf574-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf574-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="cf574-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="cf574-122">Riferimento a un'istanza della classe [**\_ DynamicForwardingEntry MSVM**](msvm-dynamicforwardingentry.md) che rappresenta la voce di avanzamento dinamico del database di inoltri.</span><span class="sxs-lookup"><span data-stu-id="cf574-122">A reference to an instance of the [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) class that represents the dynamic forwarding entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf574-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf574-123">Remarks</span></span>

<span data-ttu-id="cf574-124">L'accesso alla **classe \_ SwitchPortDynamicForwarding di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="cf574-124">Access to the **Msvm\_SwitchPortDynamicForwarding** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cf574-125">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="cf574-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="cf574-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="cf574-126">Examples</span></span>

<span data-ttu-id="cf574-127">Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="cf574-127">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf574-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf574-128">Requirements</span></span>



| <span data-ttu-id="cf574-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf574-129">Requirement</span></span> | <span data-ttu-id="cf574-130">Valore</span><span class="sxs-lookup"><span data-stu-id="cf574-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf574-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf574-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cf574-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cf574-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cf574-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf574-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cf574-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cf574-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cf574-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cf574-135">Namespace</span></span><br/>                | <span data-ttu-id="cf574-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="cf574-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cf574-137">MOF</span><span class="sxs-lookup"><span data-stu-id="cf574-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf574-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf574-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf574-139">DLL</span><span class="sxs-lookup"><span data-stu-id="cf574-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf574-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cf574-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cf574-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf574-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf574-142">**\_SWITCHPORTDYNAMICFORWARDING CIM**</span><span class="sxs-lookup"><span data-stu-id="cf574-142">**CIM\_SwitchPortDynamicForwarding**</span></span>](cim-switchportdynamicforwarding.md)
</dt> <dt>

<span data-ttu-id="cf574-143">[**\_SWITCHPORTDYNAMICFORWARDING CIM**](/previous-versions//cc136921(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf574-143">[**CIM\_SwitchPortDynamicForwarding**](/previous-versions//cc136921(v=vs.85))</span></span>
</dt> </dl>

 

