---
description: La \_ classe CIM OperatingSystemSoftwareFeature rappresenta le funzionalità software che costituiscono il sistema operativo.
ms.assetid: 9ffc709c-213e-4252-9662-76f01e1685e5
ms.tgt_platform: multiple
title: Classe CIM_OperatingSystemSoftwareFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystemSoftwareFeature
- CIM_OperatingSystemSoftwareFeature.PartComponent
- CIM_OperatingSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b9d74478f211b23e103854cedb09a1e0186618b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304974"
---
# <a name="cim_operatingsystemsoftwarefeature-class"></a><span data-ttu-id="29356-103">CIM \_ OperatingSystemSoftwareFeature (classe)</span><span class="sxs-lookup"><span data-stu-id="29356-103">CIM\_OperatingSystemSoftwareFeature class</span></span>

<span data-ttu-id="29356-104">La classe **CIM \_ OperatingSystemSoftwareFeature** rappresenta le funzionalità software che costituiscono il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="29356-104">The **CIM\_OperatingSystemSoftwareFeature** class represents the software features that make up the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="29356-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="29356-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="29356-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="29356-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="29356-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="29356-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="29356-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="29356-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="29356-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29356-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{96B4C734-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_OperatingSystemSoftwareFeature : CIM_Component
{
  CIM_SoftwareFeature REF PartComponent;
  CIM_OperatingSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="29356-110">Members</span><span class="sxs-lookup"><span data-stu-id="29356-110">Members</span></span>

<span data-ttu-id="29356-111">La classe **CIM \_ OperatingSystemSoftwareFeature** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="29356-111">The **CIM\_OperatingSystemSoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="29356-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="29356-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29356-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="29356-113">Properties</span></span>

<span data-ttu-id="29356-114">La classe **CIM \_ OperatingSystemSoftwareFeature** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="29356-114">The **CIM\_OperatingSystemSoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29356-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="29356-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29356-116">Tipo di dati: **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="29356-116">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="29356-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29356-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29356-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="29356-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="29356-119">Un [**\_ OperatingSystem CIM**](cim-operatingsystem.md) che descrive il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="29356-119">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) describing the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="29356-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="29356-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29356-121">Tipo di dati: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="29356-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="29356-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29356-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29356-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="29356-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="29356-124">Un [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) che descrive le funzionalità software che costituiscono il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="29356-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) describing the software features that make up the operating system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29356-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="29356-125">Remarks</span></span>

<span data-ttu-id="29356-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="29356-126">WMI does not implement this class.</span></span>

<span data-ttu-id="29356-127">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="29356-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="29356-128">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="29356-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="29356-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29356-129">Requirements</span></span>



| <span data-ttu-id="29356-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="29356-130">Requirement</span></span> | <span data-ttu-id="29356-131">Valore</span><span class="sxs-lookup"><span data-stu-id="29356-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29356-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29356-132">Minimum supported client</span></span><br/> | <span data-ttu-id="29356-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29356-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="29356-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29356-134">Minimum supported server</span></span><br/> | <span data-ttu-id="29356-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29356-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="29356-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="29356-136">Namespace</span></span><br/>                | <span data-ttu-id="29356-137">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="29356-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="29356-138">MOF</span><span class="sxs-lookup"><span data-stu-id="29356-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29356-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29356-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="29356-140">DLL</span><span class="sxs-lookup"><span data-stu-id="29356-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29356-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29356-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29356-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29356-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29356-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="29356-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

