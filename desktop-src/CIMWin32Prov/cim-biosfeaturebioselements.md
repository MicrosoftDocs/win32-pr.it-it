---
description: La \_ classe CIM BIOSFeatureBIOSElements associa una funzionalità BIOS e i relativi elementi BIOS aggregati.
ms.assetid: 84ebd6d0-af42-4e82-bad3-1f934789cbfe
ms.tgt_platform: multiple
title: Classe CIM_BIOSFeatureBIOSElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSFeatureBIOSElements
- CIM_BIOSFeatureBIOSElements.PartComponent
- CIM_BIOSFeatureBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a4eecea97b4d82fadcdc521d378b5b32d986b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127198"
---
# <a name="cim_biosfeaturebioselements-class"></a><span data-ttu-id="4f265-103">CIM \_ BIOSFeatureBIOSElements (classe)</span><span class="sxs-lookup"><span data-stu-id="4f265-103">CIM\_BIOSFeatureBIOSElements class</span></span>

<span data-ttu-id="4f265-104">La classe **CIM \_ BIOSFeatureBIOSElements** associa una funzionalità BIOS e i relativi elementi BIOS aggregati.</span><span class="sxs-lookup"><span data-stu-id="4f265-104">The **CIM\_BIOSFeatureBIOSElements** class associates a BIOS feature and its aggregated BIOS elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f265-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4f265-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4f265-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4f265-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4f265-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4f265-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4f265-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="4f265-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f265-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f265-109">Syntax</span></span>

``` syntax
[UUID("{42B2EC5C-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BIOSFeatureBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_BIOSElement REF PartComponent;
  CIM_BIOSFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="4f265-110">Members</span><span class="sxs-lookup"><span data-stu-id="4f265-110">Members</span></span>

<span data-ttu-id="4f265-111">La classe **CIM \_ BIOSFeatureBIOSElements** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4f265-111">The **CIM\_BIOSFeatureBIOSElements** class has these types of members:</span></span>

-   [<span data-ttu-id="4f265-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4f265-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f265-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4f265-113">Properties</span></span>

<span data-ttu-id="4f265-114">La classe **CIM \_ BIOSFeatureBIOSElements** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4f265-114">The **CIM\_BIOSFeatureBIOSElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f265-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4f265-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f265-116">Tipo di dati: **CIM \_ BIOSFeature**</span><span class="sxs-lookup"><span data-stu-id="4f265-116">Data type: **CIM\_BIOSFeature**</span></span>
</dt> <dt>

<span data-ttu-id="4f265-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f265-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f265-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="4f265-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4f265-119">Un [**\_ BIOSFeature CIM**](cim-biosfeature.md) che descrive la funzionalità BIOS.</span><span class="sxs-lookup"><span data-stu-id="4f265-119">A [**CIM\_BIOSFeature**](cim-biosfeature.md) that describes the BIOS feature.</span></span>

</dd> <dt>

<span data-ttu-id="4f265-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4f265-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f265-121">Tipo di dati: **CIM \_ bioselement**</span><span class="sxs-lookup"><span data-stu-id="4f265-121">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="4f265-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f265-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f265-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="4f265-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4f265-124">Oggetto [**CIM \_ bioselement**](cim-bioselement.md) che descrive l'elemento BIOS che implementa le funzionalità descritte dalla funzionalità BIOS.</span><span class="sxs-lookup"><span data-stu-id="4f265-124">A [**CIM\_BIOSElement**](cim-bioselement.md) that describes the BIOS element that implements the capabilities described by BIOS feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f265-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f265-125">Remarks</span></span>

<span data-ttu-id="4f265-126">La classe **CIM \_ BIOSFeatureBIOSElements** è derivata da [**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span><span class="sxs-lookup"><span data-stu-id="4f265-126">The **CIM\_BIOSFeatureBIOSElements** class is derived from [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span></span>

<span data-ttu-id="4f265-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="4f265-127">WMI does not implement this class.</span></span>

<span data-ttu-id="4f265-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="4f265-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4f265-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="4f265-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f265-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f265-130">Requirements</span></span>



| <span data-ttu-id="4f265-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f265-131">Requirement</span></span> | <span data-ttu-id="4f265-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4f265-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f265-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f265-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4f265-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f265-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f265-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f265-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4f265-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f265-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f265-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4f265-137">Namespace</span></span><br/>                | <span data-ttu-id="4f265-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4f265-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4f265-139">MOF</span><span class="sxs-lookup"><span data-stu-id="4f265-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f265-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f265-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f265-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4f265-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f265-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f265-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f265-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f265-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f265-144">**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="4f265-144">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

