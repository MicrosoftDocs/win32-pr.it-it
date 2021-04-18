---
description: La \_ classe WMI PointingDevice Win32 rappresenta un dispositivo di input utilizzato per puntare e selezionare le aree sulla visualizzazione di un computer che esegue Windows.
ms.assetid: ed81abe3-3d8f-48aa-ab64-9e6c87e44f64
ms.tgt_platform: multiple
title: Classe Win32_PointingDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PointingDevice
- Win32_PointingDevice.Reset
- Win32_PointingDevice.SetPowerState
- Win32_PointingDevice.Availability
- Win32_PointingDevice.Caption
- Win32_PointingDevice.ConfigManagerErrorCode
- Win32_PointingDevice.ConfigManagerUserConfig
- Win32_PointingDevice.CreationClassName
- Win32_PointingDevice.Description
- Win32_PointingDevice.DeviceID
- Win32_PointingDevice.DeviceInterface
- Win32_PointingDevice.DoubleSpeedThreshold
- Win32_PointingDevice.ErrorCleared
- Win32_PointingDevice.ErrorDescription
- Win32_PointingDevice.Handedness
- Win32_PointingDevice.HardwareType
- Win32_PointingDevice.InfFileName
- Win32_PointingDevice.InfSection
- Win32_PointingDevice.InstallDate
- Win32_PointingDevice.IsLocked
- Win32_PointingDevice.LastErrorCode
- Win32_PointingDevice.Manufacturer
- Win32_PointingDevice.Name
- Win32_PointingDevice.NumberOfButtons
- Win32_PointingDevice.PNPDeviceID
- Win32_PointingDevice.PointingType
- Win32_PointingDevice.PowerManagementCapabilities
- Win32_PointingDevice.PowerManagementSupported
- Win32_PointingDevice.QuadSpeedThreshold
- Win32_PointingDevice.Resolution
- Win32_PointingDevice.SampleRate
- Win32_PointingDevice.Status
- Win32_PointingDevice.StatusInfo
- Win32_PointingDevice.Synch
- Win32_PointingDevice.SystemCreationClassName
- Win32_PointingDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e4f2359e19476dfae111fc361f48e6f73d8cfac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304508"
---
# <a name="win32_pointingdevice-class"></a><span data-ttu-id="b42bb-103">Win32 \_ PointingDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="b42bb-103">Win32\_PointingDevice class</span></span>

<span data-ttu-id="b42bb-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PointingDevice Win32** rappresenta un dispositivo di input utilizzato per puntare e selezionare le aree sulla visualizzazione di un computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="b42bb-104">The **Win32\_PointingDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents an input device used to point to and select regions on the display of a computer system running Windows.</span></span> <span data-ttu-id="b42bb-105">Qualsiasi dispositivo usato per modificare un puntatore o puntare alla visualizzazione in un sistema di computer che esegue Windows è un membro di questa classe.</span><span class="sxs-lookup"><span data-stu-id="b42bb-105">Any device used to manipulate a pointer, or point to the display on a computer system running Windows is a member of this class.</span></span>

<span data-ttu-id="b42bb-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b42bb-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b42bb-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b42bb-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b42bb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b42bb-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_PointingDevice : CIM_PointingDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DeviceInterface;
  uint32   DoubleSpeedThreshold;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Handedness;
  string   HardwareType;
  string   InfFileName;
  string   InfSection;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   Manufacturer;
  string   Name;
  uint8    NumberOfButtons;
  string   PNPDeviceID;
  uint16   PointingType;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   QuadSpeedThreshold;
  uint32   Resolution;
  uint32   SampleRate;
  string   Status;
  uint16   StatusInfo;
  uint32   Synch;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="b42bb-109">Members</span><span class="sxs-lookup"><span data-stu-id="b42bb-109">Members</span></span>

<span data-ttu-id="b42bb-110">La classe **Win32 \_ PointingDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b42bb-110">The **Win32\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="b42bb-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="b42bb-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b42bb-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b42bb-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b42bb-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="b42bb-113">Methods</span></span>

<span data-ttu-id="b42bb-114">La classe **Win32 \_ PointingDevice** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b42bb-114">The **Win32\_PointingDevice** class has these methods.</span></span>



| <span data-ttu-id="b42bb-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="b42bb-115">Method</span></span>            | <span data-ttu-id="b42bb-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b42bb-116">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b42bb-117">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="b42bb-117">**Reset**</span></span>         | <span data-ttu-id="b42bb-118">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="b42bb-118">Not implemented.</span></span> <span data-ttu-id="b42bb-119">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span><br/>                 |
| <span data-ttu-id="b42bb-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b42bb-120">**SetPowerState**</span></span> | <span data-ttu-id="b42bb-121">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="b42bb-121">Not implemented.</span></span> <span data-ttu-id="b42bb-122">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b42bb-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b42bb-123">Properties</span></span>

<span data-ttu-id="b42bb-124">La classe **Win32 \_ PointingDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b42bb-124">The **Win32\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b42bb-125">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="b42bb-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b42bb-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-128">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="b42bb-128">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-129">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b42bb-129">Availability and status of the device.</span></span>

<span data-ttu-id="b42bb-130">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b42bb-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b42bb-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b42bb-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b42bb-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b42bb-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="b42bb-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-134">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="b42bb-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b42bb-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="b42bb-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b42bb-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="b42bb-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b42bb-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="b42bb-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b42bb-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="b42bb-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b42bb-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="b42bb-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b42bb-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="b42bb-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b42bb-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="b42bb-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b42bb-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="b42bb-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b42bb-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="b42bb-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b42bb-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="b42bb-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-145">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b42bb-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b42bb-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="b42bb-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-147">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="b42bb-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b42bb-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="b42bb-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-149">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="b42bb-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b42bb-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="b42bb-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b42bb-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="b42bb-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-152">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="b42bb-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b42bb-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="b42bb-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-154">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="b42bb-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b42bb-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="b42bb-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-156">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="b42bb-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b42bb-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="b42bb-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-158">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="b42bb-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b42bb-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="b42bb-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-160">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="b42bb-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b42bb-161">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b42bb-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b42bb-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-164">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b42bb-164">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-165">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b42bb-165">Short description of the object.</span></span>

<span data-ttu-id="b42bb-166">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-167">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b42bb-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-168">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b42bb-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-170">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b42bb-170">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-171">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b42bb-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="b42bb-172">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b42bb-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b42bb-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="b42bb-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-175">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b42bb-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b42bb-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b42bb-177">(1)</span><span class="sxs-lookup"><span data-stu-id="b42bb-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-178">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="b42bb-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b42bb-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b42bb-180">(2)</span><span class="sxs-lookup"><span data-stu-id="b42bb-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b42bb-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b42bb-182">(3)</span><span class="sxs-lookup"><span data-stu-id="b42bb-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-183">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="b42bb-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b42bb-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b42bb-185">(4)</span><span class="sxs-lookup"><span data-stu-id="b42bb-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-186">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b42bb-186">Device is not working properly.</span></span> <span data-ttu-id="b42bb-187">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="b42bb-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b42bb-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b42bb-189">(5)</span><span class="sxs-lookup"><span data-stu-id="b42bb-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-190">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="b42bb-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b42bb-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b42bb-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="b42bb-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-193">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b42bb-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b42bb-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b42bb-195">(7)</span><span class="sxs-lookup"><span data-stu-id="b42bb-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b42bb-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b42bb-197">(8)</span><span class="sxs-lookup"><span data-stu-id="b42bb-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-198">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="b42bb-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b42bb-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b42bb-200">(9)</span><span class="sxs-lookup"><span data-stu-id="b42bb-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-201">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b42bb-201">Device is not working properly.</span></span> <span data-ttu-id="b42bb-202">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b42bb-202">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b42bb-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b42bb-204">(10)</span><span class="sxs-lookup"><span data-stu-id="b42bb-204">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-205">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b42bb-205">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b42bb-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b42bb-207">(11)</span><span class="sxs-lookup"><span data-stu-id="b42bb-207">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-208">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b42bb-208">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b42bb-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b42bb-210">12</span><span class="sxs-lookup"><span data-stu-id="b42bb-210">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-211">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="b42bb-211">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b42bb-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b42bb-213">(13)</span><span class="sxs-lookup"><span data-stu-id="b42bb-213">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-214">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b42bb-214">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b42bb-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b42bb-216">(14)</span><span class="sxs-lookup"><span data-stu-id="b42bb-216">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-217">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="b42bb-217">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b42bb-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b42bb-219">(15)</span><span class="sxs-lookup"><span data-stu-id="b42bb-219">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-220">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="b42bb-220">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b42bb-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b42bb-222">(16)</span><span class="sxs-lookup"><span data-stu-id="b42bb-222">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-223">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b42bb-223">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b42bb-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b42bb-225">(17)</span><span class="sxs-lookup"><span data-stu-id="b42bb-225">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-226">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b42bb-226">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b42bb-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b42bb-228">(18)</span><span class="sxs-lookup"><span data-stu-id="b42bb-228">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-229">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b42bb-229">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b42bb-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b42bb-231">(19)</span><span class="sxs-lookup"><span data-stu-id="b42bb-231">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b42bb-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b42bb-233">(20)</span><span class="sxs-lookup"><span data-stu-id="b42bb-233">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-234">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="b42bb-234">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b42bb-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b42bb-236">(21)</span><span class="sxs-lookup"><span data-stu-id="b42bb-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-237">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="b42bb-237">System failure.</span></span> <span data-ttu-id="b42bb-238">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b42bb-238">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b42bb-239">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b42bb-239">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b42bb-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b42bb-241">(22)</span><span class="sxs-lookup"><span data-stu-id="b42bb-241">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-242">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b42bb-242">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b42bb-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b42bb-244">(23)</span><span class="sxs-lookup"><span data-stu-id="b42bb-244">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-245">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="b42bb-245">System failure.</span></span> <span data-ttu-id="b42bb-246">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b42bb-246">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b42bb-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b42bb-248">(24)</span><span class="sxs-lookup"><span data-stu-id="b42bb-248">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-249">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="b42bb-249">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b42bb-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b42bb-251">(25)</span><span class="sxs-lookup"><span data-stu-id="b42bb-251">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-252">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b42bb-252">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b42bb-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b42bb-254">(26)</span><span class="sxs-lookup"><span data-stu-id="b42bb-254">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-255">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b42bb-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b42bb-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b42bb-257">(27)</span><span class="sxs-lookup"><span data-stu-id="b42bb-257">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-258">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="b42bb-258">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b42bb-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b42bb-260">(28)</span><span class="sxs-lookup"><span data-stu-id="b42bb-260">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-261">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="b42bb-261">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b42bb-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b42bb-263">(29)</span><span class="sxs-lookup"><span data-stu-id="b42bb-263">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-264">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b42bb-264">Device is disabled.</span></span> <span data-ttu-id="b42bb-265">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="b42bb-265">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b42bb-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b42bb-267">(30)</span><span class="sxs-lookup"><span data-stu-id="b42bb-267">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-268">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b42bb-268">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b42bb-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b42bb-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b42bb-270">31</span><span class="sxs-lookup"><span data-stu-id="b42bb-270">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-271">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b42bb-271">Device is not working properly.</span></span> <span data-ttu-id="b42bb-272">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="b42bb-272">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b42bb-273">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b42bb-273">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-274">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b42bb-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-276">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b42bb-276">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-277">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b42bb-277">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b42bb-278">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-279">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b42bb-279">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-280">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b42bb-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-282">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="b42bb-282">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-283">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="b42bb-283">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b42bb-284">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="b42bb-284">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b42bb-285">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-286">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b42bb-286">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-287">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b42bb-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-289">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b42bb-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-290">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b42bb-290">Description of the object.</span></span>

<span data-ttu-id="b42bb-291">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-292">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b42bb-292">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-293">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b42bb-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-295">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b42bb-295">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-296">Identificatore univoco del dispositivo di puntamento con altri dispositivi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b42bb-296">Unique identifier of the pointing device with other devices on the system.</span></span>

<span data-ttu-id="b42bb-297">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-298">**DeviceInterface**</span><span class="sxs-lookup"><span data-stu-id="b42bb-298">**DeviceInterface**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-299">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b42bb-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-301">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 21 \| Interface")</span><span class="sxs-lookup"><span data-stu-id="b42bb-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 21\|Interface")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-302">Tipo di interfaccia utilizzata per il dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="b42bb-302">Type of interface used for the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b42bb-303">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b42bb-303">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b42bb-304">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b42bb-304">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial"></span><span id="serial"></span><span id="SERIAL"></span>

<span data-ttu-id="b42bb-305">**Seriale** (3)</span><span class="sxs-lookup"><span data-stu-id="b42bb-305">**Serial** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="b42bb-306">**PS/2** (4)</span><span class="sxs-lookup"><span data-stu-id="b42bb-306">**PS/2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="b42bb-307">**Infrarossi** (5)</span><span class="sxs-lookup"><span data-stu-id="b42bb-307">**Infrared** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="b42bb-308">**HP-** b (6)</span><span class="sxs-lookup"><span data-stu-id="b42bb-308">**HP-HIL** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="b42bb-309">**Mouse bus** (7)</span><span class="sxs-lookup"><span data-stu-id="b42bb-309">**Bus mouse** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB__Apple_Desktop_Bus_"></span><span id="adb__apple_desktop_bus_"></span><span id="ADB__APPLE_DESKTOP_BUS_"></span>

<span data-ttu-id="b42bb-310">**ADB (Apple Desktop Bus)** (8)</span><span class="sxs-lookup"><span data-stu-id="b42bb-310">**ADB (Apple Desktop Bus)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse_DB-9"></span><span id="bus_mouse_db-9"></span><span id="BUS_MOUSE_DB-9"></span>

<span data-ttu-id="b42bb-311">**DB mouse bus-9** (160)</span><span class="sxs-lookup"><span data-stu-id="b42bb-311">**Bus mouse DB-9** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse_micro-DIN"></span><span id="bus_mouse_micro-din"></span><span id="BUS_MOUSE_MICRO-DIN"></span>

<span data-ttu-id="b42bb-312">**Micro-DIN del bus** (161)</span><span class="sxs-lookup"><span data-stu-id="b42bb-312">**Bus mouse micro-DIN** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="b42bb-313">**USB** (162)</span><span class="sxs-lookup"><span data-stu-id="b42bb-313">**USB** (162)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b42bb-314">**DoubleSpeedThreshold**</span><span class="sxs-lookup"><span data-stu-id="b42bb-314">**DoubleSpeedThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-315">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b42bb-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-317">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions \| SystemParametersInfo"), [**unità**](../wmisdk/standard-qualifiers.md) ("mickeys")</span><span class="sxs-lookup"><span data-stu-id="b42bb-317">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-318">Uno dei due valori di accelerazione.</span><span class="sxs-lookup"><span data-stu-id="b42bb-318">One of two acceleration values.</span></span> <span data-ttu-id="b42bb-319">La sensibilità del dispositivo di puntamento raddoppia (passa dal primo al secondo valore) quando il dispositivo di puntamento sposta una distanza maggiore di questo valore soglia.</span><span class="sxs-lookup"><span data-stu-id="b42bb-319">The sensitivity of the pointing device doubles (toggles from the first to the second value) when the pointing device moves a distance greater than this threshold value.</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b42bb-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-321">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b42bb-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-323">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="b42bb-323">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="b42bb-324">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b42bb-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-326">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b42bb-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-328">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="b42bb-328">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="b42bb-329">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-330">**Mano**</span><span class="sxs-lookup"><span data-stu-id="b42bb-330">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-331">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b42bb-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-333">Configurazione del dispositivo di puntamento per l'operazione a sinistra o a destra.</span><span class="sxs-lookup"><span data-stu-id="b42bb-333">Configuration of the pointing device for left-hand or right-hand operation.</span></span>

<span data-ttu-id="b42bb-334">Questa proprietà viene ereditata da [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-334">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b42bb-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b42bb-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b42bb-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (1)</span><span class="sxs-lookup"><span data-stu-id="b42bb-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="b42bb-337"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Operazione gestita a destra** (2)</span><span class="sxs-lookup"><span data-stu-id="b42bb-337"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Right Handed Operation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-338">Operazione Right-Handed</span><span class="sxs-lookup"><span data-stu-id="b42bb-338">Right-Handed Operation</span></span>

</dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="b42bb-339"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Operazione a sinistra** (3)</span><span class="sxs-lookup"><span data-stu-id="b42bb-339"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Left Handed Operation** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-340">Operazione Left-Handed</span><span class="sxs-lookup"><span data-stu-id="b42bb-340">Left-Handed Operation</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b42bb-341">**HardwareType**</span><span class="sxs-lookup"><span data-stu-id="b42bb-341">**HardwareType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-342">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b42bb-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-344">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ Local \_ computer \\ \\ System \\ \\ ControlSet001 \\ \\ Control \\ \\ Class \| DriverDesc")</span><span class="sxs-lookup"><span data-stu-id="b42bb-344">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\ControlSet001\\\\Control\\\\Class\|DriverDesc")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-345">Tipo di hardware utilizzato per il dispositivo di puntamento di Windows.</span><span class="sxs-lookup"><span data-stu-id="b42bb-345">Type of hardware used for the Windows pointing device.</span></span>

<span data-ttu-id="b42bb-346">Esempio: "MOUSE MICROSOFT PS2"</span><span class="sxs-lookup"><span data-stu-id="b42bb-346">Example: "MICROSOFT PS2 MOUSE"</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-347">**InfFileName**</span><span class="sxs-lookup"><span data-stu-id="b42bb-347">**InfFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-348">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b42bb-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-350">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ Local \_ computer \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfPath")</span><span class="sxs-lookup"><span data-stu-id="b42bb-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-351">Nome del file con estensione inf per il dispositivo di puntamento di Windows.</span><span class="sxs-lookup"><span data-stu-id="b42bb-351">Name of the .inf file for the Windows pointing device.</span></span>

<span data-ttu-id="b42bb-352">Esempio: "ab. inf"</span><span class="sxs-lookup"><span data-stu-id="b42bb-352">Example: "ab.inf"</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-353">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="b42bb-353">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-354">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b42bb-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-356">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ Local \_ computer \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfSection")</span><span class="sxs-lookup"><span data-stu-id="b42bb-356">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-357">Sezione del file con estensione inf che include le informazioni di configurazione per il dispositivo di puntamento di Windows.</span><span class="sxs-lookup"><span data-stu-id="b42bb-357">Section of the .inf file that holds configuration information for the Windows pointing device.</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-358">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b42bb-358">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-359">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b42bb-359">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-360">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-361">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="b42bb-361">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-362">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b42bb-362">Date and time the object was installed.</span></span> <span data-ttu-id="b42bb-363">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="b42bb-363">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b42bb-364">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-364">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-365">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="b42bb-365">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-366">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b42bb-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-368">Se **true**, il dispositivo è bloccato impedendo l'input o l'output dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b42bb-368">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="b42bb-369">Questa proprietà viene ereditata da [**CIM \_ UserDevice**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-369">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-370">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b42bb-370">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-371">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b42bb-371">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-373">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b42bb-373">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b42bb-374">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-375">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="b42bb-375">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-376">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b42bb-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-378">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b42bb-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-379">Nome del produttore del processore.</span><span class="sxs-lookup"><span data-stu-id="b42bb-379">Name of the processor's manufacturer.</span></span>

<span data-ttu-id="b42bb-380">Esempio: "GenuineSilicon"</span><span class="sxs-lookup"><span data-stu-id="b42bb-380">Example: "GenuineSilicon"</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-381">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b42bb-381">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-382">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b42bb-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-384">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b42bb-384">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-385">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="b42bb-385">Label by which the object is known.</span></span> <span data-ttu-id="b42bb-386">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="b42bb-386">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b42bb-387">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-387">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-388">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="b42bb-388">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-389">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b42bb-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-391">Numero di pulsanti sul dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="b42bb-391">Number of buttons on the pointing device.</span></span>

<span data-ttu-id="b42bb-392">Questa proprietà viene ereditata da [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-392">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<span data-ttu-id="b42bb-393">Esempio: 2</span><span class="sxs-lookup"><span data-stu-id="b42bb-393">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-394">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b42bb-394">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-395">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b42bb-395">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-396">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-397">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b42bb-397">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-398">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b42bb-398">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b42bb-399">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b42bb-400">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b42bb-400">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-401">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="b42bb-401">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-402">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b42bb-402">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-403">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-404">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF che \| punta al dispositivo \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="b42bb-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Pointing Device\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-405">Tipo di dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="b42bb-405">Type of pointing device.</span></span>

<span data-ttu-id="b42bb-406">Questa proprietà viene ereditata da [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-406">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b42bb-407"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b42bb-407"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b42bb-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b42bb-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="b42bb-409"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span><span class="sxs-lookup"><span data-stu-id="b42bb-409"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="b42bb-410"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Track Ball** (4)</span><span class="sxs-lookup"><span data-stu-id="b42bb-410"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Track Ball** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-411">Trackball</span><span class="sxs-lookup"><span data-stu-id="b42bb-411">Trackball</span></span>

</dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="b42bb-412"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Track point** (5)</span><span class="sxs-lookup"><span data-stu-id="b42bb-412"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="b42bb-413"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Punto di scorrimento** (6)</span><span class="sxs-lookup"><span data-stu-id="b42bb-413"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="b42bb-414"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touch pad** (7)</span><span class="sxs-lookup"><span data-stu-id="b42bb-414"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="b42bb-415"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Touchscreen** (8)</span><span class="sxs-lookup"><span data-stu-id="b42bb-415"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="b42bb-416"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Sensore ottico del mouse** (9)</span><span class="sxs-lookup"><span data-stu-id="b42bb-416"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b42bb-417">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b42bb-417">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-418">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b42bb-418">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-419">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-420">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b42bb-420">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b42bb-421">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="b42bb-421">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b42bb-422"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b42bb-422"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b42bb-423"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="b42bb-423"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b42bb-424"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="b42bb-424"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b42bb-425"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="b42bb-425"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-426">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="b42bb-426">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b42bb-427"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="b42bb-427"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-428">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="b42bb-428">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b42bb-429"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="b42bb-429"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-430">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="b42bb-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b42bb-431">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="b42bb-431">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b42bb-432">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-432">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b42bb-433"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="b42bb-433"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-434">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="b42bb-434">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b42bb-435"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="b42bb-435"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b42bb-436">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="b42bb-436">Timed Power-On Supported</span></span>

<span data-ttu-id="b42bb-437">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="b42bb-437">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b42bb-438">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b42bb-438">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-439">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b42bb-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-440">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-441">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="b42bb-441">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="b42bb-442">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="b42bb-442">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="b42bb-443">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-443">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-444">**QuadSpeedThreshold**</span><span class="sxs-lookup"><span data-stu-id="b42bb-444">**QuadSpeedThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-445">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b42bb-445">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-446">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-447">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions \| SystemParametersInfo"), [**unità**](../wmisdk/standard-qualifiers.md) ("mickeys")</span><span class="sxs-lookup"><span data-stu-id="b42bb-447">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-448">Uno dei due valori di soglia di accelerazione.</span><span class="sxs-lookup"><span data-stu-id="b42bb-448">One of two acceleration threshold values.</span></span> <span data-ttu-id="b42bb-449">Il sistema raddoppia la velocità del movimento del puntatore quando il dispositivo puntatore Sposta una distanza maggiore rispetto a questo valore.</span><span class="sxs-lookup"><span data-stu-id="b42bb-449">The system doubles the speed of the pointer movement when the pointer device moves a distance greater than this value.</span></span> <span data-ttu-id="b42bb-450">Poiché questo aumento della velocità si verifica dopo che il valore di **DoubleSpeedThreshold** è stato raggiunto, il puntatore si sposta in modo efficace quattro volte la velocità originale.</span><span class="sxs-lookup"><span data-stu-id="b42bb-450">Because this speed increase occurs after the **DoubleSpeedThreshold** value has been met, the pointer effectively moves at four times its original speed.</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-451">**Risoluzione**</span><span class="sxs-lookup"><span data-stu-id="b42bb-451">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-452">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b42bb-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-453">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-454">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("conteggi per pollice")</span><span class="sxs-lookup"><span data-stu-id="b42bb-454">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("counts per inch")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-455">Risoluzione del rilevamento.</span><span class="sxs-lookup"><span data-stu-id="b42bb-455">Tracking resolution.</span></span>

<span data-ttu-id="b42bb-456">Questa proprietà viene ereditata da [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-456">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<span data-ttu-id="b42bb-457">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="b42bb-457">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-458">**SampleRate**</span><span class="sxs-lookup"><span data-stu-id="b42bb-458">**SampleRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-459">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b42bb-459">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-460">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-461">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sampleRate"), [**unità**](../wmisdk/standard-qualifiers.md) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="b42bb-461">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SampleRate"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-462">Frequenza con cui viene eseguito il polling del dispositivo di puntamento per le informazioni di input.</span><span class="sxs-lookup"><span data-stu-id="b42bb-462">Rate at which the pointing device is polled for input information.</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-463">**Status**</span><span class="sxs-lookup"><span data-stu-id="b42bb-463">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-464">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b42bb-464">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-465">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-466">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="b42bb-466">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-467">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b42bb-467">Current status of the object.</span></span> <span data-ttu-id="b42bb-468">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="b42bb-468">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b42bb-469">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="b42bb-469">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b42bb-470">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="b42bb-470">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b42bb-471">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="b42bb-471">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b42bb-472">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="b42bb-472">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b42bb-473">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-473">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b42bb-474">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="b42bb-474">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b42bb-475">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b42bb-475">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b42bb-476">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="b42bb-476">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b42bb-477">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="b42bb-477">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b42bb-478">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="b42bb-478">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b42bb-479">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="b42bb-479">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b42bb-480">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="b42bb-480">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b42bb-481">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="b42bb-481">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b42bb-482">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="b42bb-482">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b42bb-483">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="b42bb-483">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b42bb-484">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="b42bb-484">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b42bb-485">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="b42bb-485">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b42bb-486">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="b42bb-486">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b42bb-487">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b42bb-487">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-488">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b42bb-488">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-489">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-490">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b42bb-490">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-491">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b42bb-491">State of the logical device.</span></span> <span data-ttu-id="b42bb-492">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="b42bb-492">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b42bb-493">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-493">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b42bb-494">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b42bb-494">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b42bb-495">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="b42bb-495">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b42bb-496">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="b42bb-496">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b42bb-497">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="b42bb-497">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b42bb-498">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="b42bb-498">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b42bb-499">**Sincronizzazione**</span><span class="sxs-lookup"><span data-stu-id="b42bb-499">**Synch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-500">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b42bb-500">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-501">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-501">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-502">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| MouseSynchIn100ns"), [**unità**](../wmisdk/standard-qualifiers.md) ("100 nanosecondi")</span><span class="sxs-lookup"><span data-stu-id="b42bb-502">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|MouseSynchIn100ns"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-503">Periodo di tempo dopo il quale si presuppone l'interruzione successiva per indicare l'inizio di un nuovo pacchetto del dispositivo (i pacchetti parziali vengono eliminati).</span><span class="sxs-lookup"><span data-stu-id="b42bb-503">Length of time after which the next interrupt is assumed to indicate the start of a new device packet (partial packets are discarded).</span></span> <span data-ttu-id="b42bb-504">In caso di perdita di un interrupt, questo consente al driver del dispositivo di puntamento di sincronizzare la rappresentazione interna dello stato del pacchetto con lo stato hardware.</span><span class="sxs-lookup"><span data-stu-id="b42bb-504">In the event that an interrupt is lost, this allows the pointing device driver to synchronize its internal representation of the packet state with the hardware state.</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-505">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b42bb-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-506">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b42bb-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-507">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-508">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="b42bb-508">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-509">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="b42bb-509">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="b42bb-510">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b42bb-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b42bb-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b42bb-512">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b42bb-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-513">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b42bb-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b42bb-514">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="b42bb-514">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="b42bb-515">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="b42bb-515">Name of the scoping system.</span></span>

<span data-ttu-id="b42bb-516">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b42bb-517">Commenti</span><span class="sxs-lookup"><span data-stu-id="b42bb-517">Remarks</span></span>

<span data-ttu-id="b42bb-518">La classe **Win32 \_ PointingDevice** è derivata da [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b42bb-518">The **Win32\_PointingDevice** class is derived from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b42bb-519">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b42bb-519">Requirements</span></span>



| <span data-ttu-id="b42bb-520">Requisito</span><span class="sxs-lookup"><span data-stu-id="b42bb-520">Requirement</span></span> | <span data-ttu-id="b42bb-521">Valore</span><span class="sxs-lookup"><span data-stu-id="b42bb-521">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b42bb-522">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b42bb-522">Minimum supported client</span></span><br/> | <span data-ttu-id="b42bb-523">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b42bb-523">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b42bb-524">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b42bb-524">Minimum supported server</span></span><br/> | <span data-ttu-id="b42bb-525">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b42bb-525">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b42bb-526">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b42bb-526">Namespace</span></span><br/>                | <span data-ttu-id="b42bb-527">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b42bb-527">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b42bb-528">MOF</span><span class="sxs-lookup"><span data-stu-id="b42bb-528">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b42bb-529"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b42bb-529"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b42bb-530">DLL</span><span class="sxs-lookup"><span data-stu-id="b42bb-530">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b42bb-531"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b42bb-531"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b42bb-532">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b42bb-532">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b42bb-533">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b42bb-533">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="b42bb-534">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="b42bb-534">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
