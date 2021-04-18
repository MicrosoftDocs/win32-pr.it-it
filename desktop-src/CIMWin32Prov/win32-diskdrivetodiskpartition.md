---
description: La \_ classe WMI dell'associazione DiskDriveToDiskPartition Win32 mette in correlazione un'unità disco e una partizione esistente.
ms.assetid: 82953097-ebfb-42b8-84b4-fb4ed19f3525
ms.tgt_platform: multiple
title: Classe Win32_DiskDriveToDiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDriveToDiskPartition
- Win32_DiskDriveToDiskPartition.Antecedent
- Win32_DiskDriveToDiskPartition.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2bd5472bd4ad92ddde47f7d6a492916006a80cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305095"
---
# <a name="win32_diskdrivetodiskpartition-class"></a><span data-ttu-id="f8b04-103">Win32 \_ DiskDriveToDiskPartition (classe)</span><span class="sxs-lookup"><span data-stu-id="f8b04-103">Win32\_DiskDriveToDiskPartition class</span></span>

<span data-ttu-id="f8b04-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ DiskDriveToDiskPartition Win32** mette in correlazione un'unità disco e una partizione esistente.</span><span class="sxs-lookup"><span data-stu-id="f8b04-104">The **Win32\_DiskDriveToDiskPartition** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a disk drive and a partition existing on it.</span></span>

<span data-ttu-id="f8b04-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f8b04-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f8b04-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f8b04-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8b04-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8b04-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDriveToDiskPartition : CIM_MediaPresent
{
  Win32_DiskDrive     REF Antecedent;
  Win32_DiskPartition REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f8b04-108">Members</span><span class="sxs-lookup"><span data-stu-id="f8b04-108">Members</span></span>

<span data-ttu-id="f8b04-109">La classe **Win32 \_ DiskDriveToDiskPartition** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f8b04-109">The **Win32\_DiskDriveToDiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="f8b04-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f8b04-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8b04-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f8b04-111">Properties</span></span>

<span data-ttu-id="f8b04-112">La classe **Win32 \_ DiskDriveToDiskPartition** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f8b04-112">The **Win32\_DiskDriveToDiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8b04-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="f8b04-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b04-114">Tipo di dati: **Win32 \_ DiskDrive**</span><span class="sxs-lookup"><span data-stu-id="f8b04-114">Data type: **Win32\_DiskDrive**</span></span>
</dt> <dt>

<span data-ttu-id="f8b04-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8b04-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8b04-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| WMI \_ Win32 DiskDrive")</span><span class="sxs-lookup"><span data-stu-id="f8b04-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskDrive")</span></span>
</dt> </dl>

<span data-ttu-id="f8b04-117">Riferimento all'istanza di che rappresenta le proprietà dell'unità disco in cui è presente la partizione.</span><span class="sxs-lookup"><span data-stu-id="f8b04-117">Reference to the instance representing the properties of the disk drive where the partition exists.</span></span>

</dd> <dt>

<span data-ttu-id="f8b04-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="f8b04-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b04-119">Tipo di dati: **Win32 \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="f8b04-119">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="f8b04-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8b04-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8b04-121">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DiskPartition")</span><span class="sxs-lookup"><span data-stu-id="f8b04-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="f8b04-122">Riferimento all'istanza che rappresenta la partizione del disco che risiede nell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="f8b04-122">Reference to the instance representing the disk partition residing on the disk drive.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8b04-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8b04-123">Remarks</span></span>

<span data-ttu-id="f8b04-124">La classe **Win32 \_ DiskDriveToDiskPartition** è derivata da [**CIM \_ MediaPresent**](cim-mediapresent.md).</span><span class="sxs-lookup"><span data-stu-id="f8b04-124">The **Win32\_DiskDriveToDiskPartition** class is derived from [**CIM\_MediaPresent**](cim-mediapresent.md).</span></span>

<span data-ttu-id="f8b04-125">Per una discussione su come usare questa classe, vedere gli articoli di Blog su come [usare PowerShell per eseguire il mapping di unità disco e partizioni](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) e [come è possibile correlare unità logiche e dischi fisici?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f8b04-125">For a discussion on how to use this class, see the [Use PowerShell to Map Disk Drives and Partitions](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) and the [How Can I Correlate Logical Drives and Physical Disks?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) blog articles.</span></span>

## <a name="examples"></a><span data-ttu-id="f8b04-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="f8b04-126">Examples</span></span>

<span data-ttu-id="f8b04-127">L'esempio [usare PowerShell per raccogliere informazioni su disco/partizione/punto di montaggio](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) USA **Win32 \_ DiskDriveToDiskPartition** per restituire informazioni sui dischi locali, le partizioni e i punti di montaggio.</span><span class="sxs-lookup"><span data-stu-id="f8b04-127">The [Use Powershell to Gather Disk/Partition/Mount Point Information](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) PowerShell sample uses **Win32\_DiskDriveToDiskPartition** to return information about local disks/partitions and mount points.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8b04-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8b04-128">Requirements</span></span>



| <span data-ttu-id="f8b04-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8b04-129">Requirement</span></span> | <span data-ttu-id="f8b04-130">Valore</span><span class="sxs-lookup"><span data-stu-id="f8b04-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b04-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8b04-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f8b04-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8b04-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8b04-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8b04-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f8b04-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8b04-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8b04-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f8b04-135">Namespace</span></span><br/>                | <span data-ttu-id="f8b04-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f8b04-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f8b04-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f8b04-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8b04-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8b04-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8b04-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f8b04-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8b04-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8b04-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8b04-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8b04-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b04-142">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="f8b04-142">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dt>

<span data-ttu-id="f8b04-143">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f8b04-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f8b04-144">Attività WMI: dischi e file System</span><span class="sxs-lookup"><span data-stu-id="f8b04-144">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

