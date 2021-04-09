---
description: La \_ classe WMI dell'associazione SystemDesktop Win32 mette in correlazione un computer e la relativa configurazione desktop.
ms.assetid: 2b024660-d707-4463-8207-73df74bfa7d6
ms.tgt_platform: multiple
title: Classe Win32_SystemDesktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDesktop
- Win32_SystemDesktop.Element
- Win32_SystemDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e14cab58a445fd645b9d59c1aea713bf6c40ac0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966324"
---
# <a name="win32_systemdesktop-class"></a><span data-ttu-id="39576-103">Win32 \_ SystemDesktop (classe)</span><span class="sxs-lookup"><span data-stu-id="39576-103">Win32\_SystemDesktop class</span></span>

<span data-ttu-id="39576-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemDesktop Win32** mette in correlazione un computer e la relativa configurazione desktop.</span><span class="sxs-lookup"><span data-stu-id="39576-104">The **Win32\_SystemDesktop** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its desktop configuration.</span></span>

<span data-ttu-id="39576-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="39576-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="39576-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="39576-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="39576-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39576-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C506-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDesktop : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_Desktop        REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="39576-108">Members</span><span class="sxs-lookup"><span data-stu-id="39576-108">Members</span></span>

<span data-ttu-id="39576-109">La classe **Win32 \_ SystemDesktop** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="39576-109">The **Win32\_SystemDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="39576-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="39576-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39576-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="39576-111">Properties</span></span>

<span data-ttu-id="39576-112">La classe **Win32 \_ SystemDesktop** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="39576-112">The **Win32\_SystemDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39576-113">**elemento**</span><span class="sxs-lookup"><span data-stu-id="39576-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39576-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="39576-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="39576-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39576-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39576-116">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="39576-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="39576-117">Riferimento all'istanza di che rappresenta il computer in cui è presente la configurazione desktop.</span><span class="sxs-lookup"><span data-stu-id="39576-117">Reference to the instance representing the computer system where the desktop configuration exists.</span></span>

</dd> <dt>

<span data-ttu-id="39576-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="39576-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39576-119">Tipo di dati **: \_ desktop Win32**</span><span class="sxs-lookup"><span data-stu-id="39576-119">Data type: **Win32\_Desktop**</span></span>
</dt> <dt>

<span data-ttu-id="39576-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39576-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39576-121">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("impostazione"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| desktop Win32 Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="39576-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="39576-122">Riferimento all'istanza di che rappresenta la configurazione esistente nel computer.</span><span class="sxs-lookup"><span data-stu-id="39576-122">Reference to the instance representing the configuration existing on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39576-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="39576-123">Remarks</span></span>

<span data-ttu-id="39576-124">La classe **Win32 \_ SystemDesktop** è derivata da [**Win32 \_ SystemSetting**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="39576-124">The **Win32\_SystemDesktop** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39576-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39576-125">Requirements</span></span>



| <span data-ttu-id="39576-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="39576-126">Requirement</span></span> | <span data-ttu-id="39576-127">Valore</span><span class="sxs-lookup"><span data-stu-id="39576-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39576-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39576-128">Minimum supported client</span></span><br/> | <span data-ttu-id="39576-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39576-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39576-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39576-130">Minimum supported server</span></span><br/> | <span data-ttu-id="39576-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39576-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39576-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="39576-132">Namespace</span></span><br/>                | <span data-ttu-id="39576-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="39576-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="39576-134">MOF</span><span class="sxs-lookup"><span data-stu-id="39576-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39576-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39576-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="39576-136">DLL</span><span class="sxs-lookup"><span data-stu-id="39576-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39576-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39576-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39576-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39576-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39576-139">**\_SystemSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="39576-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="39576-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="39576-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
