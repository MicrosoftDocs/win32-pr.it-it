---
description: L' \_ associazione CIM SoftwareFeatureSoftwareElements identifica gli elementi software che costituiscono una funzionalità software specifica.
ms.assetid: 933586c5-b85e-4136-b557-5151a48abc32
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeatureSoftwareElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSoftwareElements
- CIM_SoftwareFeatureSoftwareElements.PartComponent
- CIM_SoftwareFeatureSoftwareElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71712ebb3f8bf2ab2067325f16cf31af7fb1dc38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304486"
---
# <a name="cim_softwarefeaturesoftwareelements-class"></a><span data-ttu-id="dfb2f-103">CIM \_ SoftwareFeatureSoftwareElements (classe)</span><span class="sxs-lookup"><span data-stu-id="dfb2f-103">CIM\_SoftwareFeatureSoftwareElements class</span></span>

<span data-ttu-id="dfb2f-104">L'associazione **CIM \_ SoftwareFeatureSoftwareElements** identifica gli elementi software che costituiscono una funzionalità software specifica.</span><span class="sxs-lookup"><span data-stu-id="dfb2f-104">The **CIM\_SoftwareFeatureSoftwareElements** association identifies the software elements that make up a specific software feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dfb2f-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="dfb2f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dfb2f-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dfb2f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dfb2f-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="dfb2f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dfb2f-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="dfb2f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb2f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dfb2f-109">Syntax</span></span>

``` syntax
[UUID("{A91081E2-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSoftwareElements : CIM_Component
{
  CIM_SoftwareElement REF PartComponent;
  CIM_SoftwareFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="dfb2f-110">Members</span><span class="sxs-lookup"><span data-stu-id="dfb2f-110">Members</span></span>

<span data-ttu-id="dfb2f-111">La classe **CIM \_ SoftwareFeatureSoftwareElements** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dfb2f-111">The **CIM\_SoftwareFeatureSoftwareElements** class has these types of members:</span></span>

-   [<span data-ttu-id="dfb2f-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dfb2f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dfb2f-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dfb2f-113">Properties</span></span>

<span data-ttu-id="dfb2f-114">La classe **CIM \_ SoftwareFeatureSoftwareElements** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dfb2f-114">The **CIM\_SoftwareFeatureSoftwareElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dfb2f-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="dfb2f-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb2f-116">Tipo di dati: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="dfb2f-116">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="dfb2f-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dfb2f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb2f-118">Qualificatori: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dfb2f-118">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dfb2f-119">Componente del gruppo.</span><span class="sxs-lookup"><span data-stu-id="dfb2f-119">The group component.</span></span>

<span data-ttu-id="dfb2f-120">Questa proprietà viene ereditata [**dal \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="dfb2f-120">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfb2f-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="dfb2f-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb2f-122">Tipo di dati: **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="dfb2f-122">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="dfb2f-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dfb2f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfb2f-124">Componente della parte.</span><span class="sxs-lookup"><span data-stu-id="dfb2f-124">The part component.</span></span>

<span data-ttu-id="dfb2f-125">Questa proprietà viene ereditata [**dal \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="dfb2f-125">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dfb2f-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="dfb2f-126">Remarks</span></span>

<span data-ttu-id="dfb2f-127">L'associazione **CIM \_ SoftwareFeatureSoftwareElements** è derivata dal [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="dfb2f-127">The **CIM\_SoftwareFeatureSoftwareElements** association is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="dfb2f-128">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="dfb2f-128">WMI does not implement this class.</span></span> <span data-ttu-id="dfb2f-129">Per le classi WMI derivate da **CIM \_ SoftwareFeatureSoftwareElements**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="dfb2f-129">For WMI classes derived from **CIM\_SoftwareFeatureSoftwareElements**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="dfb2f-130">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="dfb2f-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dfb2f-131">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="dfb2f-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfb2f-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfb2f-132">Requirements</span></span>



| <span data-ttu-id="dfb2f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfb2f-133">Requirement</span></span> | <span data-ttu-id="dfb2f-134">Valore</span><span class="sxs-lookup"><span data-stu-id="dfb2f-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb2f-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfb2f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dfb2f-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfb2f-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dfb2f-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfb2f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dfb2f-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfb2f-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dfb2f-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dfb2f-139">Namespace</span></span><br/>                | <span data-ttu-id="dfb2f-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="dfb2f-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dfb2f-141">MOF</span><span class="sxs-lookup"><span data-stu-id="dfb2f-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfb2f-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfb2f-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dfb2f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="dfb2f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfb2f-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfb2f-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfb2f-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dfb2f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb2f-146">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="dfb2f-146">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

