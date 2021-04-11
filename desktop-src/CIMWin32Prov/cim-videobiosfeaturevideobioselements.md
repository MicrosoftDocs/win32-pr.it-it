---
description: La \_ classe CIM VideoBIOSFeatureVideoBIOSElements associa una funzionalità BIOS video e i relativi elementi BIOS video aggregati.
ms.assetid: f1419505-213f-450e-8c96-45f547dd71da
ms.tgt_platform: multiple
title: Classe CIM_VideoBIOSFeatureVideoBIOSElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeatureVideoBIOSElements
- CIM_VideoBIOSFeatureVideoBIOSElements.PartComponent
- CIM_VideoBIOSFeatureVideoBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 421b6814499240b3364ac1aed622e2b7c96e7313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126654"
---
# <a name="cim_videobiosfeaturevideobioselements-class"></a><span data-ttu-id="f1274-103">CIM \_ VideoBIOSFeatureVideoBIOSElements (classe)</span><span class="sxs-lookup"><span data-stu-id="f1274-103">CIM\_VideoBIOSFeatureVideoBIOSElements class</span></span>

<span data-ttu-id="f1274-104">La classe **CIM \_ VideoBIOSFeatureVideoBIOSElements** associa una funzionalità BIOS video e i relativi elementi BIOS video aggregati.</span><span class="sxs-lookup"><span data-stu-id="f1274-104">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class associates a video BIOS feature and its aggregated video BIOS elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1274-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f1274-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f1274-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f1274-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f1274-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f1274-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f1274-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f1274-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1274-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1274-109">Syntax</span></span>

``` syntax
[UUID("{B3F86390-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeatureVideoBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_VideoBIOSElement REF PartComponent;
  CIM_VideoBIOSFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="f1274-110">Members</span><span class="sxs-lookup"><span data-stu-id="f1274-110">Members</span></span>

<span data-ttu-id="f1274-111">La classe **CIM \_ VideoBIOSFeatureVideoBIOSElements** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f1274-111">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class has these types of members:</span></span>

-   [<span data-ttu-id="f1274-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1274-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1274-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1274-113">Properties</span></span>

<span data-ttu-id="f1274-114">La classe **CIM \_ VideoBIOSFeatureVideoBIOSElements** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f1274-114">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1274-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f1274-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1274-116">Tipo di dati: **CIM \_ VideoBIOSFeature**</span><span class="sxs-lookup"><span data-stu-id="f1274-116">Data type: **CIM\_VideoBIOSFeature**</span></span>
</dt> <dt>

<span data-ttu-id="f1274-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1274-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1274-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="f1274-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="f1274-119">Un [**\_ VideoBIOSFeature CIM**](cim-videobiosfeature.md) che descrive la funzionalità del BIOS video.</span><span class="sxs-lookup"><span data-stu-id="f1274-119">A [**CIM\_VideoBIOSFeature**](cim-videobiosfeature.md) that describes the video BIOS feature.</span></span>

</dd> <dt>

<span data-ttu-id="f1274-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f1274-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1274-121">Tipo di dati: **CIM \_ VideoBIOSElement**</span><span class="sxs-lookup"><span data-stu-id="f1274-121">Data type: **CIM\_VideoBIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="f1274-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1274-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1274-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="f1274-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="f1274-124">Un [**\_ VideoBIOSElement CIM**](cim-videobioselement.md) che descrive l'elemento video BIOS che implementa le funzionalità descritte dalla funzionalità BIOS video.</span><span class="sxs-lookup"><span data-stu-id="f1274-124">A [**CIM\_VideoBIOSElement**](cim-videobioselement.md) that describes the video BIOS element that implements the capabilities described by video BIOS feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1274-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1274-125">Remarks</span></span>

<span data-ttu-id="f1274-126">La classe **CIM \_ VideoBIOSFeatureVideoBIOSElements** è derivata da [**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span><span class="sxs-lookup"><span data-stu-id="f1274-126">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class is derived from [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span></span>

<span data-ttu-id="f1274-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="f1274-127">WMI does not implement this class.</span></span>

<span data-ttu-id="f1274-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f1274-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f1274-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f1274-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1274-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1274-130">Requirements</span></span>



| <span data-ttu-id="f1274-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1274-131">Requirement</span></span> | <span data-ttu-id="f1274-132">Valore</span><span class="sxs-lookup"><span data-stu-id="f1274-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1274-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1274-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f1274-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1274-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1274-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1274-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f1274-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1274-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1274-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f1274-137">Namespace</span></span><br/>                | <span data-ttu-id="f1274-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f1274-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f1274-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f1274-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1274-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1274-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1274-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f1274-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1274-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1274-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1274-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1274-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1274-144">**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="f1274-144">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

