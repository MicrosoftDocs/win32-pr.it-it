---
description: La \_ classe CIM PCMCIAController rappresenta le funzionalità e la gestione di un controller PCMCIA (Personal Computer Memory Card International Association).
ms.assetid: 341cbc6c-dd25-4dea-bcce-cd4e3f4d5324
ms.tgt_platform: multiple
title: Classe CIM_PCMCIAController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCMCIAController
- CIM_PCMCIAController.Availability
- CIM_PCMCIAController.Caption
- CIM_PCMCIAController.ConfigManagerErrorCode
- CIM_PCMCIAController.ConfigManagerUserConfig
- CIM_PCMCIAController.CreationClassName
- CIM_PCMCIAController.Description
- CIM_PCMCIAController.DeviceID
- CIM_PCMCIAController.ErrorCleared
- CIM_PCMCIAController.ErrorDescription
- CIM_PCMCIAController.InstallDate
- CIM_PCMCIAController.LastErrorCode
- CIM_PCMCIAController.Manufacturer
- CIM_PCMCIAController.MaxNumberControlled
- CIM_PCMCIAController.Name
- CIM_PCMCIAController.PNPDeviceID
- CIM_PCMCIAController.PowerManagementCapabilities
- CIM_PCMCIAController.PowerManagementSupported
- CIM_PCMCIAController.ProtocolSupported
- CIM_PCMCIAController.Status
- CIM_PCMCIAController.StatusInfo
- CIM_PCMCIAController.SystemCreationClassName
- CIM_PCMCIAController.SystemName
- CIM_PCMCIAController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 95d05e11dd0c439708c477e3ec776bc7a2c333d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126537"
---
# <a name="cim_pcmciacontroller-class"></a><span data-ttu-id="771a7-103">CIM \_ PCMCIAController (classe)</span><span class="sxs-lookup"><span data-stu-id="771a7-103">CIM\_PCMCIAController class</span></span>

<span data-ttu-id="771a7-104">La classe **CIM \_ PCMCIAController** rappresenta le funzionalità e la gestione di un controller PCMCIA (Personal Computer Memory Card International Association).</span><span class="sxs-lookup"><span data-stu-id="771a7-104">The **CIM\_PCMCIAController** class represents the capabilities and management of a Personal Computer Memory Card International Association (PCMCIA) controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="771a7-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="771a7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="771a7-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="771a7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="771a7-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="771a7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="771a7-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="771a7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="771a7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="771a7-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B5A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PCMCIAController : cim_controller
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
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

## <a name="members"></a><span data-ttu-id="771a7-110">Members</span><span class="sxs-lookup"><span data-stu-id="771a7-110">Members</span></span>

<span data-ttu-id="771a7-111">La classe **CIM \_ PCMCIAController** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="771a7-111">The **CIM\_PCMCIAController** class has these types of members:</span></span>

-   [<span data-ttu-id="771a7-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="771a7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="771a7-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="771a7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="771a7-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="771a7-114">Methods</span></span>

<span data-ttu-id="771a7-115">La classe **CIM \_ PCMCIAController** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="771a7-115">The **CIM\_PCMCIAController** class has these methods.</span></span>



| <span data-ttu-id="771a7-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="771a7-116">Method</span></span>                                                                      | <span data-ttu-id="771a7-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="771a7-117">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="771a7-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="771a7-118">**Reset**</span></span>](reset-method-in-class-cim-pcmciacontroller.md)                 | <span data-ttu-id="771a7-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="771a7-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="771a7-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="771a7-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="771a7-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="771a7-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pcmciacontroller.md) | <span data-ttu-id="771a7-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="771a7-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="771a7-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="771a7-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="771a7-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="771a7-124">Properties</span></span>

<span data-ttu-id="771a7-125">La classe **CIM \_ PCMCIAController** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="771a7-125">The **CIM\_PCMCIAController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="771a7-126">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="771a7-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="771a7-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-129">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="771a7-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="771a7-130">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="771a7-130">Availability and status of the device.</span></span> <span data-ttu-id="771a7-131">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="771a7-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="771a7-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-133">Altro.</span><span class="sxs-lookup"><span data-stu-id="771a7-133">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="771a7-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="771a7-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-135">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="771a7-135">Unknown.</span></span>

</dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="771a7-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="771a7-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-137">In esecuzione o a potenza intera.</span><span class="sxs-lookup"><span data-stu-id="771a7-137">Running or full power.</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="771a7-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="771a7-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-139">Avviso.</span><span class="sxs-lookup"><span data-stu-id="771a7-139">Warning.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="771a7-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="771a7-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-141">Test.</span><span class="sxs-lookup"><span data-stu-id="771a7-141">Testing.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="771a7-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="771a7-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-143">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="771a7-143">Not applicable.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="771a7-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="771a7-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-145">Spegnimento.</span><span class="sxs-lookup"><span data-stu-id="771a7-145">Power off.</span></span>

</dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="771a7-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="771a7-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-147">Offline.</span><span class="sxs-lookup"><span data-stu-id="771a7-147">Offline.</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="771a7-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="771a7-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-149">Fuori servizio.</span><span class="sxs-lookup"><span data-stu-id="771a7-149">Off duty.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="771a7-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="771a7-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-151">Danneggiato.</span><span class="sxs-lookup"><span data-stu-id="771a7-151">Degraded.</span></span>

</dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="771a7-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="771a7-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-153">Non installato.</span><span class="sxs-lookup"><span data-stu-id="771a7-153">Not installed.</span></span>

</dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="771a7-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="771a7-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-155">Errore di installazione.</span><span class="sxs-lookup"><span data-stu-id="771a7-155">Install error.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="771a7-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="771a7-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-157">Il dispositivo è noto in modalità di risparmio energia, ma lo stato esatto in questa modalità è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="771a7-157">Device is known to be in a power save mode, but its exact status in this mode is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="771a7-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="771a7-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-159">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="771a7-159">Device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="771a7-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="771a7-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-161">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="771a7-161">Device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="771a7-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="771a7-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-163">Ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="771a7-163">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="771a7-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="771a7-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-165">Il dispositivo è in uno stato di avviso e anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="771a7-165">Device is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="771a7-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="771a7-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-167">(sospeso)</span><span class="sxs-lookup"><span data-stu-id="771a7-167">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="771a7-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="771a7-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-169">Non pronto.</span><span class="sxs-lookup"><span data-stu-id="771a7-169">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="771a7-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="771a7-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-171">Non configurata.</span><span class="sxs-lookup"><span data-stu-id="771a7-171">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="771a7-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="771a7-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-173">Il controller PCMCIA non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="771a7-173">The PCMCIA controller is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="771a7-174">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="771a7-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="771a7-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-177">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="771a7-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="771a7-178">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="771a7-178">Short textual description of the object.</span></span>

<span data-ttu-id="771a7-179">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="771a7-180">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="771a7-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-181">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="771a7-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-183">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="771a7-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="771a7-184">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="771a7-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="771a7-185">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="771a7-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="771a7-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="771a7-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="771a7-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-188">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="771a7-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="771a7-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="771a7-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="771a7-190">(1)</span><span class="sxs-lookup"><span data-stu-id="771a7-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-191">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="771a7-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="771a7-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="771a7-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="771a7-193">(2)</span><span class="sxs-lookup"><span data-stu-id="771a7-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="771a7-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="771a7-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="771a7-195">(3)</span><span class="sxs-lookup"><span data-stu-id="771a7-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-196">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="771a7-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="771a7-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="771a7-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="771a7-198">(4)</span><span class="sxs-lookup"><span data-stu-id="771a7-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-199">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="771a7-199">Device is not working properly.</span></span> <span data-ttu-id="771a7-200">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="771a7-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="771a7-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="771a7-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="771a7-202">(5)</span><span class="sxs-lookup"><span data-stu-id="771a7-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-203">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="771a7-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="771a7-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="771a7-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="771a7-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="771a7-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-206">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="771a7-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="771a7-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="771a7-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="771a7-208">(7)</span><span class="sxs-lookup"><span data-stu-id="771a7-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="771a7-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="771a7-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="771a7-210">(8)</span><span class="sxs-lookup"><span data-stu-id="771a7-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-211">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="771a7-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="771a7-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="771a7-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="771a7-213">(9)</span><span class="sxs-lookup"><span data-stu-id="771a7-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-214">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="771a7-214">Device is not working properly.</span></span> <span data-ttu-id="771a7-215">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="771a7-215">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="771a7-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="771a7-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="771a7-217">(10)</span><span class="sxs-lookup"><span data-stu-id="771a7-217">(10)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-218">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="771a7-218">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="771a7-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="771a7-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="771a7-220">(11)</span><span class="sxs-lookup"><span data-stu-id="771a7-220">(11)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-221">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="771a7-221">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="771a7-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="771a7-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="771a7-223">12</span><span class="sxs-lookup"><span data-stu-id="771a7-223">(12)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-224">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="771a7-224">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="771a7-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="771a7-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="771a7-226">(13)</span><span class="sxs-lookup"><span data-stu-id="771a7-226">(13)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-227">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="771a7-227">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="771a7-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="771a7-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="771a7-229">(14)</span><span class="sxs-lookup"><span data-stu-id="771a7-229">(14)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-230">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="771a7-230">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="771a7-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="771a7-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="771a7-232">(15)</span><span class="sxs-lookup"><span data-stu-id="771a7-232">(15)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-233">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="771a7-233">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="771a7-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="771a7-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="771a7-235">(16)</span><span class="sxs-lookup"><span data-stu-id="771a7-235">(16)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-236">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="771a7-236">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="771a7-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="771a7-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="771a7-238">(17)</span><span class="sxs-lookup"><span data-stu-id="771a7-238">(17)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-239">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="771a7-239">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="771a7-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="771a7-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="771a7-241">(18)</span><span class="sxs-lookup"><span data-stu-id="771a7-241">(18)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-242">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="771a7-242">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="771a7-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="771a7-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="771a7-244">(19)</span><span class="sxs-lookup"><span data-stu-id="771a7-244">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="771a7-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="771a7-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="771a7-246">(20)</span><span class="sxs-lookup"><span data-stu-id="771a7-246">(20)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-247">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="771a7-247">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="771a7-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="771a7-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="771a7-249">(21)</span><span class="sxs-lookup"><span data-stu-id="771a7-249">(21)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-250">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="771a7-250">System failure.</span></span> <span data-ttu-id="771a7-251">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="771a7-251">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="771a7-252">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="771a7-252">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="771a7-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="771a7-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="771a7-254">(22)</span><span class="sxs-lookup"><span data-stu-id="771a7-254">(22)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-255">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="771a7-255">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="771a7-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="771a7-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="771a7-257">(23)</span><span class="sxs-lookup"><span data-stu-id="771a7-257">(23)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-258">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="771a7-258">System failure.</span></span> <span data-ttu-id="771a7-259">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="771a7-259">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="771a7-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="771a7-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="771a7-261">(24)</span><span class="sxs-lookup"><span data-stu-id="771a7-261">(24)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-262">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="771a7-262">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="771a7-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="771a7-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="771a7-264">(25)</span><span class="sxs-lookup"><span data-stu-id="771a7-264">(25)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-265">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="771a7-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="771a7-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="771a7-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="771a7-267">(26)</span><span class="sxs-lookup"><span data-stu-id="771a7-267">(26)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-268">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="771a7-268">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="771a7-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="771a7-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="771a7-270">(27)</span><span class="sxs-lookup"><span data-stu-id="771a7-270">(27)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-271">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="771a7-271">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="771a7-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="771a7-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="771a7-273">(28)</span><span class="sxs-lookup"><span data-stu-id="771a7-273">(28)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-274">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="771a7-274">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="771a7-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="771a7-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="771a7-276">(29)</span><span class="sxs-lookup"><span data-stu-id="771a7-276">(29)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-277">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="771a7-277">Device is disabled.</span></span> <span data-ttu-id="771a7-278">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="771a7-278">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="771a7-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="771a7-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="771a7-280">(30)</span><span class="sxs-lookup"><span data-stu-id="771a7-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-281">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="771a7-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="771a7-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="771a7-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="771a7-283">31</span><span class="sxs-lookup"><span data-stu-id="771a7-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-284">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="771a7-284">Device is not working properly.</span></span> <span data-ttu-id="771a7-285">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="771a7-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="771a7-286">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="771a7-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-287">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="771a7-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-289">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="771a7-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="771a7-290">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="771a7-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="771a7-291">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="771a7-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="771a7-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-293">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="771a7-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-295">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="771a7-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="771a7-296">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="771a7-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="771a7-297">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="771a7-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="771a7-298">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="771a7-299">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="771a7-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="771a7-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-302">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="771a7-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="771a7-303">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="771a7-303">Textual description of the object.</span></span>

<span data-ttu-id="771a7-304">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="771a7-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="771a7-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-306">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="771a7-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-308">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="771a7-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="771a7-309">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="771a7-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="771a7-310">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="771a7-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="771a7-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-312">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="771a7-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="771a7-314">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="771a7-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="771a7-315">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="771a7-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="771a7-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-317">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="771a7-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="771a7-319">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="771a7-319">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="771a7-320">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="771a7-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="771a7-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-322">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="771a7-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-324">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="771a7-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="771a7-325">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="771a7-325">Date and time the object was installed.</span></span> <span data-ttu-id="771a7-326">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="771a7-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="771a7-327">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="771a7-328">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="771a7-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-329">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="771a7-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="771a7-331">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="771a7-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="771a7-332">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="771a7-333">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="771a7-333">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-334">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="771a7-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-336">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="771a7-336">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="771a7-337">Nome del produttore del controller PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="771a7-337">Name of the PCMCIA controller manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="771a7-338">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="771a7-338">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-339">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="771a7-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-341">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="771a7-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="771a7-342">Numero massimo di entità indirizzabili direttamente supportate dal controller.</span><span class="sxs-lookup"><span data-stu-id="771a7-342">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="771a7-343">Se il numero è sconosciuto o illimitato, è necessario utilizzare il valore 0.</span><span class="sxs-lookup"><span data-stu-id="771a7-343">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="771a7-344">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-344">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="771a7-345">**Nome**</span><span class="sxs-lookup"><span data-stu-id="771a7-345">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-346">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="771a7-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-348">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="771a7-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="771a7-349">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="771a7-349">Label by which the object is known.</span></span> <span data-ttu-id="771a7-350">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="771a7-350">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="771a7-351">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-351">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="771a7-352">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="771a7-352">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-353">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="771a7-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-355">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="771a7-355">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="771a7-356">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="771a7-356">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="771a7-357">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-357">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="771a7-358">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="771a7-358">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="771a7-359">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="771a7-359">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-360">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="771a7-360">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="771a7-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="771a7-362">Funzionalità specifiche relative al risparmio di energia del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="771a7-362">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="771a7-363">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="771a7-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="771a7-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-365">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="771a7-365">Unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="771a7-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="771a7-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-367">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="771a7-367">Not supported.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="771a7-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="771a7-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-369">Disattivato.</span><span class="sxs-lookup"><span data-stu-id="771a7-369">Disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="771a7-370"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="771a7-370"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-371">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="771a7-371">Power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="771a7-372"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="771a7-372"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-373">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="771a7-373">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="771a7-374"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="771a7-374"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-375">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="771a7-375">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="771a7-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="771a7-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-377">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").</span><span class="sxs-lookup"><span data-stu-id="771a7-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="771a7-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="771a7-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="771a7-379">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e il parametro *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="771a7-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="771a7-380">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="771a7-380">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-381">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="771a7-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="771a7-383">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="771a7-383">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="771a7-384">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="771a7-384">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="771a7-385">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="771a7-385">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="771a7-386">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="771a7-386">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="771a7-387">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-387">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="771a7-388">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="771a7-388">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-389">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="771a7-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-391">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,2 "," MIF. \|Dischi DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="771a7-391">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="771a7-392">Protocollo usato dal controller per accedere ai dispositivi "controllati".</span><span class="sxs-lookup"><span data-stu-id="771a7-392">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="771a7-393">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-393">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="771a7-394">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="771a7-394">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="771a7-395">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="771a7-395">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="771a7-396">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="771a7-396">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="771a7-397">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="771a7-397">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="771a7-398">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="771a7-398">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="771a7-399">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="771a7-399">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="771a7-400">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="771a7-400">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="771a7-401">**Dischetto flessibile** (7)</span><span class="sxs-lookup"><span data-stu-id="771a7-401">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="771a7-402">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="771a7-402">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="771a7-403">**Interfaccia parallela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="771a7-403">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="771a7-404">**Protocollo di Fibre Channel SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="771a7-404">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="771a7-405">**Protocollo bus seriale SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="771a7-405">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="771a7-406">**Protocollo bus seriale SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="771a7-406">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="771a7-407">**Architettura di archiviazione seriale SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="771a7-407">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="771a7-408">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="771a7-408">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="771a7-409">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="771a7-409">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="771a7-410">**Bus seriale universale** (16)</span><span class="sxs-lookup"><span data-stu-id="771a7-410">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="771a7-411">**Protocollo parallelo** (17)</span><span class="sxs-lookup"><span data-stu-id="771a7-411">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="771a7-412">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="771a7-412">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="771a7-413">**Diagnostica** (19)</span><span class="sxs-lookup"><span data-stu-id="771a7-413">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="771a7-414">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="771a7-414">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="771a7-415">**Potenza** (21)</span><span class="sxs-lookup"><span data-stu-id="771a7-415">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="771a7-416">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="771a7-416">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="771a7-417">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="771a7-417">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="771a7-418">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="771a7-418">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="771a7-419">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="771a7-419">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="771a7-420">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="771a7-420">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="771a7-421">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="771a7-421">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="771a7-422">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="771a7-422">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="771a7-423">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="771a7-423">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="771a7-424">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="771a7-424">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="771a7-425">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="771a7-425">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="771a7-426">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="771a7-426">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="771a7-427">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="771a7-427">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="771a7-428">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="771a7-428">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="771a7-429">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="771a7-429">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="771a7-430">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="771a7-430">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="771a7-431">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="771a7-431">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="771a7-432">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="771a7-432">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="771a7-433">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="771a7-433">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="771a7-434">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="771a7-434">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="771a7-435">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="771a7-435">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="771a7-436">**ATA/IDE avanzato** (42)</span><span class="sxs-lookup"><span data-stu-id="771a7-436">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="771a7-437">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="771a7-437">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="771a7-438">**TWIRP (infrarossi bidirezionali)** (44)</span><span class="sxs-lookup"><span data-stu-id="771a7-438">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="771a7-439">**FIR (infrarossi veloci)** (45)</span><span class="sxs-lookup"><span data-stu-id="771a7-439">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="771a7-440">**Sir (Serial Infrared)** (46)</span><span class="sxs-lookup"><span data-stu-id="771a7-440">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="771a7-441">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="771a7-441">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="771a7-442">**Status**</span><span class="sxs-lookup"><span data-stu-id="771a7-442">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-443">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="771a7-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-444">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-445">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="771a7-445">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="771a7-446">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="771a7-446">Current status of the object.</span></span> <span data-ttu-id="771a7-447">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="771a7-448">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="771a7-448">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="771a7-449">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="771a7-449">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="771a7-450">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="771a7-450">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="771a7-451">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="771a7-451">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="771a7-452">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="771a7-452">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="771a7-453">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="771a7-453">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="771a7-454">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="771a7-454">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="771a7-455">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="771a7-455">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="771a7-456">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="771a7-456">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="771a7-457">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="771a7-457">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="771a7-458">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="771a7-458">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="771a7-459">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="771a7-459">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="771a7-460">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="771a7-460">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="771a7-461">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="771a7-461">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-462">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="771a7-462">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-463">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-464">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="771a7-464">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="771a7-465">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="771a7-465">State of the logical device.</span></span> <span data-ttu-id="771a7-466">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="771a7-466">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="771a7-467">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="771a7-468">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="771a7-468">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="771a7-469">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="771a7-469">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="771a7-470">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="771a7-470">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="771a7-471">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="771a7-471">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="771a7-472">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="771a7-472">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="771a7-473">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="771a7-473">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-474">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="771a7-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-475">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-476">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="771a7-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="771a7-477">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="771a7-477">Scoping system's creation class name.</span></span>

<span data-ttu-id="771a7-478">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="771a7-479">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="771a7-479">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-480">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="771a7-480">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-481">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="771a7-482">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="771a7-482">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="771a7-483">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="771a7-483">Scoping system's name.</span></span>

<span data-ttu-id="771a7-484">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="771a7-485">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="771a7-485">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="771a7-486">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="771a7-486">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="771a7-487">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="771a7-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="771a7-488">Data e ora dell'ultima reimpostazione del controller, ovvero il controller è stato spento o reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="771a7-488">Date and time this controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="771a7-489">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-489">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="771a7-490">Commenti</span><span class="sxs-lookup"><span data-stu-id="771a7-490">Remarks</span></span>

<span data-ttu-id="771a7-491">La classe **CIM \_ PCMCIAController** è derivata dal [**\_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-491">The **CIM\_PCMCIAController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="771a7-492">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="771a7-492">WMI does not implement this class.</span></span> <span data-ttu-id="771a7-493">Per le classi WMI derivate da **CIM \_ PCMCIAController**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="771a7-493">For WMI classes that are derived from **CIM\_PCMCIAController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="771a7-494">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="771a7-494">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="771a7-495">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="771a7-495">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="771a7-496">Requisiti</span><span class="sxs-lookup"><span data-stu-id="771a7-496">Requirements</span></span>



| <span data-ttu-id="771a7-497">Requisito</span><span class="sxs-lookup"><span data-stu-id="771a7-497">Requirement</span></span> | <span data-ttu-id="771a7-498">Valore</span><span class="sxs-lookup"><span data-stu-id="771a7-498">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="771a7-499">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="771a7-499">Minimum supported client</span></span><br/> | <span data-ttu-id="771a7-500">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="771a7-500">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="771a7-501">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="771a7-501">Minimum supported server</span></span><br/> | <span data-ttu-id="771a7-502">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="771a7-502">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="771a7-503">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="771a7-503">Namespace</span></span><br/>                | <span data-ttu-id="771a7-504">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="771a7-504">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="771a7-505">MOF</span><span class="sxs-lookup"><span data-stu-id="771a7-505">MOF</span></span><br/>                      | <dl> <span data-ttu-id="771a7-506"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="771a7-506"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="771a7-507">DLL</span><span class="sxs-lookup"><span data-stu-id="771a7-507">DLL</span></span><br/>                      | <dl> <span data-ttu-id="771a7-508"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="771a7-508"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="771a7-509">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="771a7-509">See also</span></span>

<dl> <dt>

[<span data-ttu-id="771a7-510">**\_controller CIM**</span><span class="sxs-lookup"><span data-stu-id="771a7-510">**cim\_controller**</span></span>](cim-controller.md)
</dt> </dl>

 

