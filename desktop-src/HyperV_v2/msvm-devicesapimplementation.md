---
description: Associazione tra un punto di accesso al servizio (SAP) e la relativa modalità di implementazione.
ms.assetid: 36108521-A699-4498-A962-DC0801D9EE81
title: Classe Msvm_DeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DeviceSAPImplementation
- Msvm_DeviceSAPImplementation.Antecedent
- Msvm_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9551d4409edfdfca18b66e3a3b86d6adcb28b19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314332"
---
# <a name="msvm_devicesapimplementation-class"></a><span data-ttu-id="f6117-103">\_Classe MSVM DeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="f6117-103">Msvm\_DeviceSAPImplementation class</span></span>

<span data-ttu-id="f6117-104">Associazione tra un punto di accesso al servizio (SAP) e la relativa modalità di implementazione.</span><span class="sxs-lookup"><span data-stu-id="f6117-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="f6117-105">La cardinalità di questa associazione è molti-a-molti.</span><span class="sxs-lookup"><span data-stu-id="f6117-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="f6117-106">Un SAP può essere fornito da più di un dispositivo logico, operando insieme.</span><span class="sxs-lookup"><span data-stu-id="f6117-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="f6117-107">Qualsiasi dispositivo può fornire più di un SAP.</span><span class="sxs-lookup"><span data-stu-id="f6117-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="f6117-108">Quando molti dispositivi logici sono associati a un singolo SAP, si presuppone che questi elementi funzionino insieme per fornire il punto di accesso.</span><span class="sxs-lookup"><span data-stu-id="f6117-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="f6117-109">Se sono presenti implementazioni diverse di un SAP, ognuna di queste implementazioni genererà le singole creazioni di istanze dell'oggetto SAP.</span><span class="sxs-lookup"><span data-stu-id="f6117-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="f6117-110">Queste singole creazioni di istanze avrebbero quindi le associazioni alle implementazioni univoche.</span><span class="sxs-lookup"><span data-stu-id="f6117-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="f6117-111">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f6117-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6117-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6117-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f6117-113">Members</span><span class="sxs-lookup"><span data-stu-id="f6117-113">Members</span></span>

<span data-ttu-id="f6117-114">La **classe \_ DeviceSAPImplementation di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f6117-114">The **Msvm\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="f6117-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f6117-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6117-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f6117-116">Properties</span></span>

<span data-ttu-id="f6117-117">La **classe \_ DeviceSAPImplementation di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f6117-117">The **Msvm\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6117-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="f6117-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6117-119">Tipo di dati: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="f6117-119">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="f6117-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6117-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6117-121">Il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f6117-121">The logical device.</span></span> <span data-ttu-id="f6117-122">Questa proprietà viene ereditata da [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span><span class="sxs-lookup"><span data-stu-id="f6117-122">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> <dt>

<span data-ttu-id="f6117-123">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="f6117-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6117-124">Tipo di dati: **[ **CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span><span class="sxs-lookup"><span data-stu-id="f6117-124">Data type: **[**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span></span>
</dt> <dt>

<span data-ttu-id="f6117-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6117-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6117-126">Il punto di accesso al servizio implementato usando il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f6117-126">The service access point implemented using the logical device.</span></span> <span data-ttu-id="f6117-127">Questa proprietà viene ereditata da [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span><span class="sxs-lookup"><span data-stu-id="f6117-127">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6117-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6117-128">Remarks</span></span>

<span data-ttu-id="f6117-129">L'accesso alla **classe \_ DeviceSAPImplementation di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="f6117-129">Access to the **Msvm\_DeviceSAPImplementation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f6117-130">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f6117-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="f6117-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="f6117-131">Examples</span></span>

<span data-ttu-id="f6117-132">Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f6117-132">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6117-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6117-133">Requirements</span></span>



| <span data-ttu-id="f6117-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6117-134">Requirement</span></span> | <span data-ttu-id="f6117-135">Valore</span><span class="sxs-lookup"><span data-stu-id="f6117-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6117-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6117-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f6117-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f6117-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f6117-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6117-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f6117-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f6117-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6117-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f6117-140">Namespace</span></span><br/>                | <span data-ttu-id="f6117-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f6117-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f6117-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f6117-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6117-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6117-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6117-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f6117-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6117-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6117-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f6117-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6117-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6117-147">**\_DEVICESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="f6117-147">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dt>

[<span data-ttu-id="f6117-148">**\_DEVICESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="f6117-148">**CIM\_DeviceSAPImplementation**</span></span>](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 

