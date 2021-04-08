---
description: La \_ classe WMI dell'associazione ClassicCOMClassSettings Win32 mette in correlazione una classe Component Object Model (com) e le impostazioni utilizzate per configurare le istanze della classe com.
ms.assetid: 50f253cc-b8ae-41ac-b01f-ea816f5ca3d4
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMClassSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSettings
- Win32_ClassicCOMClassSettings.Setting
- Win32_ClassicCOMClassSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb9c190157742aeca7c1ba6008a784005d054ca6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877342"
---
# <a name="win32_classiccomclasssettings-class"></a><span data-ttu-id="1758f-103">Win32 \_ ClassicCOMClassSettings (classe)</span><span class="sxs-lookup"><span data-stu-id="1758f-103">Win32\_ClassicCOMClassSettings class</span></span>

<span data-ttu-id="1758f-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ ClassicCOMClassSettings Win32** mette in correlazione una classe Component Object Model (com) e le impostazioni utilizzate per configurare le istanze della classe com.</span><span class="sxs-lookup"><span data-stu-id="1758f-104">The **Win32\_ClassicCOMClassSettings** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) class and the settings used to configure instances of the COM class.</span></span>

<span data-ttu-id="1758f-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1758f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1758f-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="1758f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1758f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1758f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A564-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSettings : CIM_ElementSetting
{
  Win32_ClassicCOMClassSetting REF Setting;
  Win32_ClassicCOMClass        REF Element;
};
```

## <a name="members"></a><span data-ttu-id="1758f-108">Members</span><span class="sxs-lookup"><span data-stu-id="1758f-108">Members</span></span>

<span data-ttu-id="1758f-109">La classe **Win32 \_ ClassicCOMClassSettings** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1758f-109">The **Win32\_ClassicCOMClassSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="1758f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1758f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1758f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1758f-111">Properties</span></span>

<span data-ttu-id="1758f-112">La classe **Win32 \_ ClassicCOMClassSettings** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1758f-112">The **Win32\_ClassicCOMClassSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1758f-113">**elemento**</span><span class="sxs-lookup"><span data-stu-id="1758f-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1758f-114">Tipo di dati: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="1758f-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="1758f-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1758f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1758f-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="1758f-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="1758f-117">[**\_ ClassicCOMClass Win32**](win32-classiccomclass.md) che rappresenta la classe com A cui vengono applicate le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1758f-117">A [**Win32\_ClassicCOMClass**](win32-classiccomclass.md) that represents the COM class where the settings are applied.</span></span>

</dd> <dt>

<span data-ttu-id="1758f-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="1758f-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1758f-119">Tipo di dati: **Win32 \_ ClassicCOMClassSetting**</span><span class="sxs-lookup"><span data-stu-id="1758f-119">Data type: **Win32\_ClassicCOMClassSetting**</span></span>
</dt> <dt>

<span data-ttu-id="1758f-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1758f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1758f-121">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClassSetting")</span><span class="sxs-lookup"><span data-stu-id="1758f-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClassSetting")</span></span>
</dt> </dl>

<span data-ttu-id="1758f-122">[**\_ ClassicCOMClassSetting Win32**](win32-classiccomclasssetting.md) che rappresenta le impostazioni di configurazione associate alla classe com.</span><span class="sxs-lookup"><span data-stu-id="1758f-122">A [**Win32\_ClassicCOMClassSetting**](win32-classiccomclasssetting.md) that represents configuration settings associated with the COM class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1758f-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="1758f-123">Remarks</span></span>

<span data-ttu-id="1758f-124">La classe **Win32 \_ ClassicCOMClassSettings** è derivata da [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="1758f-124">The **Win32\_ClassicCOMClassSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1758f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1758f-125">Requirements</span></span>



| <span data-ttu-id="1758f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1758f-126">Requirement</span></span> | <span data-ttu-id="1758f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1758f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1758f-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1758f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1758f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1758f-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1758f-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1758f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1758f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1758f-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1758f-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1758f-132">Namespace</span></span><br/>                | <span data-ttu-id="1758f-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1758f-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1758f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1758f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1758f-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1758f-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1758f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1758f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1758f-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1758f-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1758f-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1758f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1758f-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="1758f-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

<span data-ttu-id="1758f-140">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1758f-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

