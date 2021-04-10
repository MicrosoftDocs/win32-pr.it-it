---
description: Win32 \_ SystemConfigurationChangeEvent&\# 8194; Classe WMI indica che l'elenco dei dispositivi nel sistema è stato aggiornato (un dispositivo è stato aggiunto o rimosso o la configurazione è stata modificata).
ms.assetid: dce1e866-e739-4f90-9016-48b20ccfb75b
ms.tgt_platform: multiple
title: Classe Win32_SystemConfigurationChangeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemConfigurationChangeEvent
- Win32_SystemConfigurationChangeEvent.SECURITY_DESCRIPTOR
- Win32_SystemConfigurationChangeEvent.TIME_CREATED
- Win32_SystemConfigurationChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0bc479d3415906a6536c6df1d163056e94e2af76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127443"
---
# <a name="win32_systemconfigurationchangeevent-class"></a><span data-ttu-id="93ddb-103">Win32 \_ SystemConfigurationChangeEvent (classe)</span><span class="sxs-lookup"><span data-stu-id="93ddb-103">Win32\_SystemConfigurationChangeEvent class</span></span>

<span data-ttu-id="93ddb-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemConfigurationChangeEvent Win32** indica che l'elenco dei dispositivi nel sistema è stato aggiornato (un dispositivo è stato aggiunto o rimosso o la configurazione è stata modificata).</span><span class="sxs-lookup"><span data-stu-id="93ddb-104">The **Win32\_SystemConfigurationChangeEvent** [WMI class](../wmisdk/retrieving-a-class.md) indicates that the device list on the system has been refreshed (a device has been added or removed, or the configuration changed).</span></span> <span data-ttu-id="93ddb-105">Viene generato un evento e viene creata un'istanza di questa classe quando viene inviato il messaggio "DevMgrRefreshOn<*computername*>".</span><span class="sxs-lookup"><span data-stu-id="93ddb-105">An event is fired and an instance of this is class created when the "DevMgrRefreshOn<*ComputerName*>" message is sent.</span></span> <span data-ttu-id="93ddb-106">La modifica esatta dell'elenco dei dispositivi non è contenuta nel messaggio, quindi è necessario un aggiornamento del dispositivo per ottenere le impostazioni di sistema correnti.</span><span class="sxs-lookup"><span data-stu-id="93ddb-106">The exact change to the device list is not contained in the message, so a device refresh is required to obtain the current system settings.</span></span> <span data-ttu-id="93ddb-107">Esempi di modifiche alla configurazione interessate sono le impostazioni IRQ, le porte COM e le versioni BIOS.</span><span class="sxs-lookup"><span data-stu-id="93ddb-107">Examples of configuration changes affected are IRQ settings, COM ports, and BIOS versions.</span></span>

<span data-ttu-id="93ddb-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="93ddb-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="93ddb-109">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="93ddb-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="93ddb-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93ddb-110">Syntax</span></span>

``` syntax
[UUID("76746942-D94B-47E2-BBA4-AFD2FDBA61"), AMENDMENT]
class Win32_SystemConfigurationChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a><span data-ttu-id="93ddb-111">Members</span><span class="sxs-lookup"><span data-stu-id="93ddb-111">Members</span></span>

<span data-ttu-id="93ddb-112">La classe **Win32 \_ SystemConfigurationChangeEvent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="93ddb-112">The **Win32\_SystemConfigurationChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="93ddb-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="93ddb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93ddb-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="93ddb-114">Properties</span></span>

<span data-ttu-id="93ddb-115">La classe **Win32 \_ SystemConfigurationChangeEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="93ddb-115">The **Win32\_SystemConfigurationChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93ddb-116">**EventType**</span><span class="sxs-lookup"><span data-stu-id="93ddb-116">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ddb-117">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93ddb-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93ddb-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="93ddb-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ddb-119">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice Management Messages \| WM \_ SETTINGCHANGE")</span><span class="sxs-lookup"><span data-stu-id="93ddb-119">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="93ddb-120">Tipo di notifica di modifica dell'evento che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="93ddb-120">Type of event change notification that has occurred.</span></span>

<span data-ttu-id="93ddb-121">Questa proprietà viene ereditata da [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="93ddb-121">This property is inherited from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="93ddb-122">**Configurazione modificata** (1)</span><span class="sxs-lookup"><span data-stu-id="93ddb-122">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="93ddb-123">**Arrivo del dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="93ddb-123">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="93ddb-124">**Rimozione del dispositivo** (3)</span><span class="sxs-lookup"><span data-stu-id="93ddb-124">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="93ddb-125">**Ancoraggio** (4)</span><span class="sxs-lookup"><span data-stu-id="93ddb-125">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93ddb-126">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="93ddb-126">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ddb-127">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="93ddb-127">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="93ddb-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="93ddb-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93ddb-129">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="93ddb-129">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="93ddb-130">Questa proprietà viene ereditata dall' [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="93ddb-130">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="93ddb-131">Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="93ddb-131">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ddb-132">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="93ddb-132">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ddb-133">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93ddb-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93ddb-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="93ddb-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93ddb-135">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="93ddb-135">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="93ddb-136">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="93ddb-136">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="93ddb-137">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="93ddb-137">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="93ddb-138">Questa proprietà viene ereditata dall' [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="93ddb-138">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="93ddb-139">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="93ddb-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93ddb-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="93ddb-140">Remarks</span></span>

<span data-ttu-id="93ddb-141">La classe **Win32 \_ SystemConfigurationChangeEvent** è derivata da [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="93ddb-141">The **Win32\_SystemConfigurationChangeEvent** class is derived from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93ddb-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93ddb-142">Requirements</span></span>



| <span data-ttu-id="93ddb-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="93ddb-143">Requirement</span></span> | <span data-ttu-id="93ddb-144">Valore</span><span class="sxs-lookup"><span data-stu-id="93ddb-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93ddb-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93ddb-145">Minimum supported client</span></span><br/> | <span data-ttu-id="93ddb-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93ddb-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93ddb-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93ddb-147">Minimum supported server</span></span><br/> | <span data-ttu-id="93ddb-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93ddb-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93ddb-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="93ddb-149">Namespace</span></span><br/>                | <span data-ttu-id="93ddb-150">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="93ddb-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="93ddb-151">MOF</span><span class="sxs-lookup"><span data-stu-id="93ddb-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93ddb-152"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93ddb-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="93ddb-153">DLL</span><span class="sxs-lookup"><span data-stu-id="93ddb-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93ddb-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93ddb-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93ddb-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93ddb-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ddb-156">**\_DeviceChangeEvent Win32**</span><span class="sxs-lookup"><span data-stu-id="93ddb-156">**Win32\_DeviceChangeEvent**</span></span>](win32-devicechangeevent.md)
</dt> <dt>

[<span data-ttu-id="93ddb-157">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="93ddb-157">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
