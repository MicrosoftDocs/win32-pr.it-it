---
description: La \_ classe CIM DeviceServiceImplementation rappresenta un'associazione tra un servizio e il modo in cui viene implementata.
ms.assetid: 5e2e3975-8338-4bf4-8c73-5be4b93fa2c8
ms.tgt_platform: multiple
title: Classe CIM_DeviceServiceImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceServiceImplementation
- CIM_DeviceServiceImplementation.Dependent
- CIM_DeviceServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ae96d94c95ddda684dbb4d17a2d8eb52fc6ffd4b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966229"
---
# <a name="cim_deviceserviceimplementation-class"></a><span data-ttu-id="c5b0c-103">CIM \_ DeviceServiceImplementation (classe)</span><span class="sxs-lookup"><span data-stu-id="c5b0c-103">CIM\_DeviceServiceImplementation class</span></span>

<span data-ttu-id="c5b0c-104">La classe **CIM \_ DeviceServiceImplementation** rappresenta un'associazione tra un servizio e il modo in cui viene implementata.</span><span class="sxs-lookup"><span data-stu-id="c5b0c-104">The **CIM\_DeviceServiceImplementation** class represents an association between a service and how it is implemented.</span></span> <span data-ttu-id="c5b0c-105">Quando più dispositivi sono associati a un servizio, gli elementi operano insieme per fornire il servizio.</span><span class="sxs-lookup"><span data-stu-id="c5b0c-105">When multiple devices are associated with one service, the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="c5b0c-106">Se esistono implementazioni diverse di un servizio, ogni implementazione produce singole creazioni di istanze dell'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="c5b0c-106">If different implementations of a service exist, each implementation results in individual instantiations of the service object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5b0c-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="c5b0c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c5b0c-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c5b0c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c5b0c-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c5b0c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c5b0c-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="c5b0c-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5b0c-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5b0c-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{290FC242-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceServiceImplementation : CIM_Dependency
{
  CIM_Service       REF Dependent;
  CIM_LogicalDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="c5b0c-112">Members</span><span class="sxs-lookup"><span data-stu-id="c5b0c-112">Members</span></span>

<span data-ttu-id="c5b0c-113">La classe **CIM \_ DeviceServiceImplementation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c5b0c-113">The **CIM\_DeviceServiceImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="c5b0c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c5b0c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5b0c-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c5b0c-115">Properties</span></span>

<span data-ttu-id="c5b0c-116">La classe **CIM \_ DeviceServiceImplementation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c5b0c-116">The **CIM\_DeviceServiceImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5b0c-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="c5b0c-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5b0c-118">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="c5b0c-118">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="c5b0c-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5b0c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5b0c-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="c5b0c-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c5b0c-121">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="c5b0c-121">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="c5b0c-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="c5b0c-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5b0c-123">Tipo di dati **: \_ servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="c5b0c-123">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="c5b0c-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5b0c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5b0c-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="c5b0c-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c5b0c-126">[**\_ Servizio CIM**](cim-service.md) che descrive il servizio implementato utilizzando il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="c5b0c-126">A [**CIM\_Service**](cim-service.md) that describes the service implemented using the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5b0c-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5b0c-127">Remarks</span></span>

<span data-ttu-id="c5b0c-128">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="c5b0c-128">WMI does not implement this class.</span></span>

<span data-ttu-id="c5b0c-129">La classe **CIM \_ DeviceServiceImplementation** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="c5b0c-129">The **CIM\_DeviceServiceImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="c5b0c-130">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="c5b0c-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c5b0c-131">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="c5b0c-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5b0c-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5b0c-132">Requirements</span></span>



| <span data-ttu-id="c5b0c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5b0c-133">Requirement</span></span> | <span data-ttu-id="c5b0c-134">Valore</span><span class="sxs-lookup"><span data-stu-id="c5b0c-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b0c-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5b0c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c5b0c-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5b0c-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c5b0c-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5b0c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c5b0c-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5b0c-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5b0c-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c5b0c-139">Namespace</span></span><br/>                | <span data-ttu-id="c5b0c-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c5b0c-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c5b0c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="c5b0c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5b0c-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5b0c-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5b0c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="c5b0c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5b0c-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5b0c-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5b0c-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5b0c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5b0c-146">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="c5b0c-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

