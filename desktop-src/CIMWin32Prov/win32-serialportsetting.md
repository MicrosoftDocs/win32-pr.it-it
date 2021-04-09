---
description: La \_ classe WMI dell'associazione SerialPortSetting Win32 mette in correlazione una porta seriale e le relative impostazioni di configurazione.
ms.assetid: 57856207-abe5-4d93-9a34-acfe30ccd80c
ms.tgt_platform: multiple
title: Classe Win32_SerialPortSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortSetting
- Win32_SerialPortSetting.Setting
- Win32_SerialPortSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 713cdb57b5ed7135529959d3c17f7453924ce1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965951"
---
# <a name="win32_serialportsetting-class"></a><span data-ttu-id="73b2a-103">Win32 \_ SerialPortSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="73b2a-103">Win32\_SerialPortSetting class</span></span>

<span data-ttu-id="73b2a-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SerialPortSetting Win32** mette in correlazione una porta seriale e le relative impostazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="73b2a-104">The **Win32\_SerialPortSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a serial port and its configuration settings.</span></span>

<span data-ttu-id="73b2a-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="73b2a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="73b2a-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="73b2a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="73b2a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73b2a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortSetting : Win32_DeviceSettings
{
  Win32_SerialPortConfiguration REF Setting;
  Win32_SerialPort              REF Element;
};
```

## <a name="members"></a><span data-ttu-id="73b2a-108">Members</span><span class="sxs-lookup"><span data-stu-id="73b2a-108">Members</span></span>

<span data-ttu-id="73b2a-109">La classe **Win32 \_ SerialPortSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="73b2a-109">The **Win32\_SerialPortSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="73b2a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="73b2a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73b2a-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="73b2a-111">Properties</span></span>

<span data-ttu-id="73b2a-112">La classe **Win32 \_ SerialPortSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="73b2a-112">The **Win32\_SerialPortSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73b2a-113">**elemento**</span><span class="sxs-lookup"><span data-stu-id="73b2a-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73b2a-114">Tipo di dati **: \_ SerialPort Win32**</span><span class="sxs-lookup"><span data-stu-id="73b2a-114">Data type: **Win32\_SerialPort**</span></span>
</dt> <dt>

<span data-ttu-id="73b2a-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73b2a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73b2a-116">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| SerialPort Win32 WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="73b2a-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPort")</span></span>
</dt> </dl>

<span data-ttu-id="73b2a-117">[**\_ SerialPort Win32**](win32-serialport.md) che contiene le proprietà di una porta seriale nel computer.</span><span class="sxs-lookup"><span data-stu-id="73b2a-117">A [**Win32\_SerialPort**](win32-serialport.md) that contains the properties of a serial port on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="73b2a-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="73b2a-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73b2a-119">Tipo di dati: **Win32 \_ SerialPortConfiguration**</span><span class="sxs-lookup"><span data-stu-id="73b2a-119">Data type: **Win32\_SerialPortConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="73b2a-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73b2a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73b2a-121">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPortConfiguration")</span><span class="sxs-lookup"><span data-stu-id="73b2a-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPortConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="73b2a-122">[**\_ SerialPortConfiguration Win32**](win32-serialportconfiguration.md) che contiene l'impostazione di configurazione per la porta seriale.</span><span class="sxs-lookup"><span data-stu-id="73b2a-122">A [**Win32\_SerialPortConfiguration**](win32-serialportconfiguration.md) that contains the configuration setting for the serial port.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73b2a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="73b2a-123">Remarks</span></span>

<span data-ttu-id="73b2a-124">La classe **Win32 \_ SerialPortSetting** è derivata da [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="73b2a-124">The **Win32\_SerialPortSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73b2a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73b2a-125">Requirements</span></span>



| <span data-ttu-id="73b2a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="73b2a-126">Requirement</span></span> | <span data-ttu-id="73b2a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="73b2a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73b2a-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73b2a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="73b2a-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73b2a-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="73b2a-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73b2a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="73b2a-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73b2a-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73b2a-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="73b2a-132">Namespace</span></span><br/>                | <span data-ttu-id="73b2a-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="73b2a-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="73b2a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="73b2a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73b2a-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73b2a-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="73b2a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="73b2a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73b2a-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73b2a-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73b2a-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73b2a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73b2a-139">**\_DeviceSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="73b2a-139">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="73b2a-140">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="73b2a-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
