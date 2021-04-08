---
description: La \_ classe WMI astratta Win32 DeviceChangeEvent rappresenta gli eventi di modifica del dispositivo risultanti dall'aggiunta, dalla rimozione o dalla modifica dei dispositivi nel computer.
ms.assetid: 78155357-4231-4ded-980e-89feeb864ef2
ms.tgt_platform: multiple
title: Classe Win32_DeviceChangeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceChangeEvent
- Win32_DeviceChangeEvent.SECURITY_DESCRIPTOR
- Win32_DeviceChangeEvent.TIME_CREATED
- Win32_DeviceChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f97ab262d95b70a69b06e15202a78d5c1364f90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749031"
---
# <a name="win32_devicechangeevent-class"></a><span data-ttu-id="01d29-103">Win32 \_ DeviceChangeEvent (classe)</span><span class="sxs-lookup"><span data-stu-id="01d29-103">Win32\_DeviceChangeEvent class</span></span>

<span data-ttu-id="01d29-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) astratta **Win32 \_ DeviceChangeEvent** rappresenta gli eventi di modifica del dispositivo risultanti dall'aggiunta, dalla rimozione o dalla modifica dei dispositivi nel computer.</span><span class="sxs-lookup"><span data-stu-id="01d29-104">The **Win32\_DeviceChangeEvent** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents device change events that result from the addition, removal, or modification of devices on the computer system.</span></span> <span data-ttu-id="01d29-105">Sono incluse le modifiche apportate alla configurazione hardware (ancoraggio e disancoraggio), lo stato dell'hardware o i dispositivi appena mappati (mapping di un'unità di rete).</span><span class="sxs-lookup"><span data-stu-id="01d29-105">This includes changes in the hardware configuration (docking and undocking), the hardware state, or newly mapped devices (mapping of a network drive).</span></span> <span data-ttu-id="01d29-106">Ad esempio, un dispositivo è stato modificato quando \_ viene inviato un messaggio WM DEVICECHANGE.</span><span class="sxs-lookup"><span data-stu-id="01d29-106">For example, a device has changed when a WM\_DEVICECHANGE message is sent.</span></span>

<span data-ttu-id="01d29-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="01d29-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="01d29-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="01d29-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d29-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01d29-109">Syntax</span></span>

``` syntax
[UUID("0DE6AAF8-49F1-4868-B3D4-61CB69BA4322"), AMENDMENT]
class Win32_DeviceChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a><span data-ttu-id="01d29-110">Members</span><span class="sxs-lookup"><span data-stu-id="01d29-110">Members</span></span>

<span data-ttu-id="01d29-111">La classe **Win32 \_ DeviceChangeEvent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="01d29-111">The **Win32\_DeviceChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="01d29-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="01d29-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01d29-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="01d29-113">Properties</span></span>

<span data-ttu-id="01d29-114">La classe **Win32 \_ DeviceChangeEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="01d29-114">The **Win32\_DeviceChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01d29-115">**EventType**</span><span class="sxs-lookup"><span data-stu-id="01d29-115">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d29-116">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01d29-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01d29-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01d29-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d29-118">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIDevice Management Messages \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice Management Messages \| WM \_ SETTINGCHANGE")</span><span class="sxs-lookup"><span data-stu-id="01d29-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="01d29-119">Tipo di notifica di modifica dell'evento che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="01d29-119">Type of event change notification that has occurred.</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="01d29-120">**Configurazione modificata** (1)</span><span class="sxs-lookup"><span data-stu-id="01d29-120">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="01d29-121">**Arrivo del dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="01d29-121">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="01d29-122">**Rimozione del dispositivo** (3)</span><span class="sxs-lookup"><span data-stu-id="01d29-122">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="01d29-123">**Ancoraggio** (4)</span><span class="sxs-lookup"><span data-stu-id="01d29-123">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01d29-124">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="01d29-124">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d29-125">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="01d29-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="01d29-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01d29-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d29-127">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="01d29-127">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="01d29-128">Questa proprietà viene ereditata dall' [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="01d29-128">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="01d29-129">Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="01d29-129">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="01d29-130">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="01d29-130">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d29-131">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="01d29-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="01d29-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01d29-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d29-133">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="01d29-133">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="01d29-134">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="01d29-134">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="01d29-135">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="01d29-135">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="01d29-136">Questa proprietà viene ereditata dall' [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="01d29-136">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="01d29-137">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="01d29-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01d29-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="01d29-138">Remarks</span></span>

<span data-ttu-id="01d29-139">**Win32 \_ DeviceChangeEvent** è una classe astratta derivata da [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span><span class="sxs-lookup"><span data-stu-id="01d29-139">The **Win32\_DeviceChangeEvent** is an abstract class derived from [**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="01d29-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01d29-140">Requirements</span></span>



| <span data-ttu-id="01d29-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="01d29-141">Requirement</span></span> | <span data-ttu-id="01d29-142">Valore</span><span class="sxs-lookup"><span data-stu-id="01d29-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01d29-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01d29-143">Minimum supported client</span></span><br/> | <span data-ttu-id="01d29-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01d29-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01d29-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01d29-145">Minimum supported server</span></span><br/> | <span data-ttu-id="01d29-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01d29-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01d29-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="01d29-147">Namespace</span></span><br/>                | <span data-ttu-id="01d29-148">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="01d29-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01d29-149">MOF</span><span class="sxs-lookup"><span data-stu-id="01d29-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01d29-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01d29-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01d29-151">DLL</span><span class="sxs-lookup"><span data-stu-id="01d29-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01d29-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01d29-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01d29-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01d29-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01d29-154">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="01d29-154">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

<span data-ttu-id="01d29-155">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="01d29-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

