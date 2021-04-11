---
description: Win32 \_ VolumeChangeEvent rappresenta un evento di unità locale risultante dall'aggiunta di una lettera di unità o di un'unità montata nel computer.
ms.assetid: 38595319-d7a1-4dcd-9ad8-a27cc484b699
ms.tgt_platform: multiple
title: Classe Win32_VolumeChangeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VolumeChangeEvent
- Win32_VolumeChangeEvent.SECURITY_DESCRIPTOR
- Win32_VolumeChangeEvent.TIME_CREATED
- Win32_VolumeChangeEvent.EventType
- Win32_VolumeChangeEvent.DriveName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e7610cae8d0cc746774b99a101e3c6aaf1f8a64d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126075"
---
# <a name="win32_volumechangeevent-class"></a><span data-ttu-id="d2cd9-103">Win32 \_ VolumeChangeEvent (classe)</span><span class="sxs-lookup"><span data-stu-id="d2cd9-103">Win32\_VolumeChangeEvent class</span></span>

<span data-ttu-id="d2cd9-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ VolumeChangeEvent Win32** rappresenta un evento di unità locale risultante dall'aggiunta di una lettera di unità o di un'unità montata nel computer.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-104">The **Win32\_VolumeChangeEvent** [WMI class](../wmisdk/retrieving-a-class.md) represents a local drive event that results from the addition of a drive letter or mounted drive on the computer system.</span></span> <span data-ttu-id="d2cd9-105">Le unità di rete non sono attualmente supportate.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-105">Network drives are not currently supported.</span></span>

<span data-ttu-id="d2cd9-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d2cd9-107">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2cd9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2cd9-108">Syntax</span></span>

``` syntax
[UUID("455CE053-2552-4051-A3E4-C4200DC31B7"), AMENDMENT]
class Win32_VolumeChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  string DriveName;
};
```

## <a name="members"></a><span data-ttu-id="d2cd9-109">Members</span><span class="sxs-lookup"><span data-stu-id="d2cd9-109">Members</span></span>

<span data-ttu-id="d2cd9-110">La classe **Win32 \_ VolumeChangeEvent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d2cd9-110">The **Win32\_VolumeChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="d2cd9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2cd9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2cd9-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2cd9-112">Properties</span></span>

<span data-ttu-id="d2cd9-113">La classe **Win32 \_ VolumeChangeEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-113">The **Win32\_VolumeChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2cd9-114">**DriveName**</span><span class="sxs-lookup"><span data-stu-id="d2cd9-114">**DriveName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2cd9-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2cd9-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2cd9-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2cd9-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2cd9-117">Nome dell'unità (lettera) che è stato aggiunto o rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-117">Drive name (letter) that has been added or removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d2cd9-118">**EventType**</span><span class="sxs-lookup"><span data-stu-id="d2cd9-118">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2cd9-119">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2cd9-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2cd9-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2cd9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2cd9-121">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice Management Messages \| WM \_ SETTINGCHANGE")</span><span class="sxs-lookup"><span data-stu-id="d2cd9-121">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="d2cd9-122">Tipo di notifica di modifica dell'evento che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-122">Type of event change notification that has occurred.</span></span>

<span data-ttu-id="d2cd9-123">Questa proprietà viene ereditata da [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="d2cd9-123">This property is inherited from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="d2cd9-124">**Configurazione modificata** (1)</span><span class="sxs-lookup"><span data-stu-id="d2cd9-124">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="d2cd9-125">**Arrivo del dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="d2cd9-125">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="d2cd9-126">**Rimozione del dispositivo** (3)</span><span class="sxs-lookup"><span data-stu-id="d2cd9-126">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="d2cd9-127">**Ancoraggio** (4)</span><span class="sxs-lookup"><span data-stu-id="d2cd9-127">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d2cd9-128">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="d2cd9-128">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2cd9-129">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d2cd9-129">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d2cd9-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2cd9-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2cd9-131">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-131">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="d2cd9-132">Questa proprietà viene ereditata dall' [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="d2cd9-132">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="d2cd9-133">Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d2cd9-133">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2cd9-134">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="d2cd9-134">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2cd9-135">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2cd9-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2cd9-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2cd9-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2cd9-137">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-137">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="d2cd9-138">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-138">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="d2cd9-139">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="d2cd9-139">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="d2cd9-140">Questa proprietà viene ereditata dall' [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="d2cd9-140">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="d2cd9-141">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="d2cd9-141">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2cd9-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2cd9-142">Remarks</span></span>

<span data-ttu-id="d2cd9-143">La classe **Win32 \_ VolumeChangeEvent** è derivata da [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="d2cd9-143">The **Win32\_VolumeChangeEvent** class is derived from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2cd9-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2cd9-144">Requirements</span></span>



| <span data-ttu-id="d2cd9-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2cd9-145">Requirement</span></span> | <span data-ttu-id="d2cd9-146">Valore</span><span class="sxs-lookup"><span data-stu-id="d2cd9-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2cd9-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2cd9-147">Minimum supported client</span></span><br/> | <span data-ttu-id="d2cd9-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2cd9-148">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2cd9-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2cd9-149">Minimum supported server</span></span><br/> | <span data-ttu-id="d2cd9-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2cd9-150">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2cd9-151">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d2cd9-151">Namespace</span></span><br/>                | <span data-ttu-id="d2cd9-152">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d2cd9-152">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d2cd9-153">MOF</span><span class="sxs-lookup"><span data-stu-id="d2cd9-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2cd9-154"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2cd9-154"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2cd9-155">DLL</span><span class="sxs-lookup"><span data-stu-id="d2cd9-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2cd9-156"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2cd9-156"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2cd9-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2cd9-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2cd9-158">**\_DeviceChangeEvent Win32**</span><span class="sxs-lookup"><span data-stu-id="d2cd9-158">**Win32\_DeviceChangeEvent**</span></span>](win32-devicechangeevent.md)
</dt> <dt>

[<span data-ttu-id="d2cd9-159">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d2cd9-159">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
