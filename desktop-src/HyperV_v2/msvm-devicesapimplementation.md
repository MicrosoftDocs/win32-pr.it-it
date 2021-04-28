---
description: 'Msvm_DeviceSAPImplementation classe : associazione tra un punto di accesso del servizio (SAP) e la modalità di implementazione.'
ms.assetid: 36108521-A699-4498-A962-DC0801D9EE81
title: Msvm_DeviceSAPImplementation classe
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
ms.openlocfilehash: 6fbe3c9b85e0a8c9f0c6a07d1db03784c4ac15e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112099"
---
# <a name="msvm_devicesapimplementation-class"></a><span data-ttu-id="d389a-103">Classe \_ Msvm DeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="d389a-103">Msvm\_DeviceSAPImplementation class</span></span>

<span data-ttu-id="d389a-104">Associazione tra un punto di accesso del servizio (SAP) e la modalità di implementazione.</span><span class="sxs-lookup"><span data-stu-id="d389a-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="d389a-105">La cardinalità di questa associazione è molti-a-molti.</span><span class="sxs-lookup"><span data-stu-id="d389a-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="d389a-106">Un sap può essere fornito da più di un dispositivo logico, operando in combinazione.</span><span class="sxs-lookup"><span data-stu-id="d389a-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="d389a-107">Qualsiasi dispositivo può fornire più di un SAP.</span><span class="sxs-lookup"><span data-stu-id="d389a-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="d389a-108">Quando molti dispositivi logici sono associati a un singolo SAP, si presuppone che questi elementi funzionino in combinazione per fornire il punto di accesso.</span><span class="sxs-lookup"><span data-stu-id="d389a-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="d389a-109">Se esistono implementazioni diverse di sap, ognuna di queste implementazioni comporterebbe la creazione di singole istanze dell'oggetto SAP.</span><span class="sxs-lookup"><span data-stu-id="d389a-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="d389a-110">Queste singole istanze hanno quindi associazioni alle implementazioni univoche.</span><span class="sxs-lookup"><span data-stu-id="d389a-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="d389a-111">La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d389a-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d389a-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d389a-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d389a-113">Members</span><span class="sxs-lookup"><span data-stu-id="d389a-113">Members</span></span>

<span data-ttu-id="d389a-114">La **classe \_ Msvm DeviceSAPImplementation** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d389a-114">The **Msvm\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="d389a-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d389a-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d389a-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d389a-116">Properties</span></span>

<span data-ttu-id="d389a-117">La **classe Msvm \_ DeviceSAPImplementation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d389a-117">The **Msvm\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d389a-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="d389a-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d389a-119">Tipo di dati: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="d389a-119">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="d389a-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d389a-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d389a-121">Dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d389a-121">The logical device.</span></span> <span data-ttu-id="d389a-122">Questa proprietà viene ereditata da [**CIM \_ DeviceSAPImplementation.**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)</span><span class="sxs-lookup"><span data-stu-id="d389a-122">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> <dt>

<span data-ttu-id="d389a-123">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="d389a-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d389a-124">Tipo di dati: **[ **CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span><span class="sxs-lookup"><span data-stu-id="d389a-124">Data type: **[**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span></span>
</dt> <dt>

<span data-ttu-id="d389a-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d389a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d389a-126">Punto di accesso del servizio implementato usando il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d389a-126">The service access point implemented using the logical device.</span></span> <span data-ttu-id="d389a-127">Questa proprietà viene ereditata da [**CIM \_ DeviceSAPImplementation.**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)</span><span class="sxs-lookup"><span data-stu-id="d389a-127">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d389a-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="d389a-128">Remarks</span></span>

<span data-ttu-id="d389a-129">L'accesso alla **classe Msvm \_ DeviceSAPImplementation** potrebbe essere limitato dal filtro di Controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="d389a-129">Access to the **Msvm\_DeviceSAPImplementation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d389a-130">Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="d389a-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d389a-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="d389a-131">Examples</span></span>

<span data-ttu-id="d389a-132">Vedere [Esecuzione di query sugli oggetti di rete.](querying-networking-objects.md)</span><span class="sxs-lookup"><span data-stu-id="d389a-132">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d389a-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d389a-133">Requirements</span></span>



| <span data-ttu-id="d389a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d389a-134">Requirement</span></span> | <span data-ttu-id="d389a-135">Valore</span><span class="sxs-lookup"><span data-stu-id="d389a-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d389a-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d389a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d389a-137">Windows 8 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d389a-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d389a-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d389a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d389a-139">Solo app desktop di Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d389a-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d389a-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d389a-140">Namespace</span></span><br/>                | <span data-ttu-id="d389a-141">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="d389a-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d389a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d389a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d389a-143"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="d389a-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d389a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d389a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d389a-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d389a-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d389a-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d389a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d389a-147">**CIM \_ DeviceSAPImplementation**</span><span class="sxs-lookup"><span data-stu-id="d389a-147">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dt>

[<span data-ttu-id="d389a-148">**CIM \_ DeviceSAPImplementation**</span><span class="sxs-lookup"><span data-stu-id="d389a-148">**CIM\_DeviceSAPImplementation**</span></span>](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 

