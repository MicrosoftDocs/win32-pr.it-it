---
description: La \_ classe WMI controller SCSI Win32 rappresenta un controller SCSI in un sistema di computer che esegue Windows.
ms.assetid: 14ed523e-d505-40fa-81d5-3a71eb9f078e
ms.tgt_platform: multiple
title: Classe Win32_SCSIController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIController
- Win32_SCSIController.Reset
- Win32_SCSIController.SetPowerState
- Win32_SCSIController.Availability
- Win32_SCSIController.Caption
- Win32_SCSIController.ConfigManagerErrorCode
- Win32_SCSIController.ConfigManagerUserConfig
- Win32_SCSIController.ControllerTimeouts
- Win32_SCSIController.CreationClassName
- Win32_SCSIController.Description
- Win32_SCSIController.DeviceID
- Win32_SCSIController.DeviceMap
- Win32_SCSIController.DriverName
- Win32_SCSIController.ErrorCleared
- Win32_SCSIController.ErrorDescription
- Win32_SCSIController.HardwareVersion
- Win32_SCSIController.Index
- Win32_SCSIController.InstallDate
- Win32_SCSIController.LastErrorCode
- Win32_SCSIController.Manufacturer
- Win32_SCSIController.MaxDataWidth
- Win32_SCSIController.MaxNumberControlled
- Win32_SCSIController.MaxTransferRate
- Win32_SCSIController.Name
- Win32_SCSIController.PNPDeviceID
- Win32_SCSIController.PowerManagementCapabilities
- Win32_SCSIController.PowerManagementSupported
- Win32_SCSIController.ProtectionManagement
- Win32_SCSIController.ProtocolSupported
- Win32_SCSIController.Status
- Win32_SCSIController.StatusInfo
- Win32_SCSIController.SystemCreationClassName
- Win32_SCSIController.SystemName
- Win32_SCSIController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f8ba77d626ada787ed18fd9855333fa813f3ab7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305266"
---
# <a name="win32_scsicontroller-class"></a><span data-ttu-id="939ce-103">Win32 \_ controller SCSI (classe)</span><span class="sxs-lookup"><span data-stu-id="939ce-103">Win32\_SCSIController class</span></span>

<span data-ttu-id="939ce-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ controller SCSI Win32** rappresenta un controller SCSI in un sistema di computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="939ce-104">The **Win32\_SCSIController** [WMI class](../wmisdk/retrieving-a-class.md) represents a SCSI controller on a computer system running Windows.</span></span>

<span data-ttu-id="939ce-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="939ce-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="939ce-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="939ce-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="939ce-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="939ce-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SCSIController : CIM_SCSIController
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  uint32   ControllerTimeouts;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  string   DeviceMap;
  string   DriverName;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   HardwareVersion;
  uint32   Index;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint32   MaxDataWidth;
  uint32   MaxNumberControlled;
  uint64   MaxTransferRate;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtectionManagement;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="939ce-108">Members</span><span class="sxs-lookup"><span data-stu-id="939ce-108">Members</span></span>

<span data-ttu-id="939ce-109">La classe **Win32 \_ controller SCSI** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="939ce-109">The **Win32\_SCSIController** class has these types of members:</span></span>

-   [<span data-ttu-id="939ce-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="939ce-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="939ce-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="939ce-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="939ce-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="939ce-112">Methods</span></span>

<span data-ttu-id="939ce-113">La classe **Win32 \_ controller SCSI** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="939ce-113">The **Win32\_SCSIController** class has these methods.</span></span>



| <span data-ttu-id="939ce-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="939ce-114">Method</span></span>            | <span data-ttu-id="939ce-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="939ce-115">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="939ce-116">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="939ce-116">**Reset**</span></span>         | <span data-ttu-id="939ce-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="939ce-117">Not implemented.</span></span> <span data-ttu-id="939ce-118">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ controller SCSI**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span><br/>                 |
| <span data-ttu-id="939ce-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="939ce-119">**SetPowerState**</span></span> | <span data-ttu-id="939ce-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="939ce-120">Not implemented.</span></span> <span data-ttu-id="939ce-121">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ controller SCSI**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="939ce-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="939ce-122">Properties</span></span>

<span data-ttu-id="939ce-123">La classe **Win32 \_ controller SCSI** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="939ce-123">The **Win32\_SCSIController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="939ce-124">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="939ce-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="939ce-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-127">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="939ce-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-128">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="939ce-128">Availability and status of the device.</span></span>

<span data-ttu-id="939ce-129">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="939ce-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="939ce-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="939ce-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="939ce-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="939ce-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="939ce-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-133">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="939ce-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="939ce-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="939ce-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="939ce-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="939ce-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="939ce-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="939ce-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="939ce-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="939ce-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="939ce-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="939ce-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="939ce-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="939ce-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="939ce-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="939ce-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="939ce-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="939ce-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="939ce-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="939ce-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="939ce-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="939ce-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-144">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="939ce-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="939ce-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="939ce-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-146">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="939ce-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="939ce-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="939ce-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-148">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="939ce-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="939ce-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="939ce-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="939ce-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="939ce-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-151">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="939ce-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="939ce-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="939ce-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-153">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="939ce-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="939ce-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="939ce-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-155">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="939ce-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="939ce-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="939ce-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-157">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="939ce-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="939ce-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="939ce-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-159">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="939ce-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="939ce-160">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="939ce-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="939ce-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-163">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="939ce-163">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-164">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="939ce-164">Short description of the object.</span></span>

<span data-ttu-id="939ce-165">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="939ce-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-167">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="939ce-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-169">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="939ce-169">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-170">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="939ce-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="939ce-171">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="939ce-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="939ce-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="939ce-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="939ce-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-174">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="939ce-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="939ce-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="939ce-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="939ce-176">(1)</span><span class="sxs-lookup"><span data-stu-id="939ce-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-177">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="939ce-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="939ce-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="939ce-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="939ce-179">(2)</span><span class="sxs-lookup"><span data-stu-id="939ce-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="939ce-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="939ce-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="939ce-181">(3)</span><span class="sxs-lookup"><span data-stu-id="939ce-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-182">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="939ce-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="939ce-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="939ce-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="939ce-184">(4)</span><span class="sxs-lookup"><span data-stu-id="939ce-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-185">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="939ce-185">Device is not working properly.</span></span> <span data-ttu-id="939ce-186">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="939ce-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="939ce-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="939ce-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="939ce-188">(5)</span><span class="sxs-lookup"><span data-stu-id="939ce-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-189">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="939ce-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="939ce-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="939ce-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="939ce-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="939ce-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-192">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="939ce-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="939ce-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="939ce-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="939ce-194">(7)</span><span class="sxs-lookup"><span data-stu-id="939ce-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="939ce-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="939ce-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="939ce-196">(8)</span><span class="sxs-lookup"><span data-stu-id="939ce-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-197">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="939ce-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="939ce-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="939ce-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="939ce-199">(9)</span><span class="sxs-lookup"><span data-stu-id="939ce-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-200">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="939ce-200">Device is not working properly.</span></span> <span data-ttu-id="939ce-201">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="939ce-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="939ce-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="939ce-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="939ce-203">(10)</span><span class="sxs-lookup"><span data-stu-id="939ce-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-204">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="939ce-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="939ce-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="939ce-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="939ce-206">(11)</span><span class="sxs-lookup"><span data-stu-id="939ce-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-207">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="939ce-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="939ce-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="939ce-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="939ce-209">12</span><span class="sxs-lookup"><span data-stu-id="939ce-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-210">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="939ce-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="939ce-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="939ce-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="939ce-212">(13)</span><span class="sxs-lookup"><span data-stu-id="939ce-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-213">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="939ce-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="939ce-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="939ce-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="939ce-215">(14)</span><span class="sxs-lookup"><span data-stu-id="939ce-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-216">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="939ce-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="939ce-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="939ce-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="939ce-218">(15)</span><span class="sxs-lookup"><span data-stu-id="939ce-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-219">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="939ce-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="939ce-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="939ce-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="939ce-221">(16)</span><span class="sxs-lookup"><span data-stu-id="939ce-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-222">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="939ce-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="939ce-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="939ce-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="939ce-224">(17)</span><span class="sxs-lookup"><span data-stu-id="939ce-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-225">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="939ce-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="939ce-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="939ce-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="939ce-227">(18)</span><span class="sxs-lookup"><span data-stu-id="939ce-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-228">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="939ce-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="939ce-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="939ce-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="939ce-230">(19)</span><span class="sxs-lookup"><span data-stu-id="939ce-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="939ce-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="939ce-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="939ce-232">(20)</span><span class="sxs-lookup"><span data-stu-id="939ce-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-233">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="939ce-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="939ce-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="939ce-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="939ce-235">(21)</span><span class="sxs-lookup"><span data-stu-id="939ce-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-236">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="939ce-236">System failure.</span></span> <span data-ttu-id="939ce-237">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="939ce-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="939ce-238">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="939ce-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="939ce-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="939ce-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="939ce-240">(22)</span><span class="sxs-lookup"><span data-stu-id="939ce-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-241">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="939ce-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="939ce-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="939ce-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="939ce-243">(23)</span><span class="sxs-lookup"><span data-stu-id="939ce-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-244">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="939ce-244">System failure.</span></span> <span data-ttu-id="939ce-245">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="939ce-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="939ce-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="939ce-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="939ce-247">(24)</span><span class="sxs-lookup"><span data-stu-id="939ce-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-248">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="939ce-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="939ce-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="939ce-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="939ce-250">(25)</span><span class="sxs-lookup"><span data-stu-id="939ce-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-251">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="939ce-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="939ce-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="939ce-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="939ce-253">(26)</span><span class="sxs-lookup"><span data-stu-id="939ce-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-254">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="939ce-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="939ce-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="939ce-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="939ce-256">(27)</span><span class="sxs-lookup"><span data-stu-id="939ce-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-257">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="939ce-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="939ce-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="939ce-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="939ce-259">(28)</span><span class="sxs-lookup"><span data-stu-id="939ce-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-260">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="939ce-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="939ce-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="939ce-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="939ce-262">(29)</span><span class="sxs-lookup"><span data-stu-id="939ce-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-263">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="939ce-263">Device is disabled.</span></span> <span data-ttu-id="939ce-264">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="939ce-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="939ce-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="939ce-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="939ce-266">(30)</span><span class="sxs-lookup"><span data-stu-id="939ce-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-267">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="939ce-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="939ce-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="939ce-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="939ce-269">31</span><span class="sxs-lookup"><span data-stu-id="939ce-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-270">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="939ce-270">Device is not working properly.</span></span> <span data-ttu-id="939ce-271">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="939ce-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="939ce-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="939ce-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-273">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="939ce-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-275">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="939ce-275">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-276">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="939ce-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="939ce-277">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-278">**ControllerTimeouts**</span><span class="sxs-lookup"><span data-stu-id="939ce-278">**ControllerTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-279">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="939ce-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="939ce-281">Numero di timeout che si sono verificati dopo il valore di **TimeOfLastReset** .</span><span class="sxs-lookup"><span data-stu-id="939ce-281">Number of time-outs that have occurred after the **TimeOfLastReset** value.</span></span>

<span data-ttu-id="939ce-282">Questa proprietà viene ereditata da [**CIM \_ controller SCSI**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-282">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="939ce-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-284">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="939ce-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-286">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="939ce-286">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="939ce-287">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="939ce-287">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="939ce-288">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="939ce-288">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="939ce-289">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-290">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="939ce-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-291">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="939ce-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-293">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="939ce-293">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-294">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="939ce-294">Description of the object.</span></span>

<span data-ttu-id="939ce-295">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-296">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="939ce-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-297">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="939ce-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-299">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ DeviceMap \\ \\ SCSI")</span><span class="sxs-lookup"><span data-stu-id="939ce-299">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-300">Identificatore univoco del controller SCSI con altri dispositivi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="939ce-300">Unique identifier of the SCSI controller with other devices on the system.</span></span>

<span data-ttu-id="939ce-301">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-302">**DeviceMap**</span><span class="sxs-lookup"><span data-stu-id="939ce-302">**DeviceMap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-303">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="939ce-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-305">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ DeviceMap \\ \\ SCSI \| SCSIPORT")</span><span class="sxs-lookup"><span data-stu-id="939ce-305">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi\|ScsiPort")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-306">Ordine in cui i dispositivi sono elencati con questo controller SCSI.</span><span class="sxs-lookup"><span data-stu-id="939ce-306">Order in which the devices are listed with this SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="939ce-307">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="939ce-307">**DriverName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-308">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="939ce-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-310">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| PortDriver")</span><span class="sxs-lookup"><span data-stu-id="939ce-310">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|PortDriver")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-311">Nome del file di driver del controller SCSI.</span><span class="sxs-lookup"><span data-stu-id="939ce-311">Driver file name of the SCSI controller.</span></span>

<span data-ttu-id="939ce-312">Esempio: "Adaptec"</span><span class="sxs-lookup"><span data-stu-id="939ce-312">Example: "Adaptec"</span></span>

</dd> <dt>

<span data-ttu-id="939ce-313">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="939ce-313">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-314">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="939ce-314">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="939ce-316">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="939ce-316">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="939ce-317">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-318">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="939ce-318">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-319">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="939ce-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="939ce-321">Stringa in formato libero che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="939ce-321">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="939ce-322">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-323">**HardwareVersion**</span><span class="sxs-lookup"><span data-stu-id="939ce-323">**HardwareVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="939ce-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-326">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ enum \\ \\ root \| HWRevision")</span><span class="sxs-lookup"><span data-stu-id="939ce-326">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Enum\\\\Root\|HWRevision")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-327">Numero di versione hardware del controller SCSI.</span><span class="sxs-lookup"><span data-stu-id="939ce-327">Hardware version number of the SCSI controller.</span></span>

<span data-ttu-id="939ce-328">Esempio: "1,25"</span><span class="sxs-lookup"><span data-stu-id="939ce-328">Example: "1.25"</span></span>

</dd> <dt>

<span data-ttu-id="939ce-329">**Index**</span><span class="sxs-lookup"><span data-stu-id="939ce-329">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-330">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="939ce-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-332">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ DeviceMap \\ \\ SCSI \| SCSIPORT")</span><span class="sxs-lookup"><span data-stu-id="939ce-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi\|ScsiPort")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-333">Numero di indice del controller SCSI nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="939ce-333">Index number of the SCSI controller in the system registry.</span></span>

<span data-ttu-id="939ce-334">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="939ce-334">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="939ce-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="939ce-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-336">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="939ce-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-338">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="939ce-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-339">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="939ce-339">Date and time the object was installed.</span></span> <span data-ttu-id="939ce-340">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="939ce-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="939ce-341">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-342">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="939ce-342">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-343">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="939ce-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="939ce-345">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="939ce-345">Last error code reported by the logical device.</span></span>

<span data-ttu-id="939ce-346">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-347">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="939ce-347">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-348">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="939ce-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-350">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ enum \\ \\ root \| MFG")</span><span class="sxs-lookup"><span data-stu-id="939ce-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Enum\\\\Root\|Mfg")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-351">Nome del produttore del controller SCSI.</span><span class="sxs-lookup"><span data-stu-id="939ce-351">Name of the SCSI controller manufacturer.</span></span>

<span data-ttu-id="939ce-352">Esempio: "Adaptec"</span><span class="sxs-lookup"><span data-stu-id="939ce-352">Example: "Adaptec"</span></span>

</dd> <dt>

<span data-ttu-id="939ce-353">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="939ce-353">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-354">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="939ce-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-356">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bits")</span><span class="sxs-lookup"><span data-stu-id="939ce-356">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-357">Larghezza massima dei dati (in bit) supportata dal controller SCSI.</span><span class="sxs-lookup"><span data-stu-id="939ce-357">Maximum data width (in bits) supported by the SCSI controller.</span></span>

<span data-ttu-id="939ce-358">Questa proprietà viene ereditata da [**CIM \_ controller SCSI**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-358">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-359">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="939ce-359">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-360">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="939ce-360">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-362">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="939ce-362">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-363">Numero massimo di entità indirizzabili direttamente supportato da questo controller.</span><span class="sxs-lookup"><span data-stu-id="939ce-363">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="939ce-364">Se il numero è sconosciuto, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="939ce-364">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="939ce-365">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-365">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-366">**MaxTransferRate**</span><span class="sxs-lookup"><span data-stu-id="939ce-366">**MaxTransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-367">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="939ce-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-369">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="939ce-369">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-370">Velocità massima di trasferimento (in bit al secondo) supportata dal controller SCSI.</span><span class="sxs-lookup"><span data-stu-id="939ce-370">Maximum transfer rate (in bits per second) supported by the SCSI controller.</span></span>

<span data-ttu-id="939ce-371">Questa proprietà viene ereditata da [**CIM \_ controller SCSI**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-371">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

<span data-ttu-id="939ce-372">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-372">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-373">**Nome**</span><span class="sxs-lookup"><span data-stu-id="939ce-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-374">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="939ce-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-376">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="939ce-376">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-377">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="939ce-377">Label by which the object is known.</span></span> <span data-ttu-id="939ce-378">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="939ce-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="939ce-379">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-380">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="939ce-380">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-381">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="939ce-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-383">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="939ce-383">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-384">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="939ce-384">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="939ce-385">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="939ce-386">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="939ce-386">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="939ce-387">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="939ce-387">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-388">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="939ce-388">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="939ce-389">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="939ce-390">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="939ce-390">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="939ce-391">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="939ce-391">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="939ce-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="939ce-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="939ce-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="939ce-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="939ce-394"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="939ce-394"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="939ce-395"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="939ce-395"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-396">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="939ce-396">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="939ce-397"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="939ce-397"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-398">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="939ce-398">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="939ce-399"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="939ce-399"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-400">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="939ce-400">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="939ce-401">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="939ce-401">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="939ce-402">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-402">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="939ce-403"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="939ce-403"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-404">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="939ce-404">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="939ce-405"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="939ce-405"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="939ce-406">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="939ce-406">Timed Power-On Supported</span></span>

<span data-ttu-id="939ce-407">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="939ce-407">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="939ce-408">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="939ce-408">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-409">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="939ce-409">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="939ce-411">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="939ce-411">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="939ce-412">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="939ce-412">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="939ce-413">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-414">**ProtectionManagement**</span><span class="sxs-lookup"><span data-stu-id="939ce-414">**ProtectionManagement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-415">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="939ce-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-417">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Controller di archiviazione DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="939ce-417">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Storage Controller\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-418">Supporto del controller SCSI per la ridondanza o la protezione in caso di errori del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="939ce-418">Support of the SCSI controller for redundancy or protection against device failures.</span></span>

<span data-ttu-id="939ce-419">Questa proprietà viene ereditata da [**CIM \_ controller SCSI**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-419">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="939ce-420">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="939ce-420">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="939ce-421">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="939ce-421">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span>

<span data-ttu-id="939ce-422">Non **protetto** (3)</span><span class="sxs-lookup"><span data-stu-id="939ce-422">**Unprotected** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span>

<span data-ttu-id="939ce-423">**Protetto** (4)</span><span class="sxs-lookup"><span data-stu-id="939ce-423">**Protected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC__SCSI-3_Controller_Command_"></span><span id="protected_through_scc__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="939ce-424">**Protetto tramite SCC (comando controller SCSI-3)** (5)</span><span class="sxs-lookup"><span data-stu-id="939ce-424">**Protected through SCC (SCSI-3 Controller Command)** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC-2__SCSI-3_Controller_Command_"></span><span id="protected_through_scc-2__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC-2__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="939ce-425">**Protetto tramite SCC-2 (comando controller SCSI-3)** (6)</span><span class="sxs-lookup"><span data-stu-id="939ce-425">**Protected through SCC-2 (SCSI-3 Controller Command)** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="939ce-426">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="939ce-426">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-427">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="939ce-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-428">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-429">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta bus DMTF \| 001,2 "," MIF. \|Dischi DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="939ce-429">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-430">Protocollo usato dal controller per accedere ai dispositivi "controllati".</span><span class="sxs-lookup"><span data-stu-id="939ce-430">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="939ce-431">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-431">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="939ce-432">Nell'elenco seguente sono riportati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="939ce-432">The following list shows the possible values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="939ce-433">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="939ce-433">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="939ce-434">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="939ce-434">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="939ce-435">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="939ce-435">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="939ce-436">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="939ce-436">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="939ce-437">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="939ce-437">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="939ce-438">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="939ce-438">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="939ce-439">**Dischetto flessibile** (7)</span><span class="sxs-lookup"><span data-stu-id="939ce-439">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="939ce-440">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="939ce-440">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="939ce-441">**Interfaccia parallela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="939ce-441">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="939ce-442">**Protocollo di Fibre Channel SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="939ce-442">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="939ce-443">**Protocollo bus seriale SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="939ce-443">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="939ce-444">**Protocollo bus seriale SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="939ce-444">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="939ce-445">**Architettura di archiviazione seriale SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="939ce-445">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="939ce-446">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="939ce-446">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="939ce-447">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="939ce-447">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="939ce-448">**Bus seriale universale** (16)</span><span class="sxs-lookup"><span data-stu-id="939ce-448">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="939ce-449">**Protocollo parallelo** (17)</span><span class="sxs-lookup"><span data-stu-id="939ce-449">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="939ce-450">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="939ce-450">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="939ce-451">**Diagnostica** (19)</span><span class="sxs-lookup"><span data-stu-id="939ce-451">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="939ce-452">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="939ce-452">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="939ce-453">**Potenza** (21)</span><span class="sxs-lookup"><span data-stu-id="939ce-453">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="939ce-454">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="939ce-454">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="939ce-455">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="939ce-455">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="939ce-456">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="939ce-456">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="939ce-457">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="939ce-457">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="939ce-458">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="939ce-458">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="939ce-459">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="939ce-459">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="939ce-460">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="939ce-460">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="939ce-461">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="939ce-461">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="939ce-462">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="939ce-462">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="939ce-463">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="939ce-463">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="939ce-464">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="939ce-464">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="939ce-465">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="939ce-465">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="939ce-466">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="939ce-466">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="939ce-467">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="939ce-467">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="939ce-468">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="939ce-468">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="939ce-469">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="939ce-469">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="939ce-470">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="939ce-470">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="939ce-471">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="939ce-471">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="939ce-472">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="939ce-472">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="939ce-473">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="939ce-473">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="939ce-474">**ATA/IDE avanzato** (42)</span><span class="sxs-lookup"><span data-stu-id="939ce-474">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="939ce-475">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="939ce-475">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="939ce-476">**TWIRP (infrarossi bidirezionali)** (44)</span><span class="sxs-lookup"><span data-stu-id="939ce-476">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="939ce-477">**FIR (infrarossi veloci)** (45)</span><span class="sxs-lookup"><span data-stu-id="939ce-477">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="939ce-478">**Sir (Serial Infrared)** (46)</span><span class="sxs-lookup"><span data-stu-id="939ce-478">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="939ce-479">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="939ce-479">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="939ce-480">**Status**</span><span class="sxs-lookup"><span data-stu-id="939ce-480">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-481">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="939ce-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-482">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-483">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="939ce-483">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-484">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="939ce-484">Current status of the object.</span></span> <span data-ttu-id="939ce-485">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="939ce-485">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="939ce-486">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="939ce-486">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="939ce-487">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="939ce-487">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="939ce-488">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="939ce-488">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="939ce-489">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="939ce-489">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="939ce-490">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-490">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="939ce-491">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="939ce-491">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="939ce-492">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="939ce-492">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="939ce-493">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="939ce-493">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="939ce-494">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="939ce-494">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="939ce-495">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="939ce-495">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="939ce-496">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="939ce-496">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="939ce-497">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="939ce-497">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="939ce-498">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="939ce-498">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="939ce-499">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="939ce-499">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="939ce-500">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="939ce-500">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="939ce-501">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="939ce-501">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="939ce-502">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="939ce-502">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="939ce-503">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="939ce-503">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="939ce-504">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="939ce-504">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-505">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="939ce-505">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-506">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-507">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="939ce-507">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="939ce-508">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="939ce-508">State of the logical device.</span></span> <span data-ttu-id="939ce-509">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="939ce-509">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="939ce-510">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="939ce-511">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="939ce-511">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="939ce-512">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="939ce-512">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="939ce-513">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="939ce-513">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="939ce-514">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="939ce-514">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="939ce-515">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="939ce-515">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="939ce-516">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="939ce-516">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-517">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="939ce-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-518">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-518">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-519">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="939ce-519">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="939ce-520">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="939ce-520">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="939ce-521">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-521">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-522">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="939ce-522">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-523">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="939ce-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-524">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="939ce-525">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="939ce-525">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="939ce-526">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="939ce-526">Name of the scoping system.</span></span>

<span data-ttu-id="939ce-527">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-527">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ce-528">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="939ce-528">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="939ce-529">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="939ce-529">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="939ce-530">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="939ce-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="939ce-531">Data e ora dell'ultima reimpostazione del controller.</span><span class="sxs-lookup"><span data-stu-id="939ce-531">Date and time this controller was last reset.</span></span> <span data-ttu-id="939ce-532">Questo potrebbe significare che il controller è stato spento o reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="939ce-532">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="939ce-533">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-533">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="939ce-534">Commenti</span><span class="sxs-lookup"><span data-stu-id="939ce-534">Remarks</span></span>

<span data-ttu-id="939ce-535">La classe **Win32 \_ controller SCSI** è derivata da [**CIM \_ controller SCSI**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="939ce-535">The **Win32\_SCSIController** class is derived from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="939ce-536">Requisiti</span><span class="sxs-lookup"><span data-stu-id="939ce-536">Requirements</span></span>



| <span data-ttu-id="939ce-537">Requisito</span><span class="sxs-lookup"><span data-stu-id="939ce-537">Requirement</span></span> | <span data-ttu-id="939ce-538">Valore</span><span class="sxs-lookup"><span data-stu-id="939ce-538">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="939ce-539">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="939ce-539">Minimum supported client</span></span><br/> | <span data-ttu-id="939ce-540">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="939ce-540">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="939ce-541">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="939ce-541">Minimum supported server</span></span><br/> | <span data-ttu-id="939ce-542">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="939ce-542">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="939ce-543">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="939ce-543">Namespace</span></span><br/>                | <span data-ttu-id="939ce-544">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="939ce-544">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="939ce-545">MOF</span><span class="sxs-lookup"><span data-stu-id="939ce-545">MOF</span></span><br/>                      | <dl> <span data-ttu-id="939ce-546"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="939ce-546"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="939ce-547">DLL</span><span class="sxs-lookup"><span data-stu-id="939ce-547">DLL</span></span><br/>                      | <dl> <span data-ttu-id="939ce-548"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="939ce-548"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="939ce-549">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="939ce-549">See also</span></span>

<dl> <dt>

[<span data-ttu-id="939ce-550">**\_Controller SCSI CIM**</span><span class="sxs-lookup"><span data-stu-id="939ce-550">**CIM\_SCSIController**</span></span>](cim-scsicontroller.md)
</dt> <dt>

[<span data-ttu-id="939ce-551">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="939ce-551">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
