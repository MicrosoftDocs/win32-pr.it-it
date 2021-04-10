---
description: La \_ classe WMI dell'associazione ComputerSystemProcessor Win32 mette in relazione un computer e un processore in esecuzione su tale sistema.
ms.assetid: e630ebea-19bf-43c7-a8a0-7acfda3a752b
ms.tgt_platform: multiple
title: Classe Win32_ComputerSystemProcessor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProcessor
- Win32_ComputerSystemProcessor.PartComponent
- Win32_ComputerSystemProcessor.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2f836d8f5e9053029763c38d2c4f2116987b08fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126270"
---
# <a name="win32_computersystemprocessor-class"></a><span data-ttu-id="f64fc-103">Win32 \_ ComputerSystemProcessor (classe)</span><span class="sxs-lookup"><span data-stu-id="f64fc-103">Win32\_ComputerSystemProcessor class</span></span>

<span data-ttu-id="f64fc-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ ComputerSystemProcessor Win32** mette in relazione un computer e un processore in esecuzione su tale sistema.</span><span class="sxs-lookup"><span data-stu-id="f64fc-104">The **Win32\_ComputerSystemProcessor** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a computer system and a processor running on that system.</span></span>

<span data-ttu-id="f64fc-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f64fc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f64fc-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f64fc-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f64fc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f64fc-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{719A6839-C124-11d2-85E8-0000F8102E5F}"), AMENDMENT]
class Win32_ComputerSystemProcessor : Win32_SystemDevices
{
  Win32_Processor      REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="f64fc-108">Members</span><span class="sxs-lookup"><span data-stu-id="f64fc-108">Members</span></span>

<span data-ttu-id="f64fc-109">La classe **Win32 \_ ComputerSystemProcessor** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f64fc-109">The **Win32\_ComputerSystemProcessor** class has these types of members:</span></span>

-   [<span data-ttu-id="f64fc-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f64fc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f64fc-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f64fc-111">Properties</span></span>

<span data-ttu-id="f64fc-112">La classe **Win32 \_ ComputerSystemProcessor** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f64fc-112">The **Win32\_ComputerSystemProcessor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f64fc-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f64fc-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f64fc-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="f64fc-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="f64fc-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f64fc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f64fc-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="f64fc-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="f64fc-117">**\_ ComputerSystem Win32** che descrive le proprietà del computer in cui è in esecuzione il processore.</span><span class="sxs-lookup"><span data-stu-id="f64fc-117">A **Win32\_ComputerSystem** that describes the properties of the computer system on which the processor is running.</span></span>

</dd> <dt>

<span data-ttu-id="f64fc-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f64fc-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f64fc-119">Tipo di dati **: \_ processore Win32**</span><span class="sxs-lookup"><span data-stu-id="f64fc-119">Data type: **Win32\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="f64fc-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f64fc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f64fc-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| processore Win32 WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="f64fc-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Processor")</span></span>
</dt> </dl>

<span data-ttu-id="f64fc-122">[**\_ Processore Win32**](win32-processor.md) che descrive le proprietà di un processore che esegue il computer.</span><span class="sxs-lookup"><span data-stu-id="f64fc-122">A [**Win32\_Processor**](win32-processor.md) that describes the properties of a processor which is running the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f64fc-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f64fc-123">Remarks</span></span>

<span data-ttu-id="f64fc-124">La classe **Win32 \_ ComputerSystemProcessor** è derivata da [**Win32 \_ SystemDevices**](win32-systemdevices.md).</span><span class="sxs-lookup"><span data-stu-id="f64fc-124">The **Win32\_ComputerSystemProcessor** class is derived from [**Win32\_SystemDevices**](win32-systemdevices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f64fc-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f64fc-125">Requirements</span></span>



| <span data-ttu-id="f64fc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f64fc-126">Requirement</span></span> | <span data-ttu-id="f64fc-127">Valore</span><span class="sxs-lookup"><span data-stu-id="f64fc-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f64fc-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f64fc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f64fc-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f64fc-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f64fc-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f64fc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f64fc-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f64fc-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f64fc-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f64fc-132">Namespace</span></span><br/>                | <span data-ttu-id="f64fc-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f64fc-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f64fc-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f64fc-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f64fc-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f64fc-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f64fc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f64fc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f64fc-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f64fc-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f64fc-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f64fc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f64fc-139">**\_SystemDevices Win32**</span><span class="sxs-lookup"><span data-stu-id="f64fc-139">**Win32\_SystemDevices**</span></span>](win32-systemdevices.md)
</dt> <dt>

<span data-ttu-id="f64fc-140">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f64fc-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

