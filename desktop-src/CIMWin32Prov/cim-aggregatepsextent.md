---
description: La \_ classe CIM AggregatePSExtent definisce il numero di blocchi logici indirizzabili in un singolo dispositivo di archiviazione, esclusi i blocchi logici mappati come dati di controllo.
ms.assetid: 6c188955-a963-414d-94f9-b7e1cb5960ed
ms.tgt_platform: multiple
title: Classe CIM_AggregatePSExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePSExtent
- CIM_AggregatePSExtent.Caption
- CIM_AggregatePSExtent.Description
- CIM_AggregatePSExtent.InstallDate
- CIM_AggregatePSExtent.Name
- CIM_AggregatePSExtent.Status
- CIM_AggregatePSExtent.Availability
- CIM_AggregatePSExtent.ConfigManagerErrorCode
- CIM_AggregatePSExtent.ConfigManagerUserConfig
- CIM_AggregatePSExtent.CreationClassName
- CIM_AggregatePSExtent.DeviceID
- CIM_AggregatePSExtent.PowerManagementCapabilities
- CIM_AggregatePSExtent.ErrorCleared
- CIM_AggregatePSExtent.ErrorDescription
- CIM_AggregatePSExtent.LastErrorCode
- CIM_AggregatePSExtent.PNPDeviceID
- CIM_AggregatePSExtent.PowerManagementSupported
- CIM_AggregatePSExtent.StatusInfo
- CIM_AggregatePSExtent.SystemCreationClassName
- CIM_AggregatePSExtent.SystemName
- CIM_AggregatePSExtent.Access
- CIM_AggregatePSExtent.BlockSize
- CIM_AggregatePSExtent.ErrorMethodology
- CIM_AggregatePSExtent.NumberOfBlocks
- CIM_AggregatePSExtent.Purpose
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: edc3f5b91bc39e18321778dbfdbc53446c6c27d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748719"
---
# <a name="cim_aggregatepsextent-class"></a><span data-ttu-id="a9ca8-103">CIM \_ AggregatePSExtent (classe)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-103">CIM\_AggregatePSExtent class</span></span>

<span data-ttu-id="a9ca8-104">La classe **CIM \_ AggregatePSExtent** definisce il numero di blocchi logici indirizzabili in un singolo dispositivo di archiviazione, esclusi i blocchi logici mappati come dati di controllo.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-104">The **CIM\_AggregatePSExtent** class defines the number of addressable logical blocks on a single storage device, excluding logical blocks mapped as check data.</span></span> <span data-ttu-id="a9ca8-105">Se vengono definiti set di volumi, i blocchi logici sono contenuti all'interno di un singolo set di volumi.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-105">If volume sets are defined, the logical blocks are contained within a single volume set.</span></span> <span data-ttu-id="a9ca8-106">Si tratta di un raggruppamento alternativo per [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md), quando sono necessarie solo le informazioni di riepilogo o quando si usa la configurazione automatica.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-106">This is an alternative grouping for [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md), when only summary information is needed or when automatic configuration is used.</span></span>

<span data-ttu-id="a9ca8-107">La configurazione automatica può causare la definizione di migliaia di classi [**\_ ProtectedSpaceExtent CIM**](cim-protectedspaceextent.md) .</span><span class="sxs-lookup"><span data-stu-id="a9ca8-107">Automatic configuration can result in thousands of [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) classes being defined.</span></span> <span data-ttu-id="a9ca8-108">La classe **CIM \_ AggregatePSExtent** è stata definita in modo da non dover modellare i singoli extent.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-108">The **CIM\_AggregatePSExtent** class was defined so that individual extents would not have to be modeled.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9ca8-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a9ca8-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a9ca8-111">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a9ca8-112">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ca8-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9ca8-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{2D0E255C-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AggregatePSExtent : CIM_StorageExtent
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Access;
  uint64   BlockSize;
  string   ErrorMethodology;
  uint64   NumberOfBlocks;
  string   Purpose;
};
```

## <a name="members"></a><span data-ttu-id="a9ca8-114">Members</span><span class="sxs-lookup"><span data-stu-id="a9ca8-114">Members</span></span>

<span data-ttu-id="a9ca8-115">La classe **CIM \_ AggregatePSExtent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a9ca8-115">The **CIM\_AggregatePSExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="a9ca8-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="a9ca8-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="a9ca8-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a9ca8-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a9ca8-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="a9ca8-118">Methods</span></span>

<span data-ttu-id="a9ca8-119">La classe **CIM \_ AggregatePSExtent** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-119">The **CIM\_AggregatePSExtent** class has these methods.</span></span>



| <span data-ttu-id="a9ca8-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="a9ca8-120">Method</span></span>                                                                       | <span data-ttu-id="a9ca8-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9ca8-121">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9ca8-122">**Reset**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-122">**Reset**</span></span>](reset-method-in-class-cim-aggregatepsextent.md)                 | <span data-ttu-id="a9ca8-123">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="a9ca8-124">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-124">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="a9ca8-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-aggregatepsextent.md) | <span data-ttu-id="a9ca8-126">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando il dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-126">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="a9ca8-127">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a9ca8-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a9ca8-128">Properties</span></span>

<span data-ttu-id="a9ca8-129">La classe **CIM \_ AggregatePSExtent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-129">The **CIM\_AggregatePSExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9ca8-130">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-131">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-133">Descrive le proprietà di lettura/scrittura del supporto.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-133">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="a9ca8-134">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9ca8-135">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="a9ca8-136">**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="a9ca8-137">**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="a9ca8-138">**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="a9ca8-139">**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9ca8-140">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-140">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-141">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-143">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-144">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-144">Availability and status of the device.</span></span>

<span data-ttu-id="a9ca8-145">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-145">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a9ca8-146"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-146"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9ca8-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a9ca8-148"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-148"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a9ca8-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a9ca8-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a9ca8-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a9ca8-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="a9ca8-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a9ca8-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="a9ca8-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a9ca8-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a9ca8-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a9ca8-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a9ca8-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a9ca8-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-159">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a9ca8-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-161">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a9ca8-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-163">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-163">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a9ca8-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a9ca8-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-166">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a9ca8-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-168">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a9ca8-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-170">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a9ca8-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-172">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a9ca8-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-174">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a9ca8-175">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-175">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-176">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-178">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-179">Dimensioni, in byte, dei blocchi che formano l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-179">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="a9ca8-180">Se la dimensione del blocco di variabili è, è necessario specificare la dimensione massima del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-180">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="a9ca8-181">Se le dimensioni del blocco sono sconosciute o se un concetto di blocco non è valido, ad esempio per extent di aggregazione, memoria o dischi logici, immettere 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-181">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="a9ca8-182">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="a9ca8-183">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-183">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-184">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-187">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-187">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-188">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-188">A short textual description of the object.</span></span>

<span data-ttu-id="a9ca8-189">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-190">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-190">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-191">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-193">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-193">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-194">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-194">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a9ca8-195">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-195">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a9ca8-196">**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-196">**This device is working properly.**</span></span> <span data-ttu-id="a9ca8-197"> (0)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-197">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a9ca8-198">**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-198">**This device is not configured correctly.**</span></span> <span data-ttu-id="a9ca8-199">(1)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-199">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a9ca8-200">**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-200">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a9ca8-201">(2)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a9ca8-202">**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-202">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a9ca8-203">(3)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-203">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a9ca8-204">**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-204">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a9ca8-205">(4)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-205">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a9ca8-206">**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-206">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a9ca8-207">(5)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-207">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a9ca8-208">**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-208">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a9ca8-209"> (6)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-209">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a9ca8-210">**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-210">**Cannot filter.**</span></span> <span data-ttu-id="a9ca8-211">(7)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-211">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a9ca8-212">**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-212">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a9ca8-213">(8)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-213">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a9ca8-214">**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-214">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a9ca8-215">(9)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-215">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a9ca8-216">**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-216">**This device cannot start.**</span></span> <span data-ttu-id="a9ca8-217">(10)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-217">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a9ca8-218">**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-218">**This device failed.**</span></span> <span data-ttu-id="a9ca8-219">(11)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-219">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a9ca8-220">**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-220">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a9ca8-221">12</span><span class="sxs-lookup"><span data-stu-id="a9ca8-221">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a9ca8-222">**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-222">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a9ca8-223">(13)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-223">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a9ca8-224">**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-224">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a9ca8-225">(14)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-225">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a9ca8-226">**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-226">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a9ca8-227">(15)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-227">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a9ca8-228">**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-228">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a9ca8-229">(16)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-229">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a9ca8-230">**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-230">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a9ca8-231">(17)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-231">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a9ca8-232">**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-232">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a9ca8-233">(18)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-233">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a9ca8-234">**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-234">**Failure using the VxD loader.**</span></span> <span data-ttu-id="a9ca8-235">(19)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a9ca8-236">**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-236">**Your registry might be corrupted.**</span></span> <span data-ttu-id="a9ca8-237">(20)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-237">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a9ca8-238">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-238">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a9ca8-239">(21)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-239">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a9ca8-240">**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-240">**This device is disabled.**</span></span> <span data-ttu-id="a9ca8-241">(22)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-241">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a9ca8-242">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-242">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a9ca8-243">(23)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-243">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a9ca8-244">**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-244">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a9ca8-245">(24)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-245">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a9ca8-246">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-246">**Windows is still setting up this device.**</span></span> <span data-ttu-id="a9ca8-247">(25)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-247">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a9ca8-248">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-248">**Windows is still setting up this device.**</span></span> <span data-ttu-id="a9ca8-249">(26)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-249">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a9ca8-250">**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-250">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a9ca8-251">(27)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-251">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a9ca8-252">**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-252">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a9ca8-253">(28)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-253">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a9ca8-254">**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-254">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a9ca8-255">(29)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-255">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a9ca8-256">**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-256">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a9ca8-257">(30)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-257">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a9ca8-258">**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-258">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a9ca8-259">31</span><span class="sxs-lookup"><span data-stu-id="a9ca8-259">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9ca8-260">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-260">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-261">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-263">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-263">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-264">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-264">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a9ca8-265">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-265">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-266">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-266">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-267">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-269">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-269">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-270">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-270">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a9ca8-271">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-271">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a9ca8-272">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-272">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-273">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-273">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-274">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-276">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-276">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-277">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-277">A textual description of the object.</span></span>

<span data-ttu-id="a9ca8-278">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-278">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-279">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-279">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-280">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-282">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-282">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-283">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-283">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="a9ca8-284">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-285">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-285">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-286">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-286">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-288">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-288">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="a9ca8-289">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-290">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-290">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-291">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-293">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-293">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="a9ca8-294">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-295">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-295">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-296">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-298">Stringa in formato libero che descrive il tipo di rilevamento e correzione degli errori supportato dall'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-298">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="a9ca8-299">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-299">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-300">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-300">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-301">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-301">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-303">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-304">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-304">Indicates when the object was installed.</span></span> <span data-ttu-id="a9ca8-305">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-305">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a9ca8-306">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-307">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-307">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-308">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-310">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-310">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a9ca8-311">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-312">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-312">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-313">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-315">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-315">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-316">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-316">Label by which the object is known.</span></span> <span data-ttu-id="a9ca8-317">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-317">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a9ca8-318">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-319">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-319">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-320">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-320">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-322">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-322">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-323">Numero di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-323">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="a9ca8-324">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-324">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="a9ca8-325">Se il valore di **blockSize** è 1 (uno), questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-325">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="a9ca8-326">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-326">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="a9ca8-327">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-327">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-328">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-328">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-329">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-331">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-332">Indica l'identificatore del dispositivo Plug and Play Win32 del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-332">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="a9ca8-333">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a9ca8-333">Example: "\*PNP030b"</span></span>

<span data-ttu-id="a9ca8-334">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-335">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-335">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-336">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-336">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-338">Indica le funzionalità specifiche relative al risparmio di energia del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-338">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="a9ca8-339">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-339">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9ca8-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-341">Le capacità relative al risparmio di energia sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-341">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a9ca8-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-343">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-343">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a9ca8-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-345">Le capacità correlate all'alimentazione sono state disabilitate.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-345">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a9ca8-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-347">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-347">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a9ca8-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-349">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-349">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a9ca8-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-351">Il metodo **SetPowerState** è supportato.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-351">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="a9ca8-352">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-352">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="a9ca8-353">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-353">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a9ca8-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-355">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").</span><span class="sxs-lookup"><span data-stu-id="a9ca8-355">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a9ca8-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a9ca8-357">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e il parametro *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-357">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a9ca8-358">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-358">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-359">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-360">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-361">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-361">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="a9ca8-362">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="a9ca8-362">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="a9ca8-363">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-363">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="a9ca8-364">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="a9ca8-364">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="a9ca8-365">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-366">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-366">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-367">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-369">Stringa in formato libero che descrive i supporti e il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-369">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="a9ca8-370">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-370">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-371">**Status**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-371">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-372">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-373">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-374">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-375">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-375">String that indicates the current status of the object.</span></span> <span data-ttu-id="a9ca8-376">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-376">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a9ca8-377">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="a9ca8-377">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a9ca8-378">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-378">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a9ca8-379">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="a9ca8-379">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a9ca8-380">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-380">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a9ca8-381">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-381">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a9ca8-382">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-382">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a9ca8-383">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a9ca8-383">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a9ca8-384">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-384">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a9ca8-385">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-385">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a9ca8-386">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="a9ca8-386">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9ca8-387">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-387">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a9ca8-388">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-388">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a9ca8-389">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-389">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a9ca8-390">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-390">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a9ca8-391">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-391">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a9ca8-392">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-392">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a9ca8-393">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-393">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a9ca8-394">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-394">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a9ca8-395">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-395">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9ca8-396">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-396">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-397">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-397">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-398">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-399">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a9ca8-399">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-400">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-400">State of the logical device.</span></span> <span data-ttu-id="a9ca8-401">Se questa proprietà non è applicabile al dispositivo logico, è necessario utilizzare il valore 5 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="a9ca8-401">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="a9ca8-402">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a9ca8-403">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-403">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9ca8-404">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-404">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a9ca8-405">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-405">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a9ca8-406">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-406">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a9ca8-407">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-407">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9ca8-408">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-408">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-409">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-411">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-411">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-412">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-412">The scoping system's creation class name.</span></span>

<span data-ttu-id="a9ca8-413">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ca8-414">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-414">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ca8-415">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9ca8-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ca8-417">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a9ca8-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a9ca8-418">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-418">The scoping system's name.</span></span>

<span data-ttu-id="a9ca8-419">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9ca8-420">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9ca8-420">Remarks</span></span>

<span data-ttu-id="a9ca8-421">La classe **CIM \_ AggregatePSExtent** è derivata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="a9ca8-421">The **CIM\_AggregatePSExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="a9ca8-422">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-422">WMI does not implement this class.</span></span>

<span data-ttu-id="a9ca8-423">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-423">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a9ca8-424">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a9ca8-424">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9ca8-425">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9ca8-425">Requirements</span></span>



| <span data-ttu-id="a9ca8-426">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9ca8-426">Requirement</span></span> | <span data-ttu-id="a9ca8-427">Valore</span><span class="sxs-lookup"><span data-stu-id="a9ca8-427">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ca8-428">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9ca8-428">Minimum supported client</span></span><br/> | <span data-ttu-id="a9ca8-429">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9ca8-429">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9ca8-430">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9ca8-430">Minimum supported server</span></span><br/> | <span data-ttu-id="a9ca8-431">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9ca8-431">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9ca8-432">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a9ca8-432">Namespace</span></span><br/>                | <span data-ttu-id="a9ca8-433">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a9ca8-433">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a9ca8-434">MOF</span><span class="sxs-lookup"><span data-stu-id="a9ca8-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9ca8-435"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9ca8-435"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9ca8-436">DLL</span><span class="sxs-lookup"><span data-stu-id="a9ca8-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9ca8-437"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9ca8-437"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9ca8-438">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9ca8-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ca8-439">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="a9ca8-439">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="a9ca8-440">Classi CIM</span><span class="sxs-lookup"><span data-stu-id="a9ca8-440">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

