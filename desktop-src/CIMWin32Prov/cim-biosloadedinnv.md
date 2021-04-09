---
description: La \_ classe CIM BIOSLoadedInNV associa un elemento BIOS e l'archiviazione non volatile in cui viene caricata.
ms.assetid: 11641616-e11d-49ff-bfe4-f95fe27f00b8
ms.tgt_platform: multiple
title: Classe CIM_BIOSLoadedInNV
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSLoadedInNV
- CIM_BIOSLoadedInNV.Dependent
- CIM_BIOSLoadedInNV.Antecedent
- CIM_BIOSLoadedInNV.EndingAddress
- CIM_BIOSLoadedInNV.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0de07e1d4b886ad14f6a7fd8dbb96c1c0f2d2079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966211"
---
# <a name="cim_biosloadedinnv-class"></a><span data-ttu-id="cbdc5-103">CIM \_ BIOSLoadedInNV (classe)</span><span class="sxs-lookup"><span data-stu-id="cbdc5-103">CIM\_BIOSLoadedInNV class</span></span>

<span data-ttu-id="cbdc5-104">La classe **CIM \_ BIOSLoadedInNV** associa un elemento BIOS e l'archiviazione non volatile in cui viene caricata.</span><span class="sxs-lookup"><span data-stu-id="cbdc5-104">The **CIM\_BIOSLoadedInNV** class associates a BIOS element and the non-volatile storage in which it is loaded.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cbdc5-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="cbdc5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cbdc5-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cbdc5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cbdc5-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cbdc5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cbdc5-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="cbdc5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbdc5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cbdc5-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{524ED194-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BIOSLoadedInNV : CIM_Dependency
{
  CIM_BIOSElement        REF Dependent;
  CIM_NonVolatileStorage REF Antecedent;
  uint64                     EndingAddress;
  uint64                     StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="cbdc5-110">Members</span><span class="sxs-lookup"><span data-stu-id="cbdc5-110">Members</span></span>

<span data-ttu-id="cbdc5-111">La classe **CIM \_ BIOSLoadedInNV** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cbdc5-111">The **CIM\_BIOSLoadedInNV** class has these types of members:</span></span>

-   [<span data-ttu-id="cbdc5-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cbdc5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cbdc5-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cbdc5-113">Properties</span></span>

<span data-ttu-id="cbdc5-114">La classe **CIM \_ BIOSLoadedInNV** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cbdc5-114">The **CIM\_BIOSLoadedInNV** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cbdc5-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="cbdc5-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbdc5-116">Tipo di dati: **CIM \_ NonVolatileStorage**</span><span class="sxs-lookup"><span data-stu-id="cbdc5-116">Data type: **CIM\_NonVolatileStorage**</span></span>
</dt> <dt>

<span data-ttu-id="cbdc5-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbdc5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbdc5-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="cbdc5-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="cbdc5-119">Un [**\_ NonVolatileStorage CIM**](cim-nonvolatilestorage.md) che descrive l'archiviazione non volatile.</span><span class="sxs-lookup"><span data-stu-id="cbdc5-119">A [**CIM\_NonVolatileStorage**](cim-nonvolatilestorage.md) that describes the non-volatile storage.</span></span>

</dd> <dt>

<span data-ttu-id="cbdc5-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="cbdc5-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbdc5-121">Tipo di dati: **CIM \_ bioselement**</span><span class="sxs-lookup"><span data-stu-id="cbdc5-121">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="cbdc5-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbdc5-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbdc5-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="cbdc5-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="cbdc5-124">Oggetto [**CIM \_ bioselement**](cim-bioselement.md) che descrive il BIOS archiviato nell'extent non volatile.</span><span class="sxs-lookup"><span data-stu-id="cbdc5-124">A [**CIM\_BIOSElement**](cim-bioselement.md) that describes the BIOS stored in the non-volatile extent.</span></span>

</dd> <dt>

<span data-ttu-id="cbdc5-125">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="cbdc5-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbdc5-126">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cbdc5-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cbdc5-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbdc5-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbdc5-128">Indirizzo finale in cui il BIOS si trova in una risorsa di archiviazione non volatile.</span><span class="sxs-lookup"><span data-stu-id="cbdc5-128">Ending address where the BIOS is located in non-volatile storage.</span></span>

<span data-ttu-id="cbdc5-129">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cbdc5-129">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="cbdc5-130">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="cbdc5-130">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbdc5-131">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cbdc5-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cbdc5-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbdc5-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbdc5-133">Indirizzo iniziale in cui il BIOS si trova in una risorsa di archiviazione non volatile.</span><span class="sxs-lookup"><span data-stu-id="cbdc5-133">Starting address where the BIOS is located in non-volatile storage.</span></span>

<span data-ttu-id="cbdc5-134">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cbdc5-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbdc5-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="cbdc5-135">Remarks</span></span>

<span data-ttu-id="cbdc5-136">La classe **CIM \_ BIOSLoadedInNV** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="cbdc5-136">The **CIM\_BIOSLoadedInNV** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="cbdc5-137">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="cbdc5-137">WMI does not implement this class.</span></span>

<span data-ttu-id="cbdc5-138">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="cbdc5-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cbdc5-139">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="cbdc5-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbdc5-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbdc5-140">Requirements</span></span>



| <span data-ttu-id="cbdc5-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbdc5-141">Requirement</span></span> | <span data-ttu-id="cbdc5-142">Valore</span><span class="sxs-lookup"><span data-stu-id="cbdc5-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbdc5-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbdc5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="cbdc5-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbdc5-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cbdc5-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbdc5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="cbdc5-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbdc5-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cbdc5-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cbdc5-147">Namespace</span></span><br/>                | <span data-ttu-id="cbdc5-148">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="cbdc5-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cbdc5-149">MOF</span><span class="sxs-lookup"><span data-stu-id="cbdc5-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbdc5-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cbdc5-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbdc5-151">DLL</span><span class="sxs-lookup"><span data-stu-id="cbdc5-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbdc5-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbdc5-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbdc5-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbdc5-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbdc5-154">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="cbdc5-154">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

