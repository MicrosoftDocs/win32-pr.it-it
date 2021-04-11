---
description: Win32 \_ ParallelPort &\# 32; Classe WMI rappresenta le proprietà di una porta parallela in un computer che esegue Windows.
ms.assetid: 986bd27f-71b0-4a40-a421-a8bfc0f081be
ms.tgt_platform: multiple
title: Classe Win32_ParallelPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ParallelPort
- Win32_ParallelPort.Reset
- Win32_ParallelPort.SetPowerState
- Win32_ParallelPort.Availability
- Win32_ParallelPort.Capabilities
- Win32_ParallelPort.CapabilityDescriptions
- Win32_ParallelPort.Caption
- Win32_ParallelPort.ConfigManagerErrorCode
- Win32_ParallelPort.ConfigManagerUserConfig
- Win32_ParallelPort.CreationClassName
- Win32_ParallelPort.Description
- Win32_ParallelPort.DeviceID
- Win32_ParallelPort.DMASupport
- Win32_ParallelPort.ErrorCleared
- Win32_ParallelPort.ErrorDescription
- Win32_ParallelPort.InstallDate
- Win32_ParallelPort.LastErrorCode
- Win32_ParallelPort.MaxNumberControlled
- Win32_ParallelPort.Name
- Win32_ParallelPort.OSAutoDiscovered
- Win32_ParallelPort.PNPDeviceID
- Win32_ParallelPort.PowerManagementCapabilities
- Win32_ParallelPort.PowerManagementSupported
- Win32_ParallelPort.ProtocolSupported
- Win32_ParallelPort.Status
- Win32_ParallelPort.StatusInfo
- Win32_ParallelPort.SystemCreationClassName
- Win32_ParallelPort.SystemName
- Win32_ParallelPort.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: da2ed3b34f3655067fd5ae41c31424e7599789c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127455"
---
# <a name="win32_parallelport-class"></a><span data-ttu-id="98e21-103">Win32 \_ ParallelPort (classe)</span><span class="sxs-lookup"><span data-stu-id="98e21-103">Win32\_ParallelPort class</span></span>

<span data-ttu-id="98e21-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ ParallelPort Win32** rappresenta le proprietà di una porta parallela in un computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="98e21-104">The **Win32\_ParallelPort** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a parallel port on a computer system running Windows.</span></span>

<span data-ttu-id="98e21-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="98e21-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="98e21-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="98e21-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e21-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98e21-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class  Win32_ParallelPort : CIM_ParallelController
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  DMASupport;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxNumberControlled;
  string   Name;
  boolean  OSAutoDiscovered;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="98e21-108">Members</span><span class="sxs-lookup"><span data-stu-id="98e21-108">Members</span></span>

<span data-ttu-id="98e21-109">La classe **Win32 \_ ParallelPort** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="98e21-109">The **Win32\_ParallelPort** class has these types of members:</span></span>

-   [<span data-ttu-id="98e21-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="98e21-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="98e21-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="98e21-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="98e21-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="98e21-112">Methods</span></span>

<span data-ttu-id="98e21-113">La classe **Win32 \_ ParallelPort** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="98e21-113">The **Win32\_ParallelPort** class has these methods.</span></span>



| <span data-ttu-id="98e21-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="98e21-114">Method</span></span>            | <span data-ttu-id="98e21-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98e21-115">Description</span></span>                                                                                                                                                                                              |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98e21-116">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="98e21-116">**Reset**</span></span>         | <span data-ttu-id="98e21-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="98e21-117">Not implemented.</span></span> <span data-ttu-id="98e21-118">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span><br/>                 |
| <span data-ttu-id="98e21-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="98e21-119">**SetPowerState**</span></span> | <span data-ttu-id="98e21-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="98e21-120">Not implemented.</span></span> <span data-ttu-id="98e21-121">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="98e21-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="98e21-122">Properties</span></span>

<span data-ttu-id="98e21-123">La classe **Win32 \_ ParallelPort** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="98e21-123">The **Win32\_ParallelPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98e21-124">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="98e21-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98e21-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-127">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="98e21-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-128">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98e21-128">Availability and status of the device.</span></span>

<span data-ttu-id="98e21-129">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="98e21-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="98e21-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="98e21-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="98e21-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="98e21-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="98e21-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-133">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="98e21-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="98e21-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="98e21-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="98e21-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="98e21-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="98e21-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="98e21-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="98e21-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="98e21-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="98e21-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="98e21-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="98e21-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="98e21-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="98e21-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="98e21-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="98e21-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="98e21-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="98e21-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="98e21-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="98e21-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="98e21-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-144">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="98e21-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="98e21-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="98e21-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-146">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="98e21-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="98e21-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="98e21-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-148">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="98e21-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="98e21-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="98e21-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="98e21-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="98e21-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-151">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="98e21-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="98e21-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="98e21-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-153">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="98e21-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="98e21-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="98e21-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-155">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="98e21-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="98e21-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="98e21-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-157">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="98e21-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="98e21-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="98e21-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-159">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="98e21-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="98e21-160">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="98e21-160">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-161">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98e21-161">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="98e21-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-163">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Parallel ports \| 003,8 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ParallelController**](cim-parallelcontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="98e21-163">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Parallel Ports\|003.8"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ParallelController**](cim-parallelcontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-164">Matrice delle funzionalità del controller parallelo.</span><span class="sxs-lookup"><span data-stu-id="98e21-164">Array of the capabilities of the parallel controller.</span></span>

<span data-ttu-id="98e21-165">Questa proprietà viene ereditata da [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-165">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="98e21-166">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="98e21-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="98e21-167">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="98e21-167">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="98e21-168">**XT/AT Compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="98e21-168">**XT/AT Compatible** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2_Compatible"></span><span id="ps_2_compatible"></span><span id="PS_2_COMPATIBLE"></span>

<span data-ttu-id="98e21-169">**Compatibile con PS/2** (3)</span><span class="sxs-lookup"><span data-stu-id="98e21-169">**PS/2 Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ECP"></span><span id="ecp"></span>

<span data-ttu-id="98e21-170">**ECP** (4)</span><span class="sxs-lookup"><span data-stu-id="98e21-170">**ECP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EPP"></span><span id="epp"></span>

<span data-ttu-id="98e21-171">**EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="98e21-171">**EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="98e21-172">**PC-98** (6)</span><span class="sxs-lookup"><span data-stu-id="98e21-172">**PC-98** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="98e21-173">**PC-98-Hireso** (7)</span><span class="sxs-lookup"><span data-stu-id="98e21-173">**PC-98-Hireso** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="98e21-174">**PC-H98** (8)</span><span class="sxs-lookup"><span data-stu-id="98e21-174">**PC-H98** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="98e21-175">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="98e21-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-176">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="98e21-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="98e21-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-178">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ParallelController**](cim-parallelcontroller.md).**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="98e21-178">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ParallelController**](cim-parallelcontroller.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-179">Matrice di spiegazioni più dettagliate per tutte le funzionalità del controller parallelo indicate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="98e21-179">Array of more detailed explanations for any of the parallel controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="98e21-180">Ogni voce di questa matrice è correlata alla voce nella matrice delle **funzionalità** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="98e21-180">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="98e21-181">Questa proprietà viene ereditata da [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-181">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-182">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="98e21-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="98e21-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-185">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="98e21-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-186">Breve descrizione dell'oggetto, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="98e21-186">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="98e21-187">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-188">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="98e21-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-189">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98e21-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-191">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="98e21-191">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-192">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="98e21-192">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="98e21-193">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="98e21-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="98e21-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="98e21-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="98e21-195">(0)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-196">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="98e21-196">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="98e21-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="98e21-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="98e21-198">(1)</span><span class="sxs-lookup"><span data-stu-id="98e21-198">(1)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-199">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="98e21-199">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="98e21-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="98e21-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="98e21-201">(2)</span><span class="sxs-lookup"><span data-stu-id="98e21-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="98e21-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="98e21-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="98e21-203">(3)</span><span class="sxs-lookup"><span data-stu-id="98e21-203">(3)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-204">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="98e21-204">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="98e21-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="98e21-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="98e21-206">(4)</span><span class="sxs-lookup"><span data-stu-id="98e21-206">(4)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-207">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="98e21-207">Device is not working properly.</span></span> <span data-ttu-id="98e21-208">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="98e21-208">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="98e21-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="98e21-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="98e21-210">(5)</span><span class="sxs-lookup"><span data-stu-id="98e21-210">(5)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-211">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="98e21-211">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="98e21-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="98e21-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="98e21-213"> (6)</span><span class="sxs-lookup"><span data-stu-id="98e21-213">(6)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-214">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="98e21-214">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="98e21-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="98e21-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="98e21-216">(7)</span><span class="sxs-lookup"><span data-stu-id="98e21-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="98e21-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="98e21-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="98e21-218">(8)</span><span class="sxs-lookup"><span data-stu-id="98e21-218">(8)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-219">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="98e21-219">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="98e21-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="98e21-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="98e21-221">(9)</span><span class="sxs-lookup"><span data-stu-id="98e21-221">(9)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-222">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="98e21-222">Device is not working properly.</span></span> <span data-ttu-id="98e21-223">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98e21-223">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="98e21-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="98e21-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="98e21-225">(10)</span><span class="sxs-lookup"><span data-stu-id="98e21-225">(10)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-226">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98e21-226">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="98e21-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="98e21-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="98e21-228">(11)</span><span class="sxs-lookup"><span data-stu-id="98e21-228">(11)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-229">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98e21-229">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="98e21-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="98e21-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="98e21-231">12</span><span class="sxs-lookup"><span data-stu-id="98e21-231">(12)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-232">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="98e21-232">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="98e21-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="98e21-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="98e21-234">(13)</span><span class="sxs-lookup"><span data-stu-id="98e21-234">(13)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-235">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98e21-235">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="98e21-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="98e21-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="98e21-237">(14)</span><span class="sxs-lookup"><span data-stu-id="98e21-237">(14)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-238">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="98e21-238">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="98e21-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="98e21-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="98e21-240">(15)</span><span class="sxs-lookup"><span data-stu-id="98e21-240">(15)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-241">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="98e21-241">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="98e21-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="98e21-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="98e21-243">(16)</span><span class="sxs-lookup"><span data-stu-id="98e21-243">(16)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-244">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98e21-244">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="98e21-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="98e21-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="98e21-246">(17)</span><span class="sxs-lookup"><span data-stu-id="98e21-246">(17)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-247">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="98e21-247">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="98e21-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="98e21-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="98e21-249">(18)</span><span class="sxs-lookup"><span data-stu-id="98e21-249">(18)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-250">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98e21-250">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="98e21-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="98e21-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="98e21-252">(19)</span><span class="sxs-lookup"><span data-stu-id="98e21-252">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="98e21-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="98e21-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="98e21-254">(20)</span><span class="sxs-lookup"><span data-stu-id="98e21-254">(20)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-255">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="98e21-255">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="98e21-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="98e21-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="98e21-257">(21)</span><span class="sxs-lookup"><span data-stu-id="98e21-257">(21)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-258">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="98e21-258">System failure.</span></span> <span data-ttu-id="98e21-259">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="98e21-259">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="98e21-260">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98e21-260">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="98e21-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="98e21-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="98e21-262">(22)</span><span class="sxs-lookup"><span data-stu-id="98e21-262">(22)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-263">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="98e21-263">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="98e21-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="98e21-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="98e21-265">(23)</span><span class="sxs-lookup"><span data-stu-id="98e21-265">(23)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-266">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="98e21-266">System failure.</span></span> <span data-ttu-id="98e21-267">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="98e21-267">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="98e21-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="98e21-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="98e21-269">(24)</span><span class="sxs-lookup"><span data-stu-id="98e21-269">(24)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-270">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="98e21-270">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="98e21-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="98e21-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="98e21-272">(25)</span><span class="sxs-lookup"><span data-stu-id="98e21-272">(25)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-273">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98e21-273">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="98e21-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="98e21-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="98e21-275">(26)</span><span class="sxs-lookup"><span data-stu-id="98e21-275">(26)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-276">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98e21-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="98e21-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="98e21-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="98e21-278">(27)</span><span class="sxs-lookup"><span data-stu-id="98e21-278">(27)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-279">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="98e21-279">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="98e21-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="98e21-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="98e21-281">(28)</span><span class="sxs-lookup"><span data-stu-id="98e21-281">(28)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-282">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="98e21-282">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="98e21-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="98e21-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="98e21-284">(29)</span><span class="sxs-lookup"><span data-stu-id="98e21-284">(29)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-285">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="98e21-285">Device is disabled.</span></span> <span data-ttu-id="98e21-286">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="98e21-286">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="98e21-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="98e21-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="98e21-288">(30)</span><span class="sxs-lookup"><span data-stu-id="98e21-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-289">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98e21-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="98e21-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="98e21-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="98e21-291">31</span><span class="sxs-lookup"><span data-stu-id="98e21-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-292">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="98e21-292">Device is not working properly.</span></span> <span data-ttu-id="98e21-293">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="98e21-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="98e21-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="98e21-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-295">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="98e21-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-297">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="98e21-297">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-298">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="98e21-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="98e21-299">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="98e21-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-301">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="98e21-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-303">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="98e21-303">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="98e21-304">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="98e21-304">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="98e21-305">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="98e21-305">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="98e21-306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-307">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="98e21-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-308">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="98e21-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-310">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="98e21-310">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-311">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="98e21-311">Description of the object.</span></span>

<span data-ttu-id="98e21-312">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="98e21-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-314">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="98e21-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-316">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="98e21-316">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-317">Identificatore della porta parallela.</span><span class="sxs-lookup"><span data-stu-id="98e21-317">Identifier of the parallel port.</span></span>

<span data-ttu-id="98e21-318">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-319">**DMASupport**</span><span class="sxs-lookup"><span data-stu-id="98e21-319">**DMASupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-320">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="98e21-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-322">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| porte parallele \| 003,7 ")</span><span class="sxs-lookup"><span data-stu-id="98e21-322">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Parallel Ports\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-323">Se **true**, la porta parallela supporta DMA.</span><span class="sxs-lookup"><span data-stu-id="98e21-323">If **TRUE**, the parallel port supports DMA.</span></span>

<span data-ttu-id="98e21-324">Questa proprietà viene ereditata da [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-324">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-325">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="98e21-325">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-326">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="98e21-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98e21-328">Se **true**, l'errore riportato in **LastErrorCode** è deselezionato.</span><span class="sxs-lookup"><span data-stu-id="98e21-328">If **TRUE**, the error reported in **LastErrorCode** is cleared.</span></span>

<span data-ttu-id="98e21-329">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-330">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="98e21-330">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-331">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="98e21-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98e21-333">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="98e21-333">More information about the error recorded in **LastErrorCode**, and information about corrective actions that might be taken.</span></span>

<span data-ttu-id="98e21-334">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="98e21-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-336">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="98e21-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-338">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="98e21-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-339">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="98e21-339">Date and time the object was installed.</span></span> <span data-ttu-id="98e21-340">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="98e21-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="98e21-341">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-342">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="98e21-342">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-343">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98e21-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98e21-345">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="98e21-345">Last error code reported by the logical device.</span></span>

<span data-ttu-id="98e21-346">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-347">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="98e21-347">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-348">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98e21-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-350">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="98e21-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-351">Numero massimo di entità indirizzabili direttamente supportato da questo controller.</span><span class="sxs-lookup"><span data-stu-id="98e21-351">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="98e21-352">Se il numero è sconosciuto, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="98e21-352">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="98e21-353">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-353">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-354">**Nome**</span><span class="sxs-lookup"><span data-stu-id="98e21-354">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-355">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="98e21-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-357">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="98e21-357">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-358">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="98e21-358">Label by which the object is known.</span></span> <span data-ttu-id="98e21-359">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="98e21-359">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="98e21-360">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-360">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-361">**OSAutoDiscovered**</span><span class="sxs-lookup"><span data-stu-id="98e21-361">**OSAutoDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-362">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="98e21-362">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-364">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="98e21-364">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-365">Se **true**, la porta parallela è stata rilevata automaticamente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="98e21-365">If **TRUE**, the parallel port was automatically detected by the operating system.</span></span> <span data-ttu-id="98e21-366">Se **false**, la porta è stata rilevata da altri mezzi, ad esempio aggiunti manualmente tramite il pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="98e21-366">If **FALSE**, the port was detected by other means (such as being manually added through the Control Panel).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-367">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="98e21-367">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-368">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="98e21-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-370">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="98e21-370">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-371">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="98e21-371">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="98e21-372">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="98e21-373">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="98e21-373">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="98e21-374">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="98e21-374">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-375">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98e21-375">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="98e21-376">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98e21-377">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="98e21-377">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="98e21-378">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="98e21-378">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="98e21-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="98e21-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="98e21-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="98e21-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="98e21-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="98e21-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="98e21-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="98e21-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-383">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="98e21-383">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="98e21-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="98e21-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-385">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="98e21-385">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="98e21-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="98e21-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-387">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="98e21-387">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="98e21-388">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="98e21-388">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="98e21-389">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-389">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="98e21-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="98e21-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-391">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="98e21-391">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="98e21-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="98e21-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="98e21-393">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="98e21-393">Timed Power-On Supported</span></span>

<span data-ttu-id="98e21-394">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="98e21-394">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="98e21-395">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="98e21-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-396">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="98e21-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98e21-398">Se **true**, il dispositivo può essere gestito dal risparmio energia, il che significa che può essere messo in modalità di sospensione e così via.</span><span class="sxs-lookup"><span data-stu-id="98e21-398">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="98e21-399">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="98e21-399">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="98e21-400">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-401">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="98e21-401">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-402">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98e21-402">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-403">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-404">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta bus DMTF \| 001,2 "," MIF. \|Dischi DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="98e21-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-405">Protocollo usato dal controller per accedere ai dispositivi "controllati".</span><span class="sxs-lookup"><span data-stu-id="98e21-405">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="98e21-406">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-406">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="98e21-407">I valori sono indicati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="98e21-407">Values are shown in the following list.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="98e21-408">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="98e21-408">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="98e21-409">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="98e21-409">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="98e21-410">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="98e21-410">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="98e21-411">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="98e21-411">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="98e21-412">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="98e21-412">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="98e21-413">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="98e21-413">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="98e21-414">**Dischetto flessibile** (7)</span><span class="sxs-lookup"><span data-stu-id="98e21-414">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="98e21-415">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="98e21-415">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="98e21-416">**Interfaccia parallela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="98e21-416">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="98e21-417">**Protocollo di Fibre Channel SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="98e21-417">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="98e21-418">**Protocollo bus seriale SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="98e21-418">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="98e21-419">**Protocollo bus seriale SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="98e21-419">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="98e21-420">**Architettura di archiviazione seriale SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="98e21-420">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="98e21-421">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="98e21-421">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="98e21-422">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="98e21-422">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="98e21-423">**Bus seriale universale** (16)</span><span class="sxs-lookup"><span data-stu-id="98e21-423">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="98e21-424">**Protocollo parallelo** (17)</span><span class="sxs-lookup"><span data-stu-id="98e21-424">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="98e21-425">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="98e21-425">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="98e21-426">**Diagnostica** (19)</span><span class="sxs-lookup"><span data-stu-id="98e21-426">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="98e21-427">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="98e21-427">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="98e21-428">**Potenza** (21)</span><span class="sxs-lookup"><span data-stu-id="98e21-428">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="98e21-429">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="98e21-429">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="98e21-430">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="98e21-430">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="98e21-431">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="98e21-431">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="98e21-432">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="98e21-432">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="98e21-433">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="98e21-433">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="98e21-434">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="98e21-434">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="98e21-435">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="98e21-435">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="98e21-436">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="98e21-436">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="98e21-437">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="98e21-437">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="98e21-438">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="98e21-438">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="98e21-439">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="98e21-439">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="98e21-440">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="98e21-440">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="98e21-441">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="98e21-441">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="98e21-442">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="98e21-442">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="98e21-443">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="98e21-443">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="98e21-444">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="98e21-444">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="98e21-445">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="98e21-445">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="98e21-446">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="98e21-446">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="98e21-447">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="98e21-447">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="98e21-448">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="98e21-448">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="98e21-449">**ATA/IDE avanzato** (42)</span><span class="sxs-lookup"><span data-stu-id="98e21-449">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="98e21-450">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="98e21-450">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="98e21-451">**TWIRP (infrarossi bidirezionali)** (44)</span><span class="sxs-lookup"><span data-stu-id="98e21-451">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="98e21-452">**FIR (infrarossi veloci)** (45)</span><span class="sxs-lookup"><span data-stu-id="98e21-452">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="98e21-453">**Sir (Serial Infrared)** (46)</span><span class="sxs-lookup"><span data-stu-id="98e21-453">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="98e21-454">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="98e21-454">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="98e21-455">**Status**</span><span class="sxs-lookup"><span data-stu-id="98e21-455">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-456">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="98e21-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-457">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-458">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="98e21-458">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-459">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="98e21-459">Current status of the object.</span></span> <span data-ttu-id="98e21-460">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="98e21-460">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="98e21-461">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="98e21-461">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="98e21-462">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="98e21-462">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="98e21-463">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="98e21-463">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="98e21-464">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="98e21-464">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="98e21-465">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="98e21-466">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="98e21-466">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="98e21-467">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="98e21-467">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="98e21-468">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="98e21-468">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="98e21-469">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="98e21-469">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="98e21-470">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="98e21-470">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="98e21-471">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="98e21-471">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="98e21-472">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="98e21-472">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="98e21-473">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="98e21-473">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="98e21-474">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="98e21-474">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="98e21-475">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="98e21-475">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="98e21-476">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="98e21-476">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="98e21-477">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="98e21-477">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="98e21-478">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="98e21-478">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="98e21-479">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="98e21-479">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-480">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98e21-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-481">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-482">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="98e21-482">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="98e21-483">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="98e21-483">State of the logical device.</span></span> <span data-ttu-id="98e21-484">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="98e21-484">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="98e21-485">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="98e21-486">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="98e21-486">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="98e21-487">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="98e21-487">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="98e21-488">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="98e21-488">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="98e21-489">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="98e21-489">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="98e21-490">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="98e21-490">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="98e21-491">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="98e21-491">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-492">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="98e21-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-493">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-494">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="98e21-494">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="98e21-495">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="98e21-495">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="98e21-496">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-496">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-497">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="98e21-497">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-498">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="98e21-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-499">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e21-500">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="98e21-500">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="98e21-501">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="98e21-501">Name of the scoping system.</span></span>

<span data-ttu-id="98e21-502">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-502">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e21-503">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="98e21-503">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e21-504">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="98e21-504">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="98e21-505">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="98e21-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98e21-506">Data e ora dell'ultima reimpostazione del controller.</span><span class="sxs-lookup"><span data-stu-id="98e21-506">Date and time the controller was last reset.</span></span> <span data-ttu-id="98e21-507">Questo potrebbe significare che il controller è stato spento o reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="98e21-507">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="98e21-508">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-508">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98e21-509">Commenti</span><span class="sxs-lookup"><span data-stu-id="98e21-509">Remarks</span></span>

<span data-ttu-id="98e21-510">La classe **Win32 \_ ParallelPort** è derivata da [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="98e21-510">The **Win32\_ParallelPort** class is derived from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98e21-511">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98e21-511">Requirements</span></span>



| <span data-ttu-id="98e21-512">Requisito</span><span class="sxs-lookup"><span data-stu-id="98e21-512">Requirement</span></span> | <span data-ttu-id="98e21-513">Valore</span><span class="sxs-lookup"><span data-stu-id="98e21-513">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98e21-514">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98e21-514">Minimum supported client</span></span><br/> | <span data-ttu-id="98e21-515">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98e21-515">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="98e21-516">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98e21-516">Minimum supported server</span></span><br/> | <span data-ttu-id="98e21-517">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98e21-517">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="98e21-518">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="98e21-518">Namespace</span></span><br/>                | <span data-ttu-id="98e21-519">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="98e21-519">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="98e21-520">MOF</span><span class="sxs-lookup"><span data-stu-id="98e21-520">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98e21-521"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98e21-521"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="98e21-522">DLL</span><span class="sxs-lookup"><span data-stu-id="98e21-522">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98e21-523"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98e21-523"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e21-524">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98e21-524">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e21-525">**\_PARALLELCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="98e21-525">**CIM\_ParallelController**</span></span>](cim-parallelcontroller.md)
</dt> <dt>

[<span data-ttu-id="98e21-526">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="98e21-526">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
