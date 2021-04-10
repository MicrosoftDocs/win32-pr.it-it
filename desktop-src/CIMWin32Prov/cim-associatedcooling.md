---
description: L' \_ associazione CIM AssociatedCooling indica quando le ventole o altri dispositivi di raffreddamento sono specifici di un dispositivo (rispetto alla custodia o al raffreddamento del cabinet).
ms.assetid: 7b20e429-593c-4365-a340-1aef9b0fadf5
ms.tgt_platform: multiple
title: Classe CIM_AssociatedCooling
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedCooling
- CIM_AssociatedCooling.Dependent
- CIM_AssociatedCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb838129226b225f024917e8f8e77ddc92ddf2ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127214"
---
# <a name="cim_associatedcooling-class"></a><span data-ttu-id="acc26-103">CIM \_ AssociatedCooling (classe)</span><span class="sxs-lookup"><span data-stu-id="acc26-103">CIM\_AssociatedCooling class</span></span>

<span data-ttu-id="acc26-104">L'associazione **CIM \_ AssociatedCooling** indica quando le ventole o altri dispositivi di raffreddamento sono specifici di un dispositivo (rispetto alla custodia o al raffreddamento del cabinet).</span><span class="sxs-lookup"><span data-stu-id="acc26-104">The **CIM\_AssociatedCooling** association indicates when fans or other cooling devices are specific to a device (versus providing enclosure or cabinet cooling).</span></span>

<span data-ttu-id="acc26-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="acc26-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="acc26-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="acc26-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="acc26-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="acc26-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{306F88F2-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedCooling : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_CoolingDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="acc26-108">Members</span><span class="sxs-lookup"><span data-stu-id="acc26-108">Members</span></span>

<span data-ttu-id="acc26-109">La classe **CIM \_ AssociatedCooling** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="acc26-109">The **CIM\_AssociatedCooling** class has these types of members:</span></span>

-   [<span data-ttu-id="acc26-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="acc26-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="acc26-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="acc26-111">Properties</span></span>

<span data-ttu-id="acc26-112">La classe **CIM \_ AssociatedCooling** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="acc26-112">The **CIM\_AssociatedCooling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="acc26-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="acc26-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acc26-114">Tipo di dati: **CIM \_ CoolingDevice**</span><span class="sxs-lookup"><span data-stu-id="acc26-114">Data type: **CIM\_CoolingDevice**</span></span>
</dt> <dt>

<span data-ttu-id="acc26-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acc26-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acc26-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="acc26-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="acc26-117">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive il dispositivo di raffreddamento.</span><span class="sxs-lookup"><span data-stu-id="acc26-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the cooling device.</span></span>

</dd> <dt>

<span data-ttu-id="acc26-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="acc26-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acc26-119">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="acc26-119">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="acc26-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acc26-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acc26-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="acc26-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="acc26-122">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che fa riferimento al dispositivo logico che si sta raffreddando.</span><span class="sxs-lookup"><span data-stu-id="acc26-122">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that references the logical device being cooled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="acc26-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="acc26-123">Remarks</span></span>

<span data-ttu-id="acc26-124">La classe **CIM \_ AssociatedCooling** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="acc26-124">The **CIM\_AssociatedCooling** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="acc26-125">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="acc26-125">WMI does not implement this class.</span></span>

<span data-ttu-id="acc26-126">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="acc26-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="acc26-127">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="acc26-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="acc26-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="acc26-128">Requirements</span></span>



| <span data-ttu-id="acc26-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="acc26-129">Requirement</span></span> | <span data-ttu-id="acc26-130">Valore</span><span class="sxs-lookup"><span data-stu-id="acc26-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acc26-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acc26-131">Minimum supported client</span></span><br/> | <span data-ttu-id="acc26-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="acc26-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="acc26-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acc26-133">Minimum supported server</span></span><br/> | <span data-ttu-id="acc26-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acc26-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="acc26-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="acc26-135">Namespace</span></span><br/>                | <span data-ttu-id="acc26-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="acc26-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="acc26-137">MOF</span><span class="sxs-lookup"><span data-stu-id="acc26-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="acc26-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="acc26-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="acc26-139">DLL</span><span class="sxs-lookup"><span data-stu-id="acc26-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acc26-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acc26-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acc26-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="acc26-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acc26-142">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="acc26-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

