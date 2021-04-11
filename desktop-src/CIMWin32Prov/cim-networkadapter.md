---
description: La \_ classe CIM NetworkAdapter è una classe astratta che definisce i concetti relativi all'hardware di rete generale, ad esempio l'indirizzo permanente o la velocità dell'operazione. Le informazioni vengono trasmesse mediante l'associazione CIM \_ DeviceSAPImplementation.
ms.assetid: dd44e05a-1124-42c2-aa69-340c06da35a2
ms.tgt_platform: multiple
title: Classe CIM_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkAdapter
- CIM_NetworkAdapter.AutoSense
- CIM_NetworkAdapter.Availability
- CIM_NetworkAdapter.Caption
- CIM_NetworkAdapter.ConfigManagerErrorCode
- CIM_NetworkAdapter.ConfigManagerUserConfig
- CIM_NetworkAdapter.CreationClassName
- CIM_NetworkAdapter.Description
- CIM_NetworkAdapter.DeviceID
- CIM_NetworkAdapter.ErrorCleared
- CIM_NetworkAdapter.ErrorDescription
- CIM_NetworkAdapter.InstallDate
- CIM_NetworkAdapter.LastErrorCode
- CIM_NetworkAdapter.MaxSpeed
- CIM_NetworkAdapter.Name
- CIM_NetworkAdapter.NetworkAddresses
- CIM_NetworkAdapter.PermanentAddress
- CIM_NetworkAdapter.PNPDeviceID
- CIM_NetworkAdapter.PowerManagementCapabilities
- CIM_NetworkAdapter.PowerManagementSupported
- CIM_NetworkAdapter.Speed
- CIM_NetworkAdapter.Status
- CIM_NetworkAdapter.StatusInfo
- CIM_NetworkAdapter.SystemCreationClassName
- CIM_NetworkAdapter.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 76ec70bb74d74514dfe037c9e67604b29aee541a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127074"
---
# <a name="cim_networkadapter-class"></a><span data-ttu-id="f5551-104">CIM \_ NetworkAdapter (classe)</span><span class="sxs-lookup"><span data-stu-id="f5551-104">CIM\_NetworkAdapter class</span></span>

<span data-ttu-id="f5551-105">La classe **CIM \_ NetworkAdapter** è una classe astratta che definisce i concetti relativi all'hardware di rete generale, ad esempio l'indirizzo permanente o la velocità dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f5551-105">The **CIM\_NetworkAdapter** class is an abstract class that defines general networking hardware concepts (for example, permanent address or speed of operation).</span></span> <span data-ttu-id="f5551-106">Le informazioni vengono trasmesse mediante l'associazione [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) .</span><span class="sxs-lookup"><span data-stu-id="f5551-106">The information is conveyed using the [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) association.</span></span>

<span data-ttu-id="f5551-107">Le schede di rete e gli endpoint correlati rappresentano la possibilità di connettività tra i peer.</span><span class="sxs-lookup"><span data-stu-id="f5551-107">Network adapters and related endpoints represent the potential for connectivity among peers.</span></span> <span data-ttu-id="f5551-108">Il potenziale di connettività è significativamente diverso da quello del Master, del subordinato e del controller o delle relazioni controllate dal [**\_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-108">The potential for connectivity is significantly different from the master or subordinate and controller or controlled-by relationships of [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="f5551-109">Occasionalmente, tuttavia, un singolo dispositivo funge sia da scheda di rete che da controller, ad esempio quando una scheda Fibre Channel funziona come controller SCSI del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="f5551-109">Occasionally, however, a single device acts as both a network adapter and a controller, for example, when a fiber channel adapter operates as a computer system's SCSI controller.</span></span> <span data-ttu-id="f5551-110">In tal caso, gli aspetti del dispositivo sono orientati alla rete e altri sono orientati ai controller.</span><span class="sxs-lookup"><span data-stu-id="f5551-110">In which case, aspects of the device are network oriented and others are controller oriented.</span></span> <span data-ttu-id="f5551-111">È necessario creare un'istanza delle classi controller e adapter e creare anche una relazione di identità del dispositivo per collegare i diversi aspetti del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5551-111">The controller and adapter classes should be instantiated and a device identity relationship should also be created to link the different aspects of the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5551-112">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f5551-112">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f5551-113">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f5551-113">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f5551-114">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f5551-114">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f5551-115">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f5551-115">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5551-116">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5551-116">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C532-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_NetworkAdapter : CIM_LogicalDevice
{
  boolean  AutoSense;
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
  uint64   MaxSpeed;
  string   Name;
  string   NetworkAddresses[];
  string   PermanentAddress;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint64   Speed;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="f5551-117">Members</span><span class="sxs-lookup"><span data-stu-id="f5551-117">Members</span></span>

<span data-ttu-id="f5551-118">La classe **CIM \_ NetworkAdapter** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f5551-118">The **CIM\_NetworkAdapter** class has these types of members:</span></span>

-   [<span data-ttu-id="f5551-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="f5551-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="f5551-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f5551-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f5551-121">Metodi</span><span class="sxs-lookup"><span data-stu-id="f5551-121">Methods</span></span>

<span data-ttu-id="f5551-122">La classe **CIM \_ NetworkAdapter** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f5551-122">The **CIM\_NetworkAdapter** class has these methods.</span></span>



| <span data-ttu-id="f5551-123">Metodo</span><span class="sxs-lookup"><span data-stu-id="f5551-123">Method</span></span>                                                                    | <span data-ttu-id="f5551-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5551-124">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5551-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="f5551-125">**Reset**</span></span>](reset-method-in-class-cim-networkadapter.md)                 | <span data-ttu-id="f5551-126">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f5551-126">Requests a reset of the logical device.</span></span> <span data-ttu-id="f5551-127">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="f5551-127">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="f5551-128">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f5551-128">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-networkadapter.md) | <span data-ttu-id="f5551-129">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="f5551-129">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="f5551-130">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="f5551-130">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f5551-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f5551-131">Properties</span></span>

<span data-ttu-id="f5551-132">La classe **CIM \_ NetworkAdapter** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f5551-132">The **CIM\_NetworkAdapter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5551-133">**Rilevamento automatico**</span><span class="sxs-lookup"><span data-stu-id="f5551-133">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-134">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f5551-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5551-136">Se **true**, la scheda di rete è in grado di determinare automaticamente la velocità o altre caratteristiche di comunicazione del supporto di rete collegato.</span><span class="sxs-lookup"><span data-stu-id="f5551-136">If **TRUE**, the network adapter can automatically determine the speed or other communications characteristics of the attached network media.</span></span>

</dd> <dt>

<span data-ttu-id="f5551-137">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="f5551-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-138">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f5551-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-140">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="f5551-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f5551-141">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5551-141">Availability and status of the device.</span></span>

<span data-ttu-id="f5551-142">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f5551-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f5551-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f5551-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="f5551-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f5551-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="f5551-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f5551-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="f5551-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f5551-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="f5551-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f5551-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="f5551-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f5551-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="f5551-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f5551-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="f5551-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f5551-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="f5551-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f5551-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="f5551-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f5551-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="f5551-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f5551-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="f5551-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f5551-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="f5551-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-156">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f5551-156">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f5551-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="f5551-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-158">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="f5551-158">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f5551-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="f5551-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-160">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="f5551-160">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f5551-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="f5551-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f5551-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="f5551-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-163">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="f5551-163">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f5551-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="f5551-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-165">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="f5551-165">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f5551-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="f5551-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-167">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="f5551-167">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f5551-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="f5551-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-169">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="f5551-169">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f5551-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="f5551-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-171">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="f5551-171">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f5551-172">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f5551-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5551-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-175">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f5551-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f5551-176">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f5551-176">Short textual description of the object.</span></span>

<span data-ttu-id="f5551-177">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5551-178">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f5551-178">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-179">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5551-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-181">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f5551-181">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f5551-182">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f5551-182">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="f5551-183">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-183">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f5551-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="f5551-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="f5551-185"> (0)</span><span class="sxs-lookup"><span data-stu-id="f5551-185">(0)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-186">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="f5551-186">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f5551-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="f5551-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="f5551-188">(1)</span><span class="sxs-lookup"><span data-stu-id="f5551-188">(1)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-189">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="f5551-189">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f5551-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f5551-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f5551-191">(2)</span><span class="sxs-lookup"><span data-stu-id="f5551-191">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f5551-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="f5551-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f5551-193">(3)</span><span class="sxs-lookup"><span data-stu-id="f5551-193">(3)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-194">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="f5551-194">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f5551-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="f5551-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f5551-196">(4)</span><span class="sxs-lookup"><span data-stu-id="f5551-196">(4)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-197">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="f5551-197">Device is not working properly.</span></span> <span data-ttu-id="f5551-198">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="f5551-198">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f5551-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="f5551-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f5551-200">(5)</span><span class="sxs-lookup"><span data-stu-id="f5551-200">(5)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-201">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="f5551-201">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f5551-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="f5551-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f5551-203"> (6)</span><span class="sxs-lookup"><span data-stu-id="f5551-203">(6)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-204">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="f5551-204">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f5551-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="f5551-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="f5551-206">(7)</span><span class="sxs-lookup"><span data-stu-id="f5551-206">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f5551-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="f5551-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f5551-208">(8)</span><span class="sxs-lookup"><span data-stu-id="f5551-208">(8)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-209">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="f5551-209">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f5551-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="f5551-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f5551-211">(9)</span><span class="sxs-lookup"><span data-stu-id="f5551-211">(9)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-212">Il dispositivo non funziona correttamente; il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5551-212">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f5551-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f5551-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="f5551-214">(10)</span><span class="sxs-lookup"><span data-stu-id="f5551-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-215">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5551-215">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f5551-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f5551-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="f5551-217">(11)</span><span class="sxs-lookup"><span data-stu-id="f5551-217">(11)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-218">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5551-218">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f5551-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="f5551-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f5551-220">12</span><span class="sxs-lookup"><span data-stu-id="f5551-220">(12)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-221">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="f5551-221">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f5551-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f5551-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f5551-223">(13)</span><span class="sxs-lookup"><span data-stu-id="f5551-223">(13)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-224">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5551-224">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f5551-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="f5551-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f5551-226">(14)</span><span class="sxs-lookup"><span data-stu-id="f5551-226">(14)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-227">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="f5551-227">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f5551-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="f5551-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f5551-229">(15)</span><span class="sxs-lookup"><span data-stu-id="f5551-229">(15)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-230">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="f5551-230">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f5551-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f5551-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f5551-232">(16)</span><span class="sxs-lookup"><span data-stu-id="f5551-232">(16)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-233">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5551-233">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f5551-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="f5551-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f5551-235">(17)</span><span class="sxs-lookup"><span data-stu-id="f5551-235">(17)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-236">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f5551-236">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f5551-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f5551-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f5551-238">(18)</span><span class="sxs-lookup"><span data-stu-id="f5551-238">(18)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-239">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5551-239">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f5551-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="f5551-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="f5551-241">(19)</span><span class="sxs-lookup"><span data-stu-id="f5551-241">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f5551-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="f5551-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="f5551-243">(20)</span><span class="sxs-lookup"><span data-stu-id="f5551-243">(20)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-244">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="f5551-244">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f5551-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f5551-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f5551-246">(21)</span><span class="sxs-lookup"><span data-stu-id="f5551-246">(21)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-247">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="f5551-247">System failure.</span></span> <span data-ttu-id="f5551-248">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="f5551-248">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="f5551-249">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5551-249">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f5551-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="f5551-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="f5551-251">(22)</span><span class="sxs-lookup"><span data-stu-id="f5551-251">(22)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-252">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="f5551-252">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f5551-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="f5551-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f5551-254">(23)</span><span class="sxs-lookup"><span data-stu-id="f5551-254">(23)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-255">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="f5551-255">System failure.</span></span> <span data-ttu-id="f5551-256">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="f5551-256">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f5551-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="f5551-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f5551-258">(24)</span><span class="sxs-lookup"><span data-stu-id="f5551-258">(24)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-259">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="f5551-259">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f5551-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f5551-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f5551-261">(25)</span><span class="sxs-lookup"><span data-stu-id="f5551-261">(25)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-262">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5551-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f5551-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f5551-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f5551-264">(26)</span><span class="sxs-lookup"><span data-stu-id="f5551-264">(26)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-265">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5551-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f5551-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="f5551-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f5551-267">(27)</span><span class="sxs-lookup"><span data-stu-id="f5551-267">(27)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-268">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="f5551-268">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f5551-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="f5551-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f5551-270">(28)</span><span class="sxs-lookup"><span data-stu-id="f5551-270">(28)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-271">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="f5551-271">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f5551-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="f5551-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f5551-273">(29)</span><span class="sxs-lookup"><span data-stu-id="f5551-273">(29)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-274">Il dispositivo è disabilitato; il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="f5551-274">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f5551-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f5551-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f5551-276">(30)</span><span class="sxs-lookup"><span data-stu-id="f5551-276">(30)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-277">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5551-277">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f5551-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f5551-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f5551-279">31</span><span class="sxs-lookup"><span data-stu-id="f5551-279">(31)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-280">Il dispositivo non funziona correttamente; Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="f5551-280">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f5551-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="f5551-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-282">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f5551-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-284">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f5551-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f5551-285">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f5551-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f5551-286">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5551-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f5551-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5551-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-290">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f5551-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f5551-291">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="f5551-291">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f5551-292">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="f5551-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f5551-293">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5551-294">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f5551-294">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-295">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5551-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-297">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f5551-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f5551-298">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f5551-298">Textual description of the object.</span></span>

<span data-ttu-id="f5551-299">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5551-300">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f5551-300">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-301">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5551-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-303">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f5551-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f5551-304">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f5551-304">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="f5551-305">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5551-306">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f5551-306">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-307">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f5551-307">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5551-309">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="f5551-309">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="f5551-310">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5551-311">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f5551-311">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-312">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5551-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5551-314">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="f5551-314">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="f5551-315">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5551-316">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f5551-316">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-317">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f5551-317">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-319">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="f5551-319">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f5551-320">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f5551-320">Date and time the object was installed.</span></span> <span data-ttu-id="f5551-321">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="f5551-321">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f5551-322">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-322">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5551-323">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f5551-323">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-324">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5551-324">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5551-326">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f5551-326">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f5551-327">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5551-328">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="f5551-328">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-329">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f5551-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-331">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="f5551-331">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="f5551-332">Velocità massima, in bit al secondo (BPS), per la scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="f5551-332">Maximum speed, in bits per second (BPS), for the network adapter.</span></span>

<span data-ttu-id="f5551-333">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f5551-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f5551-334">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f5551-334">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-335">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5551-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-337">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f5551-337">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f5551-338">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="f5551-338">Label by which the object is known.</span></span> <span data-ttu-id="f5551-339">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="f5551-339">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f5551-340">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5551-341">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="f5551-341">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-342">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f5551-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f5551-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-344">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Scheda di rete DMTF 802 porta \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="f5551-344">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="f5551-345">Elenco di indirizzi di rete per un adapter.</span><span class="sxs-lookup"><span data-stu-id="f5551-345">List of network addresses for an adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f5551-346">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="f5551-346">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-347">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5551-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-349">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Scheda di rete DMTF 802 porta \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="f5551-349">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="f5551-350">Indirizzo di rete hardcoded in un adapter.</span><span class="sxs-lookup"><span data-stu-id="f5551-350">Network address hard-coded into an adapter.</span></span> <span data-ttu-id="f5551-351">L'indirizzo hardcoded può essere modificato con un aggiornamento del firmware o una configurazione software.</span><span class="sxs-lookup"><span data-stu-id="f5551-351">The hard-coded address can be changed with a firmware upgrade or software configuration.</span></span> <span data-ttu-id="f5551-352">Se modificato, il campo deve essere aggiornato quando viene apportata la modifica.</span><span class="sxs-lookup"><span data-stu-id="f5551-352">If changed, the field should be updated when the change is made.</span></span> <span data-ttu-id="f5551-353">Questa proprietà deve essere lasciata vuota se non esiste alcun indirizzo hardcoded per la scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="f5551-353">This property should be left blank if no hard-coded address exists for the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f5551-354">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f5551-354">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-355">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5551-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-357">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f5551-357">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f5551-358">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f5551-358">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="f5551-359">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="f5551-360">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="f5551-360">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="f5551-361">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f5551-361">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-362">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f5551-362">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f5551-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5551-364">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f5551-364">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="f5551-365">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="f5551-365">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f5551-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f5551-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f5551-367"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="f5551-367"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f5551-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="f5551-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f5551-369"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="f5551-369"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-370">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="f5551-370">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f5551-371"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="f5551-371"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-372">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="f5551-372">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f5551-373"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="f5551-373"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-374">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="f5551-374">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="f5551-375">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="f5551-375">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="f5551-376">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="f5551-376">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f5551-377"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="f5551-377"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-378">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="f5551-378">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f5551-379"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="f5551-379"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f5551-380">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="f5551-380">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f5551-381">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f5551-381">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-382">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f5551-382">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5551-384">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="f5551-384">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="f5551-385">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="f5551-385">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f5551-386">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="f5551-386">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="f5551-387">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="f5551-387">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="f5551-388">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-388">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5551-389">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="f5551-389">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-390">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f5551-390">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-391">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-392">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| RFC1213-MIB. ifSpeed "," MIF. \|Scheda di rete DMTF 802 porta \| 001,5 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bit al secondo ")</span><span class="sxs-lookup"><span data-stu-id="f5551-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|RFC1213-MIB.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="f5551-393">Stima della larghezza di banda corrente, in BPS.</span><span class="sxs-lookup"><span data-stu-id="f5551-393">Estimate of the current bandwidth, in BPS.</span></span> <span data-ttu-id="f5551-394">Per gli endpoint che variano a seconda della larghezza di banda o per quelli in cui non è possibile effettuare una stima accurata, questa proprietà deve contenere la larghezza di banda nominale.</span><span class="sxs-lookup"><span data-stu-id="f5551-394">For endpoints that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

<span data-ttu-id="f5551-395">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f5551-395">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f5551-396">**Status**</span><span class="sxs-lookup"><span data-stu-id="f5551-396">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-397">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5551-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-398">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-399">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f5551-399">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f5551-400">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f5551-400">Current status of the object.</span></span>

<span data-ttu-id="f5551-401">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f5551-402">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f5551-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f5551-403">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f5551-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f5551-404">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="f5551-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f5551-405">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="f5551-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f5551-406">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="f5551-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f5551-407">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="f5551-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f5551-408">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="f5551-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f5551-409">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="f5551-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f5551-410">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="f5551-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f5551-411">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="f5551-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f5551-412">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="f5551-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f5551-413">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="f5551-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f5551-414">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="f5551-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f5551-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f5551-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-416">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f5551-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-417">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-418">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f5551-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f5551-419">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f5551-419">State of the logical device.</span></span> <span data-ttu-id="f5551-420">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="f5551-420">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="f5551-421">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f5551-422">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f5551-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f5551-423">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="f5551-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f5551-424">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="f5551-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f5551-425">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="f5551-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f5551-426">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="f5551-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f5551-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f5551-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-428">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5551-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-429">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-430">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f5551-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f5551-431">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="f5551-431">Scoping system's creation class name.</span></span>

<span data-ttu-id="f5551-432">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5551-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f5551-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5551-434">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5551-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5551-435">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5551-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5551-436">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f5551-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f5551-437">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="f5551-437">Scoping system's name.</span></span>

<span data-ttu-id="f5551-438">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5551-439">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5551-439">Remarks</span></span>

<span data-ttu-id="f5551-440">La classe **CIM \_ NetworkAdapter** è derivata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-440">The **CIM\_NetworkAdapter** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="f5551-441">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="f5551-441">WMI does not implement this class.</span></span> <span data-ttu-id="f5551-442">Per le classi derivate da **CIM \_ NetworkAdapter**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f5551-442">For classes that are derived from **CIM\_NetworkAdapter**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f5551-443">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f5551-443">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f5551-444">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f5551-444">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5551-445">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5551-445">Requirements</span></span>



| <span data-ttu-id="f5551-446">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5551-446">Requirement</span></span> | <span data-ttu-id="f5551-447">Valore</span><span class="sxs-lookup"><span data-stu-id="f5551-447">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5551-448">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5551-448">Minimum supported client</span></span><br/> | <span data-ttu-id="f5551-449">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5551-449">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f5551-450">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5551-450">Minimum supported server</span></span><br/> | <span data-ttu-id="f5551-451">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5551-451">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f5551-452">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f5551-452">Namespace</span></span><br/>                | <span data-ttu-id="f5551-453">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f5551-453">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f5551-454">MOF</span><span class="sxs-lookup"><span data-stu-id="f5551-454">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5551-455"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5551-455"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5551-456">DLL</span><span class="sxs-lookup"><span data-stu-id="f5551-456">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5551-457"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5551-457"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5551-458">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5551-458">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5551-459">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="f5551-459">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

