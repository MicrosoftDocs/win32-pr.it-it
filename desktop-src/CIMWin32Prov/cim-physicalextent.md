---
description: La \_ classe CIM PhysicalExtent rappresenta un'implementazione RAID di SCC.
ms.assetid: d1950464-e17a-4651-aa53-6385659994ff
ms.tgt_platform: multiple
title: Classe CIM_PhysicalExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalExtent
- CIM_PhysicalExtent.Access
- CIM_PhysicalExtent.Availability
- CIM_PhysicalExtent.BlockSize
- CIM_PhysicalExtent.Caption
- CIM_PhysicalExtent.ConfigManagerErrorCode
- CIM_PhysicalExtent.ConfigManagerUserConfig
- CIM_PhysicalExtent.CreationClassName
- CIM_PhysicalExtent.Description
- CIM_PhysicalExtent.DeviceID
- CIM_PhysicalExtent.ErrorCleared
- CIM_PhysicalExtent.ErrorDescription
- CIM_PhysicalExtent.ErrorMethodology
- CIM_PhysicalExtent.InstallDate
- CIM_PhysicalExtent.LastErrorCode
- CIM_PhysicalExtent.Name
- CIM_PhysicalExtent.NumberOfBlocks
- CIM_PhysicalExtent.PNPDeviceID
- CIM_PhysicalExtent.PowerManagementCapabilities
- CIM_PhysicalExtent.PowerManagementSupported
- CIM_PhysicalExtent.Purpose
- CIM_PhysicalExtent.Status
- CIM_PhysicalExtent.StatusInfo
- CIM_PhysicalExtent.SystemCreationClassName
- CIM_PhysicalExtent.SystemName
- CIM_PhysicalExtent.UnitsBeforeCheckDataInterleave
- CIM_PhysicalExtent.UnitsOfCheckData
- CIM_PhysicalExtent.UnitsOfUserData
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 31e05d3b339d64fd640460716376c3d8b538fa95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747847"
---
# <a name="cim_physicalextent-class"></a><span data-ttu-id="37927-103">CIM \_ PhysicalExtent (classe)</span><span class="sxs-lookup"><span data-stu-id="37927-103">CIM\_PhysicalExtent class</span></span>

<span data-ttu-id="37927-104">La classe **CIM \_ PhysicalExtent** rappresenta un'implementazione RAID di SCC.</span><span class="sxs-lookup"><span data-stu-id="37927-104">The **CIM\_PhysicalExtent** class represents an SCC RAID implementation.</span></span> <span data-ttu-id="37927-105">Definisce gli indirizzi di blocco indirizzabili consecutivi in un singolo dispositivo di archiviazione che vengono considerati come un singolo extent di archiviazione nella stessa classe [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) .</span><span class="sxs-lookup"><span data-stu-id="37927-105">It defines the consecutive addressable block addresses on a single storage device that are treated as a single storage extent in the same [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class.</span></span> <span data-ttu-id="37927-106">In alternativa, quando si usa la configurazione automatica, è possibile creare un'istanza o estendere la classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) .</span><span class="sxs-lookup"><span data-stu-id="37927-106">An alternative, when automatic configuration is used, is to instantiate or extend the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37927-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="37927-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="37927-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="37927-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="37927-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="37927-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="37927-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="37927-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="37927-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37927-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979E-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalExtent : CIM_StorageExtent
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint64   UnitsBeforeCheckDataInterleave;
  uint64   UnitsOfCheckData;
  uint64   UnitsOfUserData;
};
```

## <a name="members"></a><span data-ttu-id="37927-112">Members</span><span class="sxs-lookup"><span data-stu-id="37927-112">Members</span></span>

<span data-ttu-id="37927-113">La classe **CIM \_ PhysicalExtent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="37927-113">The **CIM\_PhysicalExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="37927-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="37927-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="37927-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="37927-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="37927-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="37927-116">Methods</span></span>

<span data-ttu-id="37927-117">La classe **CIM \_ PhysicalExtent** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="37927-117">The **CIM\_PhysicalExtent** class has these methods.</span></span>



| <span data-ttu-id="37927-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="37927-118">Method</span></span>                                                                    | <span data-ttu-id="37927-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37927-119">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37927-120">**Reset**</span><span class="sxs-lookup"><span data-stu-id="37927-120">**Reset**</span></span>](reset-method-in-class-cim-physicalextent.md)                 | <span data-ttu-id="37927-121">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="37927-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="37927-122">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="37927-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="37927-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="37927-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-physicalextent.md) | <span data-ttu-id="37927-124">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="37927-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="37927-125">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="37927-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="37927-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="37927-126">Properties</span></span>

<span data-ttu-id="37927-127">La classe **CIM \_ PhysicalExtent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="37927-127">The **CIM\_PhysicalExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37927-128">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="37927-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37927-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37927-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37927-131">Proprietà di lettura/scrittura del supporto.</span><span class="sxs-lookup"><span data-stu-id="37927-131">Read/write properties of the media.</span></span>

<span data-ttu-id="37927-132">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="37927-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37927-133">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="37927-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="37927-134">**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="37927-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="37927-135">**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="37927-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="37927-136">**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="37927-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="37927-137">**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="37927-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37927-138">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="37927-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-139">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37927-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37927-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-141">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="37927-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="37927-142">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37927-142">Availability and status of the device.</span></span>

<span data-ttu-id="37927-143">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37927-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="37927-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="37927-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37927-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="37927-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="37927-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="37927-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="37927-147">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="37927-147">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="37927-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="37927-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="37927-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="37927-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="37927-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="37927-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="37927-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="37927-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="37927-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="37927-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="37927-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="37927-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="37927-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="37927-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="37927-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="37927-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="37927-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="37927-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="37927-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="37927-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="37927-158">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="37927-158">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="37927-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="37927-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="37927-160">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="37927-160">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="37927-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="37927-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="37927-162">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="37927-162">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="37927-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="37927-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="37927-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="37927-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="37927-165">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="37927-165">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="37927-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="37927-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="37927-167">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="37927-167">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="37927-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="37927-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="37927-169">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="37927-169">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="37927-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="37927-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="37927-171">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="37927-171">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="37927-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="37927-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="37927-173">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="37927-173">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="37927-174">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="37927-174">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-175">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37927-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37927-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-177">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("BLOCKSIZE"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extent fisico DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="37927-177">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("BlockSize"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="37927-178">Dimensioni, in byte, dei blocchi che formano l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="37927-178">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="37927-179">Se la dimensione del blocco di variabili è, è necessario specificare la dimensione massima del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="37927-179">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="37927-180">Se le dimensioni del blocco sono sconosciute o se un concetto di blocco non è valido, ad esempio per extent di aggregazione, memoria o dischi logici, immettere 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="37927-180">If the block size is unknown or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one) .</span></span>

<span data-ttu-id="37927-181">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="37927-181">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="37927-182">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="37927-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37927-183">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="37927-183">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37927-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37927-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-186">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="37927-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="37927-187">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="37927-187">Short textual description of the object.</span></span>

<span data-ttu-id="37927-188">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="37927-188">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37927-189">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="37927-189">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-190">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37927-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37927-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-192">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="37927-192">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="37927-193">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="37927-193">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="37927-194">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37927-194">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="37927-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="37927-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="37927-196"> (0)</span><span class="sxs-lookup"><span data-stu-id="37927-196">(0)</span></span>


</dt> <dd>

<span data-ttu-id="37927-197">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="37927-197">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="37927-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="37927-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="37927-199">(1)</span><span class="sxs-lookup"><span data-stu-id="37927-199">(1)</span></span>


</dt> <dd>

<span data-ttu-id="37927-200">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="37927-200">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="37927-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37927-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="37927-202">(2)</span><span class="sxs-lookup"><span data-stu-id="37927-202">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="37927-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="37927-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="37927-204">(3)</span><span class="sxs-lookup"><span data-stu-id="37927-204">(3)</span></span>


</dt> <dd>

<span data-ttu-id="37927-205">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="37927-205">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="37927-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="37927-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="37927-207">(4)</span><span class="sxs-lookup"><span data-stu-id="37927-207">(4)</span></span>


</dt> <dd>

<span data-ttu-id="37927-208">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="37927-208">Device is not working properly.</span></span> <span data-ttu-id="37927-209">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="37927-209">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="37927-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="37927-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="37927-211">(5)</span><span class="sxs-lookup"><span data-stu-id="37927-211">(5)</span></span>


</dt> <dd>

<span data-ttu-id="37927-212">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="37927-212">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="37927-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="37927-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="37927-214"> (6)</span><span class="sxs-lookup"><span data-stu-id="37927-214">(6)</span></span>


</dt> <dd>

<span data-ttu-id="37927-215">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="37927-215">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="37927-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="37927-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="37927-217">(7)</span><span class="sxs-lookup"><span data-stu-id="37927-217">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="37927-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="37927-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="37927-219">(8)</span><span class="sxs-lookup"><span data-stu-id="37927-219">(8)</span></span>


</dt> <dd>

<span data-ttu-id="37927-220">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="37927-220">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="37927-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="37927-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="37927-222">(9)</span><span class="sxs-lookup"><span data-stu-id="37927-222">(9)</span></span>


</dt> <dd>

<span data-ttu-id="37927-223">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="37927-223">Device is not working properly.</span></span> <span data-ttu-id="37927-224">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37927-224">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="37927-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37927-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="37927-226">(10)</span><span class="sxs-lookup"><span data-stu-id="37927-226">(10)</span></span>


</dt> <dd>

<span data-ttu-id="37927-227">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37927-227">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="37927-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37927-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="37927-229">(11)</span><span class="sxs-lookup"><span data-stu-id="37927-229">(11)</span></span>


</dt> <dd>

<span data-ttu-id="37927-230">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37927-230">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="37927-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="37927-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="37927-232">12</span><span class="sxs-lookup"><span data-stu-id="37927-232">(12)</span></span>


</dt> <dd>

<span data-ttu-id="37927-233">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="37927-233">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="37927-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37927-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="37927-235">(13)</span><span class="sxs-lookup"><span data-stu-id="37927-235">(13)</span></span>


</dt> <dd>

<span data-ttu-id="37927-236">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37927-236">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="37927-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="37927-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="37927-238">(14)</span><span class="sxs-lookup"><span data-stu-id="37927-238">(14)</span></span>


</dt> <dd>

<span data-ttu-id="37927-239">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="37927-239">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="37927-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="37927-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="37927-241">(15)</span><span class="sxs-lookup"><span data-stu-id="37927-241">(15)</span></span>


</dt> <dd>

<span data-ttu-id="37927-242">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="37927-242">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="37927-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37927-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="37927-244">(16)</span><span class="sxs-lookup"><span data-stu-id="37927-244">(16)</span></span>


</dt> <dd>

<span data-ttu-id="37927-245">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37927-245">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="37927-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="37927-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="37927-247">(17)</span><span class="sxs-lookup"><span data-stu-id="37927-247">(17)</span></span>


</dt> <dd>

<span data-ttu-id="37927-248">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="37927-248">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="37927-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37927-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="37927-250">(18)</span><span class="sxs-lookup"><span data-stu-id="37927-250">(18)</span></span>


</dt> <dd>

<span data-ttu-id="37927-251">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37927-251">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="37927-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="37927-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="37927-253">(19)</span><span class="sxs-lookup"><span data-stu-id="37927-253">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="37927-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="37927-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="37927-255">(20)</span><span class="sxs-lookup"><span data-stu-id="37927-255">(20)</span></span>


</dt> <dd>

<span data-ttu-id="37927-256">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="37927-256">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="37927-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37927-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="37927-258">(21)</span><span class="sxs-lookup"><span data-stu-id="37927-258">(21)</span></span>


</dt> <dd>

<span data-ttu-id="37927-259">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="37927-259">System failure.</span></span> <span data-ttu-id="37927-260">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="37927-260">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="37927-261">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37927-261">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="37927-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="37927-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="37927-263">(22)</span><span class="sxs-lookup"><span data-stu-id="37927-263">(22)</span></span>


</dt> <dd>

<span data-ttu-id="37927-264">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="37927-264">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="37927-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="37927-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="37927-266">(23)</span><span class="sxs-lookup"><span data-stu-id="37927-266">(23)</span></span>


</dt> <dd>

<span data-ttu-id="37927-267">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="37927-267">System failure.</span></span> <span data-ttu-id="37927-268">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="37927-268">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="37927-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="37927-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="37927-270">(24)</span><span class="sxs-lookup"><span data-stu-id="37927-270">(24)</span></span>


</dt> <dd>

<span data-ttu-id="37927-271">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="37927-271">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="37927-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37927-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="37927-273">(25)</span><span class="sxs-lookup"><span data-stu-id="37927-273">(25)</span></span>


</dt> <dd>

<span data-ttu-id="37927-274">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37927-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="37927-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37927-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="37927-276">(26)</span><span class="sxs-lookup"><span data-stu-id="37927-276">(26)</span></span>


</dt> <dd>

<span data-ttu-id="37927-277">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37927-277">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="37927-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="37927-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="37927-279">(27)</span><span class="sxs-lookup"><span data-stu-id="37927-279">(27)</span></span>


</dt> <dd>

<span data-ttu-id="37927-280">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="37927-280">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="37927-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="37927-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="37927-282">(28)</span><span class="sxs-lookup"><span data-stu-id="37927-282">(28)</span></span>


</dt> <dd>

<span data-ttu-id="37927-283">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="37927-283">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="37927-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="37927-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="37927-285">(29)</span><span class="sxs-lookup"><span data-stu-id="37927-285">(29)</span></span>


</dt> <dd>

<span data-ttu-id="37927-286">Il dispositivo è disabilitato; il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="37927-286">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="37927-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37927-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="37927-288">(30)</span><span class="sxs-lookup"><span data-stu-id="37927-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="37927-289">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37927-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="37927-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="37927-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="37927-291">31</span><span class="sxs-lookup"><span data-stu-id="37927-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="37927-292">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="37927-292">Device is not working properly.</span></span> <span data-ttu-id="37927-293">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="37927-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="37927-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="37927-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-295">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="37927-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37927-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-297">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="37927-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="37927-298">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="37927-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="37927-299">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37927-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37927-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="37927-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-301">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37927-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37927-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-303">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="37927-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="37927-304">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="37927-304">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="37927-305">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="37927-305">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="37927-306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37927-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37927-307">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="37927-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-308">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37927-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37927-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-310">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="37927-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="37927-311">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="37927-311">Textual description of the object.</span></span>

<span data-ttu-id="37927-312">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="37927-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37927-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="37927-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-314">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37927-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37927-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-316">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="37927-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="37927-317">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="37927-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="37927-318">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37927-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37927-319">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="37927-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-320">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="37927-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37927-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37927-322">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="37927-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="37927-323">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37927-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37927-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="37927-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-325">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37927-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37927-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37927-327">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="37927-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="37927-328">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37927-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37927-329">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="37927-329">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-330">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37927-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37927-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37927-332">Stringa in formato libero che descrive il tipo di rilevamento e correzione degli errori supportato dall'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="37927-332">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="37927-333">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="37927-333">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="37927-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="37927-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-335">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="37927-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="37927-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-337">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="37927-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="37927-338">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="37927-338">Date and time the object was installed.</span></span> <span data-ttu-id="37927-339">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="37927-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="37927-340">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="37927-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37927-341">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="37927-341">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-342">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37927-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37927-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37927-344">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="37927-344">Last error code reported by the logical device.</span></span>

<span data-ttu-id="37927-345">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37927-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37927-346">**Nome**</span><span class="sxs-lookup"><span data-stu-id="37927-346">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-347">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37927-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37927-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-349">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="37927-349">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="37927-350">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="37927-350">Label by which the object is known.</span></span> <span data-ttu-id="37927-351">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="37927-351">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="37927-352">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="37927-352">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37927-353">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="37927-353">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-354">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37927-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37927-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-356">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Proprietà NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extent fisico DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="37927-356">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="37927-357">Numero totale di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="37927-357">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="37927-358">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="37927-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="37927-359">Se il valore di **blockSize** è 1, questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="37927-359">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="37927-360">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="37927-360">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="37927-361">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="37927-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37927-362">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="37927-362">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-363">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37927-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37927-364">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-365">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="37927-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="37927-366">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="37927-366">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="37927-367">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37927-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="37927-368">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="37927-368">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="37927-369">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="37927-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-370">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37927-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="37927-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37927-372">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="37927-372">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="37927-373">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="37927-373">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37927-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="37927-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="37927-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="37927-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="37927-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="37927-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="37927-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="37927-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="37927-378">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="37927-378">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="37927-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="37927-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="37927-380">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="37927-380">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="37927-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="37927-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="37927-382">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="37927-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="37927-383">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="37927-383">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="37927-384">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="37927-384">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="37927-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="37927-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="37927-386">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="37927-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="37927-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="37927-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="37927-388">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="37927-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="37927-389">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="37927-389">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-390">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="37927-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37927-391">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37927-392">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="37927-392">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="37927-393">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="37927-393">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="37927-394">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="37927-394">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="37927-395">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="37927-395">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="37927-396">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37927-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37927-397">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="37927-397">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-398">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37927-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37927-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37927-400">Stringa in formato libero che descrive i supporti e il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="37927-400">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="37927-401">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="37927-401">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="37927-402">**Status**</span><span class="sxs-lookup"><span data-stu-id="37927-402">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-403">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37927-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37927-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-405">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="37927-405">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="37927-406">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="37927-406">Current status of the object.</span></span>

<span data-ttu-id="37927-407">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="37927-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="37927-408">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="37927-408">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="37927-409">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="37927-409">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="37927-410">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="37927-410">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="37927-411">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="37927-411">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37927-412">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="37927-412">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="37927-413">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="37927-413">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="37927-414">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="37927-414">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="37927-415">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="37927-415">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="37927-416">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="37927-416">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="37927-417">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="37927-417">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="37927-418">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="37927-418">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="37927-419">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="37927-419">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="37927-420">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="37927-420">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37927-421">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="37927-421">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-422">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37927-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37927-423">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-424">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="37927-424">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="37927-425">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="37927-425">State of the logical device.</span></span> <span data-ttu-id="37927-426">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="37927-426">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="37927-427">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37927-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="37927-428">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="37927-428">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37927-429">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="37927-429">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="37927-430">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="37927-430">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="37927-431">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="37927-431">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="37927-432">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="37927-432">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37927-433">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="37927-433">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-434">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37927-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37927-435">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-436">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="37927-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="37927-437">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="37927-437">Scoping system's creation class name.</span></span>

<span data-ttu-id="37927-438">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37927-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37927-439">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="37927-439">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-440">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37927-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37927-441">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-442">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="37927-442">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="37927-443">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="37927-443">Scoping system's name.</span></span>

<span data-ttu-id="37927-444">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="37927-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="37927-445">**UnitsBeforeCheckDataInterleave**</span><span class="sxs-lookup"><span data-stu-id="37927-445">**UnitsBeforeCheckDataInterleave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-446">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37927-446">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37927-447">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-448">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extent fisico DMTF \| 001,6 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="37927-448">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="37927-449">Numero di byte di dati utente da ignorare prima di avviare l'interleave check-data.</span><span class="sxs-lookup"><span data-stu-id="37927-449">Number of user data bytes to skip before starting the check-data interleave.</span></span>

<span data-ttu-id="37927-450">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="37927-450">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37927-451">**UnitsOfCheckData**</span><span class="sxs-lookup"><span data-stu-id="37927-451">**UnitsOfCheckData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-452">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37927-452">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37927-453">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-454">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extent fisico DMTF \| 001,7 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="37927-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="37927-455">Numero di byte da riservare per i dati di controllo.</span><span class="sxs-lookup"><span data-stu-id="37927-455">Number of bytes to be reserved for check data.</span></span>

<span data-ttu-id="37927-456">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="37927-456">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37927-457">**UnitsOfUserData**</span><span class="sxs-lookup"><span data-stu-id="37927-457">**UnitsOfUserData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37927-458">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37927-458">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37927-459">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37927-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37927-460">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extent fisico DMTF \| 001,8 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="37927-460">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="37927-461">Numero di byte da riservare per i dati utente.</span><span class="sxs-lookup"><span data-stu-id="37927-461">Number of bytes to be reserved for user data.</span></span>

<span data-ttu-id="37927-462">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="37927-462">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37927-463">Commenti</span><span class="sxs-lookup"><span data-stu-id="37927-463">Remarks</span></span>

<span data-ttu-id="37927-464">La classe **CIM \_ PhysicalExtent** è derivata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="37927-464">The **CIM\_PhysicalExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="37927-465">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="37927-465">WMI does not implement this class.</span></span>

<span data-ttu-id="37927-466">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="37927-466">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="37927-467">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="37927-467">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="37927-468">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37927-468">Requirements</span></span>



| <span data-ttu-id="37927-469">Requisito</span><span class="sxs-lookup"><span data-stu-id="37927-469">Requirement</span></span> | <span data-ttu-id="37927-470">Valore</span><span class="sxs-lookup"><span data-stu-id="37927-470">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37927-471">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37927-471">Minimum supported client</span></span><br/> | <span data-ttu-id="37927-472">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37927-472">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="37927-473">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37927-473">Minimum supported server</span></span><br/> | <span data-ttu-id="37927-474">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37927-474">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="37927-475">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="37927-475">Namespace</span></span><br/>                | <span data-ttu-id="37927-476">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="37927-476">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="37927-477">MOF</span><span class="sxs-lookup"><span data-stu-id="37927-477">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37927-478"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37927-478"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="37927-479">DLL</span><span class="sxs-lookup"><span data-stu-id="37927-479">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37927-480"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37927-480"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37927-481">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37927-481">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37927-482">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="37927-482">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

