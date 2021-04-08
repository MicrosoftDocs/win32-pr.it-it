---
description: La \_ classe WMI dell'associazione SystemTimeZone Win32 mette in correlazione un computer e un fuso orario.
ms.assetid: 53c74a61-c91d-4daa-933e-4cc7b9583d98
ms.tgt_platform: multiple
title: Classe Win32_SystemTimeZone
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemTimeZone
- Win32_SystemTimeZone.Element
- Win32_SystemTimeZone.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ec294600fdc81f085bf29f5e664bcbec961417c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877801"
---
# <a name="win32_systemtimezone-class"></a><span data-ttu-id="340af-103">Win32 \_ SystemTimeZone (classe)</span><span class="sxs-lookup"><span data-stu-id="340af-103">Win32\_SystemTimeZone class</span></span>

<span data-ttu-id="340af-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemTimeZone Win32** mette in correlazione un computer e un fuso orario.</span><span class="sxs-lookup"><span data-stu-id="340af-104">The **Win32\_SystemTimeZone** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a time zone.</span></span>

<span data-ttu-id="340af-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="340af-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="340af-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="340af-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="340af-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="340af-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C504-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemTimeZone : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_TimeZone       REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="340af-108">Members</span><span class="sxs-lookup"><span data-stu-id="340af-108">Members</span></span>

<span data-ttu-id="340af-109">La classe **Win32 \_ SystemTimeZone** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="340af-109">The **Win32\_SystemTimeZone** class has these types of members:</span></span>

-   [<span data-ttu-id="340af-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="340af-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="340af-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="340af-111">Properties</span></span>

<span data-ttu-id="340af-112">La classe **Win32 \_ SystemTimeZone** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="340af-112">The **Win32\_SystemTimeZone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="340af-113">**elemento**</span><span class="sxs-lookup"><span data-stu-id="340af-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="340af-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="340af-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="340af-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="340af-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="340af-116">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="340af-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="340af-117">Riferimento all'istanza che rappresenta il sistema del computer che tiene traccia del fuso orario di sistema.</span><span class="sxs-lookup"><span data-stu-id="340af-117">Reference to the instance representing the computer system keeping track of the system time zone.</span></span>

</dd> <dt>

<span data-ttu-id="340af-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="340af-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="340af-119">Tipo di dati **: \_ fuso orario Win32**</span><span class="sxs-lookup"><span data-stu-id="340af-119">Data type: **Win32\_TimeZone**</span></span>
</dt> <dt>

<span data-ttu-id="340af-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="340af-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="340af-121">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ TimeZone")</span><span class="sxs-lookup"><span data-stu-id="340af-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_TimeZone")</span></span>
</dt> </dl>

<span data-ttu-id="340af-122">Riferimento all'istanza di che rappresenta le proprietà del fuso orario registrate dal sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="340af-122">Reference to the instance representing the time zone properties tracked by the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="340af-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="340af-123">Remarks</span></span>

<span data-ttu-id="340af-124">La classe **Win32 \_ SystemTimeZone** è derivata da [**Win32 \_ SystemSetting**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="340af-124">The **Win32\_SystemTimeZone** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="340af-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="340af-125">Requirements</span></span>



| <span data-ttu-id="340af-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="340af-126">Requirement</span></span> | <span data-ttu-id="340af-127">Valore</span><span class="sxs-lookup"><span data-stu-id="340af-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="340af-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="340af-128">Minimum supported client</span></span><br/> | <span data-ttu-id="340af-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="340af-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="340af-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="340af-130">Minimum supported server</span></span><br/> | <span data-ttu-id="340af-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="340af-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="340af-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="340af-132">Namespace</span></span><br/>                | <span data-ttu-id="340af-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="340af-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="340af-134">MOF</span><span class="sxs-lookup"><span data-stu-id="340af-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="340af-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="340af-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="340af-136">DLL</span><span class="sxs-lookup"><span data-stu-id="340af-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="340af-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="340af-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="340af-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="340af-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="340af-139">**\_SystemSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="340af-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="340af-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="340af-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
