---
description: La \_ classe WMI dell'associazione SystemBootConfiguration Win32 mette in correlazione un computer e la relativa configurazione di avvio.
ms.assetid: 1c6bce81-84d9-4949-92da-6111b4ecc939
ms.tgt_platform: multiple
title: Classe Win32_SystemBootConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBootConfiguration
- Win32_SystemBootConfiguration.Element
- Win32_SystemBootConfiguration.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 863e4103f7e87681e25ccf53679bfe006ed3ff75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877810"
---
# <a name="win32_systembootconfiguration-class"></a><span data-ttu-id="43e50-103">Win32 \_ SystemBootConfiguration (classe)</span><span class="sxs-lookup"><span data-stu-id="43e50-103">Win32\_SystemBootConfiguration class</span></span>

<span data-ttu-id="43e50-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemBootConfiguration Win32** mette in correlazione un computer e la relativa configurazione di avvio.</span><span class="sxs-lookup"><span data-stu-id="43e50-104">The **Win32\_SystemBootConfiguration** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its boot configuration.</span></span>

<span data-ttu-id="43e50-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="43e50-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="43e50-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="43e50-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="43e50-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43e50-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C507-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBootConfiguration : Win32_SystemSetting
{
  Win32_ComputerSystem    REF Element;
  Win32_BootConfiguration REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="43e50-108">Members</span><span class="sxs-lookup"><span data-stu-id="43e50-108">Members</span></span>

<span data-ttu-id="43e50-109">La classe **Win32 \_ SystemBootConfiguration** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="43e50-109">The **Win32\_SystemBootConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="43e50-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43e50-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43e50-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43e50-111">Properties</span></span>

<span data-ttu-id="43e50-112">La classe **Win32 \_ SystemBootConfiguration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="43e50-112">The **Win32\_SystemBootConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43e50-113">**elemento**</span><span class="sxs-lookup"><span data-stu-id="43e50-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43e50-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="43e50-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="43e50-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43e50-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43e50-116">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="43e50-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="43e50-117">Riferimento all'istanza di che rappresenta il sistema del computer utilizzando la configurazione di avvio.</span><span class="sxs-lookup"><span data-stu-id="43e50-117">Reference to the instance representing the computer system using the boot configuration.</span></span>

</dd> <dt>

<span data-ttu-id="43e50-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="43e50-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43e50-119">Tipo di dati: **Win32 \_ BootConfiguration**</span><span class="sxs-lookup"><span data-stu-id="43e50-119">Data type: **Win32\_BootConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="43e50-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43e50-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43e50-121">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ BootConfiguration")</span><span class="sxs-lookup"><span data-stu-id="43e50-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_BootConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="43e50-122">Riferimento all'istanza di che rappresenta la configurazione di avvio per il computer.</span><span class="sxs-lookup"><span data-stu-id="43e50-122">Reference to the instance representing the boot configuration for the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43e50-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="43e50-123">Remarks</span></span>

<span data-ttu-id="43e50-124">La classe **Win32 \_ SystemBootConfiguration** è derivata da [**Win32 \_ SystemSetting**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="43e50-124">The **Win32\_SystemBootConfiguration** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43e50-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43e50-125">Requirements</span></span>



| <span data-ttu-id="43e50-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="43e50-126">Requirement</span></span> | <span data-ttu-id="43e50-127">Valore</span><span class="sxs-lookup"><span data-stu-id="43e50-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43e50-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43e50-128">Minimum supported client</span></span><br/> | <span data-ttu-id="43e50-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43e50-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43e50-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43e50-130">Minimum supported server</span></span><br/> | <span data-ttu-id="43e50-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43e50-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43e50-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="43e50-132">Namespace</span></span><br/>                | <span data-ttu-id="43e50-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="43e50-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="43e50-134">MOF</span><span class="sxs-lookup"><span data-stu-id="43e50-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43e50-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43e50-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="43e50-136">DLL</span><span class="sxs-lookup"><span data-stu-id="43e50-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43e50-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43e50-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43e50-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43e50-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43e50-139">**\_SystemSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="43e50-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="43e50-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="43e50-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
