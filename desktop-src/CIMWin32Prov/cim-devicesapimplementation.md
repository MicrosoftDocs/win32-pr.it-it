---
description: La \_ classe CIM DeviceSAPImplementation rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il modo in cui viene implementato.
ms.assetid: 6c059507-bfc0-4630-9b39-9c4bae2bf138
ms.tgt_platform: multiple
title: Classe CIM_DeviceSAPImplementation (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Dependent
- CIM_DeviceSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eadc1e42427c06717c7b0d7a13aba8a2a71ccddb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748698"
---
# <a name="cim_devicesapimplementation-class-cimwin32-wmi-providers"></a><span data-ttu-id="88ac2-103">Classe CIM_DeviceSAPImplementation (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="88ac2-103">CIM_DeviceSAPImplementation class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="88ac2-104">La classe **CIM \_ DeviceSAPImplementation** rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il modo in cui viene implementato.</span><span class="sxs-lookup"><span data-stu-id="88ac2-104">The **CIM\_DeviceSAPImplementation** class represents an association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="88ac2-105">Quando molti dispositivi logici sono associati a un SAP, gli elementi operano insieme per fornire il punto di accesso.</span><span class="sxs-lookup"><span data-stu-id="88ac2-105">When many logical devices are associated with one SAP, the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="88ac2-106">Se esistono implementazioni diverse di un SAP, ogni implementazione genera singole creazioni di istanze dell'oggetto SAP.</span><span class="sxs-lookup"><span data-stu-id="88ac2-106">If different implementations of a SAP exist, each implementation results in individual instantiations of the SAP object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88ac2-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="88ac2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="88ac2-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="88ac2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="88ac2-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="88ac2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="88ac2-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="88ac2-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ac2-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88ac2-111">Syntax</span></span>

``` syntax
[UUID("{1BE949DA-DB36-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_LogicalDevice      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="88ac2-112">Members</span><span class="sxs-lookup"><span data-stu-id="88ac2-112">Members</span></span>

<span data-ttu-id="88ac2-113">La classe **CIM \_ DeviceSAPImplementation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="88ac2-113">The **CIM\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="88ac2-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="88ac2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88ac2-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="88ac2-115">Properties</span></span>

<span data-ttu-id="88ac2-116">La classe **CIM \_ DeviceSAPImplementation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="88ac2-116">The **CIM\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88ac2-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="88ac2-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ac2-118">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="88ac2-118">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="88ac2-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="88ac2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ac2-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="88ac2-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="88ac2-121">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="88ac2-121">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="88ac2-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="88ac2-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ac2-123">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="88ac2-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="88ac2-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="88ac2-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ac2-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="88ac2-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="88ac2-126">Un [**\_ serviceAccessPoint CIM**](cim-serviceaccesspoint.md) che descrive il punto di accesso al servizio implementato usando il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="88ac2-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88ac2-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="88ac2-127">Remarks</span></span>

<span data-ttu-id="88ac2-128">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="88ac2-128">WMI does not implement this class.</span></span>

<span data-ttu-id="88ac2-129">La classe **CIM \_ DeviceSAPImplementation** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="88ac2-129">The **CIM\_DeviceSAPImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="88ac2-130">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="88ac2-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="88ac2-131">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="88ac2-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="88ac2-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88ac2-132">Requirements</span></span>



| <span data-ttu-id="88ac2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="88ac2-133">Requirement</span></span> | <span data-ttu-id="88ac2-134">Valore</span><span class="sxs-lookup"><span data-stu-id="88ac2-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88ac2-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88ac2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="88ac2-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88ac2-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88ac2-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88ac2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="88ac2-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88ac2-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88ac2-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="88ac2-139">Namespace</span></span><br/>                | <span data-ttu-id="88ac2-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="88ac2-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="88ac2-141">MOF</span><span class="sxs-lookup"><span data-stu-id="88ac2-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88ac2-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88ac2-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="88ac2-143">DLL</span><span class="sxs-lookup"><span data-stu-id="88ac2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88ac2-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88ac2-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ac2-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88ac2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ac2-146">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="88ac2-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

