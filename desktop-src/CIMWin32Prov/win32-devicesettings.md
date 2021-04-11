---
description: Win32 \_ DeviceSettings abstract, associazione classe WMI mette in correlazione un dispositivo logico e un'impostazione che può essere applicata a tale dispositivo.
ms.assetid: 4f6c4c26-8da9-4e2c-8b8c-cec658ac08d4
ms.tgt_platform: multiple
title: Classe Win32_DeviceSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceSettings
- Win32_DeviceSettings.Setting
- Win32_DeviceSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1cd9cae29cfa608c9f3c0c36ebfe3ca7f903c809
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225741"
---
# <a name="win32_devicesettings-class"></a><span data-ttu-id="e9da0-103">Win32 \_ DeviceSettings (classe)</span><span class="sxs-lookup"><span data-stu-id="e9da0-103">Win32\_DeviceSettings class</span></span>

<span data-ttu-id="e9da0-104">**Win32 \_ DeviceSettings** abstract, associazione [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) mette in correlazione un dispositivo logico e un'impostazione che può essere applicata a tale dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9da0-104">The **Win32\_DeviceSettings** abstract, association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical device and a setting that can be applied to it.</span></span>

<span data-ttu-id="e9da0-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e9da0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e9da0-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="e9da0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9da0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9da0-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4FD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceSettings : CIM_ElementSetting
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a><span data-ttu-id="e9da0-108">Members</span><span class="sxs-lookup"><span data-stu-id="e9da0-108">Members</span></span>

<span data-ttu-id="e9da0-109">La classe **Win32 \_ DeviceSettings** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e9da0-109">The **Win32\_DeviceSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="e9da0-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e9da0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9da0-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e9da0-111">Properties</span></span>

<span data-ttu-id="e9da0-112">La classe **Win32 \_ DeviceSettings** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e9da0-112">The **Win32\_DeviceSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9da0-113">**elemento**</span><span class="sxs-lookup"><span data-stu-id="e9da0-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9da0-114">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="e9da0-114">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="e9da0-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9da0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9da0-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="e9da0-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="e9da0-117">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che rappresenta le proprietà del dispositivo logico in cui è possibile applicare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="e9da0-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents properties of the logical device on which the settings can be applied.</span></span>

</dd> <dt>

<span data-ttu-id="e9da0-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="e9da0-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9da0-119">Tipo di dati **: \_ impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="e9da0-119">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="e9da0-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9da0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9da0-121">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("impostazione"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("impostazione CIM CIM \| \_ ")</span><span class="sxs-lookup"><span data-stu-id="e9da0-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="e9da0-122">[**\_ Impostazione CIM**](cim-setting.md) che rappresenta le impostazioni che possono essere applicate al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e9da0-122">A [**CIM\_Setting**](cim-setting.md) that represents settings that can be applied to the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9da0-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9da0-123">Remarks</span></span>

<span data-ttu-id="e9da0-124">La classe **Win32 \_ DeviceSettings** è derivata da [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="e9da0-124">The **Win32\_DeviceSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9da0-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9da0-125">Requirements</span></span>



| <span data-ttu-id="e9da0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9da0-126">Requirement</span></span> | <span data-ttu-id="e9da0-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e9da0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9da0-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9da0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e9da0-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9da0-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9da0-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9da0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e9da0-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9da0-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9da0-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e9da0-132">Namespace</span></span><br/>                | <span data-ttu-id="e9da0-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e9da0-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9da0-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e9da0-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9da0-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9da0-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9da0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e9da0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9da0-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9da0-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9da0-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9da0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9da0-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="e9da0-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="e9da0-140">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="e9da0-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

