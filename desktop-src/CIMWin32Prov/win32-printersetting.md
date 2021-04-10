---
description: La \_ classe WMI dell'associazione PrinterSetting Win32 mette in relazione una stampante e le relative impostazioni di configurazione.
ms.assetid: 5d0f0724-0583-449b-a6da-336e7c8e526e
ms.tgt_platform: multiple
title: Classe Win32_PrinterSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterSetting
- Win32_PrinterSetting.Setting
- Win32_PrinterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90a77678e61b755550ebb1818c34ccdc3159a88c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225654"
---
# <a name="win32_printersetting-class"></a><span data-ttu-id="332be-103">Win32 \_ PrinterSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="332be-103">Win32\_PrinterSetting class</span></span>

<span data-ttu-id="332be-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ PrinterSetting Win32** mette in relazione una stampante e le relative impostazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="332be-104">The **Win32\_PrinterSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a printer and its configuration settings.</span></span>

<span data-ttu-id="332be-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="332be-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="332be-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="332be-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="332be-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="332be-107">Syntax</span></span>

``` syntax
class Win32_PrinterSetting : Win32_DeviceSettings
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a><span data-ttu-id="332be-108">Members</span><span class="sxs-lookup"><span data-stu-id="332be-108">Members</span></span>

<span data-ttu-id="332be-109">La classe **Win32 \_ PrinterSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="332be-109">The **Win32\_PrinterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="332be-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="332be-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="332be-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="332be-111">Properties</span></span>

<span data-ttu-id="332be-112">La classe **Win32 \_ PrinterSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="332be-112">The **Win32\_PrinterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="332be-113">**elemento**</span><span class="sxs-lookup"><span data-stu-id="332be-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="332be-114">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="332be-114">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="332be-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="332be-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="332be-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="332be-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="332be-117">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che rappresenta le proprietà del dispositivo logico in cui è possibile applicare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="332be-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents properties of the logical device on which the settings can be applied.</span></span>

<span data-ttu-id="332be-118">Questa proprietà viene ereditata da [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="332be-118">This property is inherited from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

</dd> <dt>

<span data-ttu-id="332be-119">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="332be-119">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="332be-120">Tipo di dati **: \_ impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="332be-120">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="332be-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="332be-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="332be-122">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("impostazione CIM CIM \| \_ ")</span><span class="sxs-lookup"><span data-stu-id="332be-122">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="332be-123">[**\_ Impostazione CIM**](cim-setting.md) che rappresenta le impostazioni che possono essere applicate al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="332be-123">A [**CIM\_Setting**](cim-setting.md) that represents settings that can be applied to the logical device.</span></span>

<span data-ttu-id="332be-124">Questa proprietà viene ereditata da [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="332be-124">This property is inherited from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="332be-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="332be-125">Remarks</span></span>

<span data-ttu-id="332be-126">La classe **Win32 \_ PrinterSetting** è derivata da [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="332be-126">The **Win32\_PrinterSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="332be-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="332be-127">Requirements</span></span>



| <span data-ttu-id="332be-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="332be-128">Requirement</span></span> | <span data-ttu-id="332be-129">Valore</span><span class="sxs-lookup"><span data-stu-id="332be-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="332be-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="332be-130">Minimum supported client</span></span><br/> | <span data-ttu-id="332be-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="332be-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="332be-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="332be-132">Minimum supported server</span></span><br/> | <span data-ttu-id="332be-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="332be-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="332be-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="332be-134">Namespace</span></span><br/>                | <span data-ttu-id="332be-135">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="332be-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="332be-136">MOF</span><span class="sxs-lookup"><span data-stu-id="332be-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="332be-137"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="332be-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="332be-138">DLL</span><span class="sxs-lookup"><span data-stu-id="332be-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="332be-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="332be-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="332be-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="332be-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="332be-141">**\_DeviceSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="332be-141">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="332be-142">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="332be-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
