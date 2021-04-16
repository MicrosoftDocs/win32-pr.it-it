---
description: L' \_ associazione CIM ParallelController è correlata alle funzionalità e alla gestione del dispositivo logico della porta parallela.
ms.assetid: c05e79b6-f3a6-48cc-a831-b67e216f43eb
ms.tgt_platform: multiple
title: Classe CIM_ParallelController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParallelController
- CIM_ParallelController.Availability
- CIM_ParallelController.Capabilities
- CIM_ParallelController.CapabilityDescriptions
- CIM_ParallelController.Caption
- CIM_ParallelController.ConfigManagerErrorCode
- CIM_ParallelController.ConfigManagerUserConfig
- CIM_ParallelController.CreationClassName
- CIM_ParallelController.Description
- CIM_ParallelController.DeviceID
- CIM_ParallelController.DMASupport
- CIM_ParallelController.ErrorCleared
- CIM_ParallelController.ErrorDescription
- CIM_ParallelController.InstallDate
- CIM_ParallelController.LastErrorCode
- CIM_ParallelController.MaxNumberControlled
- CIM_ParallelController.Name
- CIM_ParallelController.PNPDeviceID
- CIM_ParallelController.PowerManagementCapabilities
- CIM_ParallelController.PowerManagementSupported
- CIM_ParallelController.ProtocolSupported
- CIM_ParallelController.Status
- CIM_ParallelController.StatusInfo
- CIM_ParallelController.SystemCreationClassName
- CIM_ParallelController.SystemName
- CIM_ParallelController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc21290de08b6e22c0bc69ec127f3c996ee5b65e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524025"
---
# <a name="cim_parallelcontroller-class"></a><span data-ttu-id="d6d80-103">CIM \_ ParallelController (classe)</span><span class="sxs-lookup"><span data-stu-id="d6d80-103">CIM\_ParallelController class</span></span>

<span data-ttu-id="d6d80-104">L'associazione **CIM \_ ParallelController** è correlata alle funzionalità e alla gestione del dispositivo logico della porta parallela.</span><span class="sxs-lookup"><span data-stu-id="d6d80-104">The **CIM\_ParallelController** association relates to the capabilities and management of the parallel port logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6d80-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="d6d80-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d6d80-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d6d80-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d6d80-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d6d80-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d6d80-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d6d80-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d80-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6d80-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C552-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ParallelController : CIM_Controller
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

## <a name="members"></a><span data-ttu-id="d6d80-110">Members</span><span class="sxs-lookup"><span data-stu-id="d6d80-110">Members</span></span>

<span data-ttu-id="d6d80-111">La classe **CIM \_ ParallelController** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d6d80-111">The **CIM\_ParallelController** class has these types of members:</span></span>

-   [<span data-ttu-id="d6d80-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="d6d80-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d6d80-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d6d80-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d6d80-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="d6d80-114">Methods</span></span>

<span data-ttu-id="d6d80-115">La classe **CIM \_ ParallelController** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d6d80-115">The **CIM\_ParallelController** class has these methods.</span></span>



| <span data-ttu-id="d6d80-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="d6d80-116">Method</span></span>                                                                        | <span data-ttu-id="d6d80-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6d80-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6d80-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="d6d80-118">**Reset**</span></span>](reset-method-in-class-cim-parallelcontroller.md)                 | <span data-ttu-id="d6d80-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d6d80-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="d6d80-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="d6d80-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="d6d80-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d6d80-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-parallelcontroller.md) | <span data-ttu-id="d6d80-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="d6d80-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="d6d80-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="d6d80-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d6d80-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d6d80-124">Properties</span></span>

<span data-ttu-id="d6d80-125">La classe **CIM \_ ParallelController** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d6d80-125">The **CIM\_ParallelController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6d80-126">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="d6d80-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d6d80-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-129">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="d6d80-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-130">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6d80-130">Availability and status of the device.</span></span>

<span data-ttu-id="d6d80-131">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d6d80-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d6d80-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d6d80-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="d6d80-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d6d80-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="d6d80-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d6d80-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="d6d80-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d6d80-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="d6d80-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d6d80-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="d6d80-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d6d80-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="d6d80-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d6d80-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="d6d80-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d6d80-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="d6d80-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d6d80-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="d6d80-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d6d80-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="d6d80-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d6d80-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="d6d80-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d6d80-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="d6d80-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-145">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="d6d80-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d6d80-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="d6d80-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-147">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="d6d80-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d6d80-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="d6d80-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-149">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="d6d80-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d6d80-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="d6d80-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d6d80-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="d6d80-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-152">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="d6d80-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d6d80-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="d6d80-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-154">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="d6d80-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d6d80-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="d6d80-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-156">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="d6d80-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d6d80-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="d6d80-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-158">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="d6d80-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d6d80-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="d6d80-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-160">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="d6d80-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d6d80-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d6d80-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-162">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d6d80-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-164">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Parallel ports \| 003,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ParallelController**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="d6d80-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Parallel Ports\|003.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ParallelController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-165">Funzionalità del controller parallelo.</span><span class="sxs-lookup"><span data-stu-id="d6d80-165">Capabilities of the parallel controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d6d80-166">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d6d80-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d6d80-167">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d6d80-167">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="d6d80-168">**XT/AT Compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="d6d80-168">**XT/AT Compatible** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2_Compatible"></span><span id="ps_2_compatible"></span><span id="PS_2_COMPATIBLE"></span>

<span data-ttu-id="d6d80-169">**Compatibile con PS/2** (3)</span><span class="sxs-lookup"><span data-stu-id="d6d80-169">**PS/2 Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ECP"></span><span id="ecp"></span>

<span data-ttu-id="d6d80-170">**ECP** (4)</span><span class="sxs-lookup"><span data-stu-id="d6d80-170">**ECP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EPP"></span><span id="epp"></span>

<span data-ttu-id="d6d80-171">**EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="d6d80-171">**EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="d6d80-172">**PC-98** (6)</span><span class="sxs-lookup"><span data-stu-id="d6d80-172">**PC-98** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="d6d80-173">**PC-98-Hireso** (7)</span><span class="sxs-lookup"><span data-stu-id="d6d80-173">**PC-98-Hireso** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="d6d80-174">**PC-H98** (8)</span><span class="sxs-lookup"><span data-stu-id="d6d80-174">**PC-H98** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d6d80-175">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d6d80-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-176">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="d6d80-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-178">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ParallelController**.**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="d6d80-178">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ParallelController**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-179">Stringhe in formato libero che forniscono spiegazioni dettagliate per le funzionalità del controller parallelo indicate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="d6d80-179">Free-form strings that provide detailed explanations for the parallel controller features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="d6d80-180">Ogni voce di questa matrice è correlata alla voce nella matrice di **funzionalità** , che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="d6d80-180">Each entry of this array is related to the entry in the **Capabilities** array, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="d6d80-181">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="d6d80-181">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6d80-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-184">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d6d80-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-185">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6d80-185">Short textual description of the object.</span></span>

<span data-ttu-id="d6d80-186">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-187">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d6d80-187">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-188">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6d80-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-190">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d6d80-190">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-191">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d6d80-191">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="d6d80-192">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-192">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d6d80-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="d6d80-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="d6d80-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-195">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="d6d80-195">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d6d80-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="d6d80-197">(1)</span><span class="sxs-lookup"><span data-stu-id="d6d80-197">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-198">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="d6d80-198">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d6d80-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d6d80-200">(2)</span><span class="sxs-lookup"><span data-stu-id="d6d80-200">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d6d80-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d6d80-202">(3)</span><span class="sxs-lookup"><span data-stu-id="d6d80-202">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-203">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="d6d80-203">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d6d80-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d6d80-205">(4)</span><span class="sxs-lookup"><span data-stu-id="d6d80-205">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-206">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="d6d80-206">Device is not working properly.</span></span> <span data-ttu-id="d6d80-207">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="d6d80-207">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d6d80-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d6d80-209">(5)</span><span class="sxs-lookup"><span data-stu-id="d6d80-209">(5)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-210">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="d6d80-210">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d6d80-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d6d80-212"> (6)</span><span class="sxs-lookup"><span data-stu-id="d6d80-212">(6)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-213">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="d6d80-213">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d6d80-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="d6d80-215">(7)</span><span class="sxs-lookup"><span data-stu-id="d6d80-215">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d6d80-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d6d80-217">(8)</span><span class="sxs-lookup"><span data-stu-id="d6d80-217">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-218">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="d6d80-218">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d6d80-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d6d80-220">(9)</span><span class="sxs-lookup"><span data-stu-id="d6d80-220">(9)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-221">Il dispositivo non funziona correttamente; il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6d80-221">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d6d80-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="d6d80-223">(10)</span><span class="sxs-lookup"><span data-stu-id="d6d80-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-224">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6d80-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d6d80-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="d6d80-226">(11)</span><span class="sxs-lookup"><span data-stu-id="d6d80-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-227">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6d80-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d6d80-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d6d80-229">12</span><span class="sxs-lookup"><span data-stu-id="d6d80-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-230">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="d6d80-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d6d80-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d6d80-232">(13)</span><span class="sxs-lookup"><span data-stu-id="d6d80-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-233">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6d80-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d6d80-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d6d80-235">(14)</span><span class="sxs-lookup"><span data-stu-id="d6d80-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-236">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="d6d80-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d6d80-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d6d80-238">(15)</span><span class="sxs-lookup"><span data-stu-id="d6d80-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-239">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="d6d80-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d6d80-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d6d80-241">(16)</span><span class="sxs-lookup"><span data-stu-id="d6d80-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-242">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6d80-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d6d80-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d6d80-244">(17)</span><span class="sxs-lookup"><span data-stu-id="d6d80-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-245">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="d6d80-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d6d80-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d6d80-247">(18)</span><span class="sxs-lookup"><span data-stu-id="d6d80-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-248">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6d80-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d6d80-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="d6d80-250">(19)</span><span class="sxs-lookup"><span data-stu-id="d6d80-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d6d80-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="d6d80-252">(20)</span><span class="sxs-lookup"><span data-stu-id="d6d80-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-253">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="d6d80-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d6d80-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d6d80-255">(21)</span><span class="sxs-lookup"><span data-stu-id="d6d80-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-256">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="d6d80-256">System failure.</span></span> <span data-ttu-id="d6d80-257">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="d6d80-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="d6d80-258">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6d80-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d6d80-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="d6d80-260">(22)</span><span class="sxs-lookup"><span data-stu-id="d6d80-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-261">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="d6d80-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d6d80-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d6d80-263">(23)</span><span class="sxs-lookup"><span data-stu-id="d6d80-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-264">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="d6d80-264">System failure.</span></span> <span data-ttu-id="d6d80-265">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="d6d80-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d6d80-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d6d80-267">(24)</span><span class="sxs-lookup"><span data-stu-id="d6d80-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-268">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="d6d80-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d6d80-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d6d80-270">(25)</span><span class="sxs-lookup"><span data-stu-id="d6d80-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-271">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6d80-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d6d80-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d6d80-273">(26)</span><span class="sxs-lookup"><span data-stu-id="d6d80-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-274">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6d80-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d6d80-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d6d80-276">(27)</span><span class="sxs-lookup"><span data-stu-id="d6d80-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-277">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="d6d80-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d6d80-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d6d80-279">(28)</span><span class="sxs-lookup"><span data-stu-id="d6d80-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-280">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="d6d80-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d6d80-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d6d80-282">(29)</span><span class="sxs-lookup"><span data-stu-id="d6d80-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-283">Il dispositivo è disabilitato; il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="d6d80-283">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d6d80-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d6d80-285">(30)</span><span class="sxs-lookup"><span data-stu-id="d6d80-285">(30)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-286">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6d80-286">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d6d80-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d6d80-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d6d80-288">31</span><span class="sxs-lookup"><span data-stu-id="d6d80-288">(31)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-289">Il dispositivo non funziona correttamente; Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="d6d80-289">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d6d80-290">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d6d80-290">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-291">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d6d80-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-293">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d6d80-293">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-294">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d6d80-294">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d6d80-295">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-296">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d6d80-296">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-297">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6d80-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-299">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d6d80-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-300">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="d6d80-300">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d6d80-301">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="d6d80-301">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d6d80-302">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-303">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d6d80-303">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-304">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6d80-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-306">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d6d80-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-307">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6d80-307">Textual description of the object.</span></span>

<span data-ttu-id="d6d80-308">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-309">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d6d80-309">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-310">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6d80-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-312">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d6d80-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-313">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d6d80-313">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="d6d80-314">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-315">**DMASupport**</span><span class="sxs-lookup"><span data-stu-id="d6d80-315">**DMASupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-316">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d6d80-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-318">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| porte parallele \| 003,7 ")</span><span class="sxs-lookup"><span data-stu-id="d6d80-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Parallel Ports\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-319">Se **true**, è supportato l'accesso diretto alla memoria (DMA).</span><span class="sxs-lookup"><span data-stu-id="d6d80-319">If **TRUE**, direct memory access (DMA) is supported.</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d6d80-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-321">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d6d80-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-323">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="d6d80-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="d6d80-324">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d6d80-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-326">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6d80-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-328">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="d6d80-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="d6d80-329">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-330">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d6d80-330">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-331">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d6d80-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-333">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="d6d80-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-334">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6d80-334">Date and time the object was installed.</span></span> <span data-ttu-id="d6d80-335">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="d6d80-335">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d6d80-336">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-336">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-337">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d6d80-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-338">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6d80-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-340">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d6d80-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d6d80-341">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-342">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="d6d80-342">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-343">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6d80-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-345">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="d6d80-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-346">Numero massimo di entità indirizzabili direttamente supportate dal controller.</span><span class="sxs-lookup"><span data-stu-id="d6d80-346">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="d6d80-347">Se il numero è sconosciuto o illimitato, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="d6d80-347">A value of 0 (zero) should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="d6d80-348">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-348">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-349">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d6d80-349">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-350">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6d80-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-352">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d6d80-352">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-353">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="d6d80-353">Label by which the object is known.</span></span> <span data-ttu-id="d6d80-354">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="d6d80-354">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d6d80-355">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-355">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-356">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d6d80-356">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-357">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6d80-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-359">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d6d80-359">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-360">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d6d80-360">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="d6d80-361">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-361">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d6d80-362">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="d6d80-362">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-363">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d6d80-363">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-364">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d6d80-364">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-366">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d6d80-366">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d6d80-367">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="d6d80-367">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d6d80-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d6d80-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d6d80-369"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="d6d80-369"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d6d80-370"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="d6d80-370"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d6d80-371"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="d6d80-371"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-372">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="d6d80-372">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d6d80-373"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="d6d80-373"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-374">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="d6d80-374">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d6d80-375"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="d6d80-375"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-376">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="d6d80-376">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d6d80-377">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="d6d80-377">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="d6d80-378">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="d6d80-378">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d6d80-379"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="d6d80-379"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-380">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="d6d80-380">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d6d80-381"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="d6d80-381"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d6d80-382">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="d6d80-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d6d80-383">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d6d80-383">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-384">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d6d80-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-385">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-386">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="d6d80-386">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="d6d80-387">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="d6d80-387">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="d6d80-388">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="d6d80-388">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="d6d80-389">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="d6d80-389">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="d6d80-390">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-391">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="d6d80-391">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-392">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d6d80-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-394">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,2 "," MIF. \|Dischi DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d6d80-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-395">Protocollo usato dal controller per accedere ai dispositivi "controllati".</span><span class="sxs-lookup"><span data-stu-id="d6d80-395">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="d6d80-396">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-396">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="d6d80-397">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="d6d80-397">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d6d80-398">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d6d80-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d6d80-399">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="d6d80-399">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="d6d80-400">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="d6d80-400">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="d6d80-401">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="d6d80-401">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="d6d80-402">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="d6d80-402">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="d6d80-403">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="d6d80-403">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="d6d80-404">**Dischetto flessibile** (7)</span><span class="sxs-lookup"><span data-stu-id="d6d80-404">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="d6d80-405">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="d6d80-405">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="d6d80-406">**Interfaccia parallela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="d6d80-406">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="d6d80-407">**Protocollo di Fibre Channel SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="d6d80-407">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="d6d80-408">**Protocollo bus seriale SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="d6d80-408">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="d6d80-409">**Protocollo bus seriale SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="d6d80-409">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="d6d80-410">**Architettura di archiviazione seriale SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="d6d80-410">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="d6d80-411">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="d6d80-411">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="d6d80-412">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="d6d80-412">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="d6d80-413">**Bus seriale universale** (16)</span><span class="sxs-lookup"><span data-stu-id="d6d80-413">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="d6d80-414">**Protocollo parallelo** (17)</span><span class="sxs-lookup"><span data-stu-id="d6d80-414">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="d6d80-415">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="d6d80-415">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="d6d80-416">**Diagnostica** (19)</span><span class="sxs-lookup"><span data-stu-id="d6d80-416">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="d6d80-417">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="d6d80-417">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="d6d80-418">**Potenza** (21)</span><span class="sxs-lookup"><span data-stu-id="d6d80-418">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="d6d80-419">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="d6d80-419">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="d6d80-420">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="d6d80-420">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="d6d80-421">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="d6d80-421">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="d6d80-422">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="d6d80-422">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="d6d80-423">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="d6d80-423">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="d6d80-424">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="d6d80-424">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="d6d80-425">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="d6d80-425">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="d6d80-426">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="d6d80-426">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="d6d80-427">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="d6d80-427">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="d6d80-428">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="d6d80-428">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="d6d80-429">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="d6d80-429">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="d6d80-430">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="d6d80-430">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="d6d80-431">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="d6d80-431">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="d6d80-432">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="d6d80-432">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="d6d80-433">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="d6d80-433">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="d6d80-434">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="d6d80-434">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="d6d80-435">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="d6d80-435">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="d6d80-436">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="d6d80-436">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="d6d80-437">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="d6d80-437">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="d6d80-438">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="d6d80-438">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="d6d80-439">**ATA/IDE avanzato** (42)</span><span class="sxs-lookup"><span data-stu-id="d6d80-439">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="d6d80-440">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="d6d80-440">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="d6d80-441">**TWIRP (infrarossi bidirezionali)** (44)</span><span class="sxs-lookup"><span data-stu-id="d6d80-441">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="d6d80-442">**FIR (infrarossi veloci)** (45)</span><span class="sxs-lookup"><span data-stu-id="d6d80-442">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="d6d80-443">**Sir (Serial Infrared)** (46)</span><span class="sxs-lookup"><span data-stu-id="d6d80-443">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="d6d80-444">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="d6d80-444">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d6d80-445">**Status**</span><span class="sxs-lookup"><span data-stu-id="d6d80-445">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-446">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6d80-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-447">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-448">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="d6d80-448">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-449">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6d80-449">Current status of the object.</span></span> <span data-ttu-id="d6d80-450">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-450">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d6d80-451">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="d6d80-451">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d6d80-452">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="d6d80-452">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d6d80-453">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="d6d80-453">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d6d80-454">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="d6d80-454">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d6d80-455">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="d6d80-455">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d6d80-456">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="d6d80-456">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d6d80-457">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="d6d80-457">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d6d80-458">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="d6d80-458">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d6d80-459">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="d6d80-459">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d6d80-460">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="d6d80-460">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d6d80-461">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="d6d80-461">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d6d80-462">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="d6d80-462">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d6d80-463">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="d6d80-463">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d6d80-464">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d6d80-464">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-465">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d6d80-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-466">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-467">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d6d80-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-468">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d6d80-468">State of the logical device.</span></span> <span data-ttu-id="d6d80-469">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="d6d80-469">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="d6d80-470">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d6d80-471">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d6d80-471">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d6d80-472">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="d6d80-472">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d6d80-473">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="d6d80-473">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d6d80-474">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="d6d80-474">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d6d80-475">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="d6d80-475">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d6d80-476">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d6d80-476">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-477">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6d80-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-478">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-479">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d6d80-479">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-480">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="d6d80-480">Scoping system's creation class name.</span></span>

<span data-ttu-id="d6d80-481">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-481">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-482">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d6d80-482">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-483">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6d80-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-484">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-485">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d6d80-485">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-486">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="d6d80-486">Scoping system's name.</span></span>

<span data-ttu-id="d6d80-487">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6d80-488">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="d6d80-488">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6d80-489">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d6d80-489">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d6d80-490">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6d80-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6d80-491">Data e ora dell'ultima reimpostazione del controller, ovvero il controller è stato spento o reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="d6d80-491">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="d6d80-492">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-492">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6d80-493">Commenti</span><span class="sxs-lookup"><span data-stu-id="d6d80-493">Remarks</span></span>

<span data-ttu-id="d6d80-494">La classe **CIM \_ ParallelController** è derivata dal [**\_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-494">The **CIM\_ParallelController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="d6d80-495">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="d6d80-495">WMI does not implement this class.</span></span> <span data-ttu-id="d6d80-496">Per le classi WMI derivate da **CIM \_ ParallelController**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d6d80-496">For WMI classes that are derived from **CIM\_ParallelController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d6d80-497">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="d6d80-497">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d6d80-498">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="d6d80-498">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6d80-499">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6d80-499">Requirements</span></span>



| <span data-ttu-id="d6d80-500">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6d80-500">Requirement</span></span> | <span data-ttu-id="d6d80-501">Valore</span><span class="sxs-lookup"><span data-stu-id="d6d80-501">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d80-502">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6d80-502">Minimum supported client</span></span><br/> | <span data-ttu-id="d6d80-503">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6d80-503">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6d80-504">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6d80-504">Minimum supported server</span></span><br/> | <span data-ttu-id="d6d80-505">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6d80-505">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6d80-506">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d6d80-506">Namespace</span></span><br/>                | <span data-ttu-id="d6d80-507">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d6d80-507">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d6d80-508">MOF</span><span class="sxs-lookup"><span data-stu-id="d6d80-508">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6d80-509"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6d80-509"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6d80-510">DLL</span><span class="sxs-lookup"><span data-stu-id="d6d80-510">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6d80-511"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6d80-511"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6d80-512">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6d80-512">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6d80-513">**\_Controller CIM**</span><span class="sxs-lookup"><span data-stu-id="d6d80-513">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

