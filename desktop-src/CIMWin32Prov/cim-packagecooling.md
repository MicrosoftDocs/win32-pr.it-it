---
description: L' \_ associazione CIM PackageCooling rappresenta la relazione in cui un dispositivo di raffreddamento viene installato in un pacchetto, ad esempio uno chassis o un rack, per facilitare il raffreddamento del pacchetto.
ms.assetid: 0aaae8e1-6e70-4b26-8e56-dac5657e58c1
ms.tgt_platform: multiple
title: Classe CIM_PackageCooling
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageCooling
- CIM_PackageCooling.Dependent
- CIM_PackageCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f88cd3f07983870bed8fd2d740f3bf9051019b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523738"
---
# <a name="cim_packagecooling-class"></a><span data-ttu-id="ea35a-103">CIM \_ PackageCooling (classe)</span><span class="sxs-lookup"><span data-stu-id="ea35a-103">CIM\_PackageCooling class</span></span>

<span data-ttu-id="ea35a-104">L'associazione **CIM \_ PackageCooling** rappresenta la relazione in cui un dispositivo di raffreddamento viene installato in un pacchetto, ad esempio uno chassis o un rack, per facilitare il raffreddamento del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="ea35a-104">The **CIM\_PackageCooling** association represents the relationship in which a cooling device is installed in a package, such as a chassis or rack, to assist with the package's cooling.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea35a-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ea35a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ea35a-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ea35a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ea35a-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ea35a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ea35a-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ea35a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea35a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea35a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageCooling : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_CoolingDevice   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="ea35a-110">Members</span><span class="sxs-lookup"><span data-stu-id="ea35a-110">Members</span></span>

<span data-ttu-id="ea35a-111">La classe **CIM \_ PackageCooling** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ea35a-111">The **CIM\_PackageCooling** class has these types of members:</span></span>

-   [<span data-ttu-id="ea35a-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ea35a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea35a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ea35a-113">Properties</span></span>

<span data-ttu-id="ea35a-114">La classe **CIM \_ PackageCooling** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea35a-114">The **CIM\_PackageCooling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea35a-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="ea35a-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea35a-116">Tipo di dati: **CIM \_ CoolingDevice**</span><span class="sxs-lookup"><span data-stu-id="ea35a-116">Data type: **CIM\_CoolingDevice**</span></span>
</dt> <dt>

<span data-ttu-id="ea35a-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea35a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea35a-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="ea35a-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ea35a-119">Un [**\_ CoolingDevice CIM**](cim-coolingdevice.md) che descrive il dispositivo di raffreddamento per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="ea35a-119">A [**CIM\_CoolingDevice**](cim-coolingdevice.md) that describes the cooling device for the package.</span></span>

</dd> <dt>

<span data-ttu-id="ea35a-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="ea35a-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea35a-121">Tipo di dati: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="ea35a-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="ea35a-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ea35a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea35a-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="ea35a-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ea35a-124">Un [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) che descrive il pacchetto fisico il cui ambiente è raffreddato.</span><span class="sxs-lookup"><span data-stu-id="ea35a-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package whose environment is cooled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea35a-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea35a-125">Remarks</span></span>

<span data-ttu-id="ea35a-126">**CIM \_ PackageCooling** è derivato dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="ea35a-126">**CIM\_PackageCooling** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="ea35a-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ea35a-127">WMI does not implement this class.</span></span>

<span data-ttu-id="ea35a-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ea35a-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ea35a-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ea35a-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea35a-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea35a-130">Requirements</span></span>



| <span data-ttu-id="ea35a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea35a-131">Requirement</span></span> | <span data-ttu-id="ea35a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ea35a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea35a-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea35a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ea35a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea35a-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ea35a-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea35a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ea35a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea35a-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ea35a-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ea35a-137">Namespace</span></span><br/>                | <span data-ttu-id="ea35a-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ea35a-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ea35a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ea35a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea35a-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea35a-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea35a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ea35a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea35a-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea35a-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea35a-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea35a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea35a-144">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="ea35a-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

