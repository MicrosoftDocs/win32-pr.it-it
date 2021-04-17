---
description: La \_ classe di associazione CIM installatoos rappresenta un collegamento tra il computer e il sistema operativo installato.
ms.assetid: 6db5b5a2-91b6-4540-83b8-bb9c86c7f94e
ms.tgt_platform: multiple
title: Classe CIM_InstalledOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledOS
- CIM_InstalledOS.PartComponent
- CIM_InstalledOS.GroupComponent
- CIM_InstalledOS.PrimaryOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53e01be6a87fa6e5ef91ad6e8a81dbbddff4a576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523762"
---
# <a name="cim_installedos-class"></a><span data-ttu-id="b551b-103">\_Classe CIM installato</span><span class="sxs-lookup"><span data-stu-id="b551b-103">CIM\_InstalledOS class</span></span>

<span data-ttu-id="b551b-104">La classe di associazione **CIM \_ installatoos** rappresenta un collegamento tra il computer e il sistema operativo installato.</span><span class="sxs-lookup"><span data-stu-id="b551b-104">The **CIM\_InstalledOS** association class represents a link between the computer system and the installed operating system.</span></span> <span data-ttu-id="b551b-105">Un sistema operativo viene installato quando si trova in un ambito di archiviazione del computer (ad esempio, copiato in un'unità disco o scaricato in memoria).</span><span class="sxs-lookup"><span data-stu-id="b551b-105">An operating system is installed when it is in a computer system's storage extent (for example, copied to a disk drive or downloaded to memory).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b551b-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="b551b-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b551b-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b551b-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b551b-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b551b-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b551b-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b551b-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b551b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b551b-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C575-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_InstalledOS : CIM_SystemComponent
{
  CIM_OperatingSystem REF PartComponent;
  CIM_ComputerSystem  REF GroupComponent;
  boolean                 PrimaryOS;
};
```

## <a name="members"></a><span data-ttu-id="b551b-111">Members</span><span class="sxs-lookup"><span data-stu-id="b551b-111">Members</span></span>

<span data-ttu-id="b551b-112">La classe **CIM \_ installatoos** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b551b-112">The **CIM\_InstalledOS** class has these types of members:</span></span>

-   [<span data-ttu-id="b551b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b551b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b551b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b551b-114">Properties</span></span>

<span data-ttu-id="b551b-115">La classe **CIM \_ installatoos** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b551b-115">The **CIM\_InstalledOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b551b-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b551b-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b551b-117">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="b551b-117">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b551b-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b551b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b551b-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="b551b-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b551b-120">Un [**\_ ComputerSystem CIM**](cim-computersystem.md) che descrive il computer.</span><span class="sxs-lookup"><span data-stu-id="b551b-120">A [**CIM\_ComputerSystem**](cim-computersystem.md) describing the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="b551b-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b551b-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b551b-122">Tipo di dati: **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="b551b-122">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b551b-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b551b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b551b-124">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b551b-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b551b-125">Un [**\_ OperatingSystem CIM**](cim-operatingsystem.md) che descrive il sistema operativo installato nel computer.</span><span class="sxs-lookup"><span data-stu-id="b551b-125">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) that describes the operating system installed on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="b551b-126">**Primarie**</span><span class="sxs-lookup"><span data-stu-id="b551b-126">**PrimaryOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b551b-127">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b551b-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b551b-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b551b-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b551b-129">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sistema operativo DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="b551b-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operating System\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="b551b-130">Se **true**, il sistema operativo installato è il sistema operativo predefinito per il computer.</span><span class="sxs-lookup"><span data-stu-id="b551b-130">If **TRUE**, the installed operating system is the default operating system for the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b551b-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="b551b-131">Remarks</span></span>

<span data-ttu-id="b551b-132">La classe **CIM \_ installato** è derivata da [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="b551b-132">The **CIM\_InstalledOS** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="b551b-133">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="b551b-133">WMI does not implement this class.</span></span> <span data-ttu-id="b551b-134">Per le classi derivate da **CIM \_ installato**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b551b-134">For classes derived from **CIM\_InstalledOS**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b551b-135">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="b551b-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b551b-136">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="b551b-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b551b-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b551b-137">Requirements</span></span>



| <span data-ttu-id="b551b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="b551b-138">Requirement</span></span> | <span data-ttu-id="b551b-139">Valore</span><span class="sxs-lookup"><span data-stu-id="b551b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b551b-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b551b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b551b-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b551b-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b551b-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b551b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b551b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b551b-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b551b-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b551b-144">Namespace</span></span><br/>                | <span data-ttu-id="b551b-145">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b551b-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b551b-146">MOF</span><span class="sxs-lookup"><span data-stu-id="b551b-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b551b-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b551b-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b551b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="b551b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b551b-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b551b-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b551b-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b551b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b551b-151">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="b551b-151">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

