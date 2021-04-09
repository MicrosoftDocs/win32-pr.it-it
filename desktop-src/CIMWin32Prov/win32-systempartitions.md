---
description: La \_ classe WMI dell'associazione SystemPartitions Win32 mette in correlazione un computer e una partizione disco in tale sistema.
ms.assetid: e8f02cd0-9446-4258-b476-5dc6c72c80d4
ms.tgt_platform: multiple
title: Classe Win32_SystemPartitions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemPartitions
- Win32_SystemPartitions.GroupComponent
- Win32_SystemPartitions.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deae8129772e5d854f05b5b953ec66a12bd5bcaf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877806"
---
# <a name="win32_systempartitions-class"></a><span data-ttu-id="b61c8-103">Win32 \_ SystemPartitions (classe)</span><span class="sxs-lookup"><span data-stu-id="b61c8-103">Win32\_SystemPartitions class</span></span>

<span data-ttu-id="b61c8-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemPartitions Win32** mette in correlazione un computer e una partizione disco in tale sistema.</span><span class="sxs-lookup"><span data-stu-id="b61c8-104">The **Win32\_SystemPartitions** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a disk partition on that system.</span></span>

<span data-ttu-id="b61c8-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b61c8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b61c8-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b61c8-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b61c8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b61c8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemPartitions : Win32_SystemDevices
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_DiskPartition  REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="b61c8-108">Members</span><span class="sxs-lookup"><span data-stu-id="b61c8-108">Members</span></span>

<span data-ttu-id="b61c8-109">La classe **Win32 \_ SystemPartitions** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b61c8-109">The **Win32\_SystemPartitions** class has these types of members:</span></span>

-   [<span data-ttu-id="b61c8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b61c8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b61c8-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b61c8-111">Properties</span></span>

<span data-ttu-id="b61c8-112">La classe **Win32 \_ SystemPartitions** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b61c8-112">The **Win32\_SystemPartitions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b61c8-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b61c8-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b61c8-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="b61c8-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b61c8-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b61c8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b61c8-116">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="b61c8-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="b61c8-117">Riferimento all'istanza di che rappresenta le proprietà del computer in cui si trova la partizione del disco.</span><span class="sxs-lookup"><span data-stu-id="b61c8-117">Reference to the instance representing the properties of the computer system where the disk partition is located.</span></span>

</dd> <dt>

<span data-ttu-id="b61c8-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b61c8-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b61c8-119">Tipo di dati: **Win32 \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="b61c8-119">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="b61c8-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b61c8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b61c8-121">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ DiskPartition")</span><span class="sxs-lookup"><span data-stu-id="b61c8-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="b61c8-122">Riferimento all'istanza di che rappresenta le proprietà di una partizione disco esistente nel computer.</span><span class="sxs-lookup"><span data-stu-id="b61c8-122">Reference to the instance representing the properties of a disk partition that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b61c8-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="b61c8-123">Remarks</span></span>

<span data-ttu-id="b61c8-124">La classe **Win32 \_ SystemPartitions** è derivata da [**Win32 \_ SystemDevices**](win32-systemdevices.md).</span><span class="sxs-lookup"><span data-stu-id="b61c8-124">The **Win32\_SystemPartitions** class is derived from [**Win32\_SystemDevices**](win32-systemdevices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b61c8-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b61c8-125">Requirements</span></span>



| <span data-ttu-id="b61c8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b61c8-126">Requirement</span></span> | <span data-ttu-id="b61c8-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b61c8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b61c8-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b61c8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b61c8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b61c8-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b61c8-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b61c8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b61c8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b61c8-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b61c8-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b61c8-132">Namespace</span></span><br/>                | <span data-ttu-id="b61c8-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b61c8-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b61c8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b61c8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b61c8-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b61c8-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b61c8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b61c8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b61c8-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b61c8-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b61c8-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b61c8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b61c8-139">**\_SystemDevices Win32**</span><span class="sxs-lookup"><span data-stu-id="b61c8-139">**Win32\_SystemDevices**</span></span>](win32-systemdevices.md)
</dt> <dt>

[<span data-ttu-id="b61c8-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b61c8-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
