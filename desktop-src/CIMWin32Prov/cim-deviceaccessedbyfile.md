---
description: La \_ classe di associazione CIM DeviceAccessedByFile specifica il dispositivo logico a cui si accede tramite la classe CIM DeviceFile a cui si fa riferimento \_ .
ms.assetid: 8ba44f40-8b84-4f5c-b719-aded10877654
ms.tgt_platform: multiple
title: Classe CIM_DeviceAccessedByFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceAccessedByFile
- CIM_DeviceAccessedByFile.Dependent
- CIM_DeviceAccessedByFile.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cf84d2e7943dfe6da88f81ef6963190553f028e7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877913"
---
# <a name="cim_deviceaccessedbyfile-class"></a><span data-ttu-id="78b1f-103">CIM \_ DeviceAccessedByFile (classe)</span><span class="sxs-lookup"><span data-stu-id="78b1f-103">CIM\_DeviceAccessedByFile class</span></span>

<span data-ttu-id="78b1f-104">La classe di associazione **CIM \_ DeviceAccessedByFile** specifica il dispositivo logico a cui si accede tramite la classe [**CIM \_ DeviceFile**](cim-devicefile.md) a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="78b1f-104">The **CIM\_DeviceAccessedByFile** association class specifies the logical device accessed by using the referenced [**CIM\_DeviceFile**](cim-devicefile.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78b1f-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="78b1f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="78b1f-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="78b1f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="78b1f-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="78b1f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="78b1f-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="78b1f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="78b1f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78b1f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{05D1FFF2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceAccessedByFile : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_DeviceFile    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="78b1f-110">Members</span><span class="sxs-lookup"><span data-stu-id="78b1f-110">Members</span></span>

<span data-ttu-id="78b1f-111">La classe **CIM \_ DeviceAccessedByFile** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="78b1f-111">The **CIM\_DeviceAccessedByFile** class has these types of members:</span></span>

-   [<span data-ttu-id="78b1f-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="78b1f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78b1f-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="78b1f-113">Properties</span></span>

<span data-ttu-id="78b1f-114">La classe **CIM \_ DeviceAccessedByFile** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="78b1f-114">The **CIM\_DeviceAccessedByFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78b1f-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="78b1f-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b1f-116">Tipo di dati: **CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="78b1f-116">Data type: **CIM\_DeviceFile**</span></span>
</dt> <dt>

<span data-ttu-id="78b1f-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="78b1f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b1f-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="78b1f-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="78b1f-119">Un [**\_ DeviceFile CIM**](cim-devicefile.md) che descrive il file del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78b1f-119">A [**CIM\_DeviceFile**](cim-devicefile.md) that describes the device file.</span></span>

</dd> <dt>

<span data-ttu-id="78b1f-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="78b1f-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b1f-121">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="78b1f-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="78b1f-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="78b1f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b1f-123">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="78b1f-123">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="78b1f-124">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive il dispositivo A cui si accede tramite il file del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78b1f-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the device that is accessed using the device file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78b1f-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="78b1f-125">Remarks</span></span>

<span data-ttu-id="78b1f-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="78b1f-126">WMI does not implement this class.</span></span>

<span data-ttu-id="78b1f-127">La classe **CIM \_ DeviceAccessedByFile** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="78b1f-127">The **CIM\_DeviceAccessedByFile** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="78b1f-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="78b1f-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="78b1f-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="78b1f-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="78b1f-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78b1f-130">Requirements</span></span>



| <span data-ttu-id="78b1f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="78b1f-131">Requirement</span></span> | <span data-ttu-id="78b1f-132">Valore</span><span class="sxs-lookup"><span data-stu-id="78b1f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78b1f-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78b1f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="78b1f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78b1f-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="78b1f-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78b1f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="78b1f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78b1f-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="78b1f-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="78b1f-137">Namespace</span></span><br/>                | <span data-ttu-id="78b1f-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="78b1f-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="78b1f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="78b1f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78b1f-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78b1f-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="78b1f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="78b1f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78b1f-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78b1f-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78b1f-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78b1f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78b1f-144">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="78b1f-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

