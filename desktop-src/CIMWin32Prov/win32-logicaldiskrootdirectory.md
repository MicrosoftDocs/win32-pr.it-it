---
description: La \_ classe WMI dell'associazione LogicalDiskRootDirectory Win32 mette in correlazione un disco logico e la relativa struttura di directory.
ms.assetid: 860cd28a-2a59-4ce3-be26-8fdc869c70d1
ms.tgt_platform: multiple
title: Classe Win32_LogicalDiskRootDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDiskRootDirectory
- Win32_LogicalDiskRootDirectory.GroupComponent
- Win32_LogicalDiskRootDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4b015891a37c5cc92bbf102482f48306d537bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877269"
---
# <a name="win32_logicaldiskrootdirectory-class"></a><span data-ttu-id="2f79f-103">Win32 \_ LogicalDiskRootDirectory (classe)</span><span class="sxs-lookup"><span data-stu-id="2f79f-103">Win32\_LogicalDiskRootDirectory class</span></span>

<span data-ttu-id="2f79f-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ LogicalDiskRootDirectory Win32** mette in correlazione un disco logico e la relativa struttura di directory.</span><span class="sxs-lookup"><span data-stu-id="2f79f-104">The **Win32\_LogicalDiskRootDirectory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical disk and its directory structure.</span></span>

<span data-ttu-id="2f79f-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2f79f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2f79f-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="2f79f-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f79f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f79f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE468-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalDiskRootDirectory : CIM_Component
{
  Win32_LogicalDisk REF GroupComponent;
  Win32_Directory   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="2f79f-108">Members</span><span class="sxs-lookup"><span data-stu-id="2f79f-108">Members</span></span>

<span data-ttu-id="2f79f-109">La classe **Win32 \_ LogicalDiskRootDirectory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2f79f-109">The **Win32\_LogicalDiskRootDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="2f79f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2f79f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f79f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2f79f-111">Properties</span></span>

<span data-ttu-id="2f79f-112">La classe **Win32 \_ LogicalDiskRootDirectory** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2f79f-112">The **Win32\_LogicalDiskRootDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f79f-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="2f79f-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f79f-114">Tipo di dati: **Win32 \_ disco logico**</span><span class="sxs-lookup"><span data-stu-id="2f79f-114">Data type: **Win32\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="2f79f-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f79f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f79f-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ disco logico")</span><span class="sxs-lookup"><span data-stu-id="2f79f-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalDisk")</span></span>
</dt> </dl>

<span data-ttu-id="2f79f-117">Riferimento all'istanza di che rappresenta le proprietà del disco logico.</span><span class="sxs-lookup"><span data-stu-id="2f79f-117">Reference to the instance representing the properties of the logical disk.</span></span>

</dd> <dt>

<span data-ttu-id="2f79f-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2f79f-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f79f-119">Tipo di dati **: \_ directory Win32**</span><span class="sxs-lookup"><span data-stu-id="2f79f-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="2f79f-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f79f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f79f-121">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| directory Win32 WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="2f79f-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="2f79f-122">Riferimento all'istanza di che rappresenta le proprietà della struttura di directory di file.</span><span class="sxs-lookup"><span data-stu-id="2f79f-122">Reference to the instance representing the properties of the file directory structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f79f-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f79f-123">Remarks</span></span>

<span data-ttu-id="2f79f-124">La classe **Win32 \_ LogicalDiskRootDirectory** è derivata dal [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="2f79f-124">The **Win32\_LogicalDiskRootDirectory** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f79f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f79f-125">Requirements</span></span>



| <span data-ttu-id="2f79f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f79f-126">Requirement</span></span> | <span data-ttu-id="2f79f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="2f79f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f79f-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f79f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2f79f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f79f-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f79f-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f79f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2f79f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f79f-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f79f-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2f79f-132">Namespace</span></span><br/>                | <span data-ttu-id="2f79f-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2f79f-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2f79f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="2f79f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f79f-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f79f-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f79f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2f79f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f79f-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f79f-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f79f-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f79f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f79f-139">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="2f79f-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="2f79f-140">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f79f-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

