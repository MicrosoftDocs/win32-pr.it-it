---
description: La \_ classe CIM DiscreteSensor presenta un set di valori stringa validi che possono essere segnalati. I valori vengono enumerati nella proprietà PossibleValues del sensore. Un sensore discreto ha sempre una lettura corrente corrispondente a uno dei valori enumerati.
ms.assetid: 58ab5b4d-ff8b-4981-8f09-c9a255635110
ms.tgt_platform: multiple
title: Classe CIM_DiscreteSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiscreteSensor
- CIM_DiscreteSensor.AcceptableValues
- CIM_DiscreteSensor.Availability
- CIM_DiscreteSensor.Caption
- CIM_DiscreteSensor.ConfigManagerErrorCode
- CIM_DiscreteSensor.ConfigManagerUserConfig
- CIM_DiscreteSensor.CreationClassName
- CIM_DiscreteSensor.CurrentReading
- CIM_DiscreteSensor.Description
- CIM_DiscreteSensor.DeviceID
- CIM_DiscreteSensor.ErrorCleared
- CIM_DiscreteSensor.ErrorDescription
- CIM_DiscreteSensor.InstallDate
- CIM_DiscreteSensor.LastErrorCode
- CIM_DiscreteSensor.Name
- CIM_DiscreteSensor.PNPDeviceID
- CIM_DiscreteSensor.PossibleValues
- CIM_DiscreteSensor.PowerManagementCapabilities
- CIM_DiscreteSensor.PowerManagementSupported
- CIM_DiscreteSensor.Status
- CIM_DiscreteSensor.StatusInfo
- CIM_DiscreteSensor.SystemCreationClassName
- CIM_DiscreteSensor.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5211aa8d840384eaf140c1afbeb2fa9c0680cb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523881"
---
# <a name="cim_discretesensor-class"></a><span data-ttu-id="ba03d-105">CIM \_ DiscreteSensor (classe)</span><span class="sxs-lookup"><span data-stu-id="ba03d-105">CIM\_DiscreteSensor class</span></span>

<span data-ttu-id="ba03d-106">La classe **CIM \_ DiscreteSensor** presenta un set di valori stringa validi che possono essere segnalati.</span><span class="sxs-lookup"><span data-stu-id="ba03d-106">The **CIM\_DiscreteSensor** class has a set of legal string values that it can report.</span></span> <span data-ttu-id="ba03d-107">I valori vengono enumerati nella proprietà **PossibleValues** del sensore.</span><span class="sxs-lookup"><span data-stu-id="ba03d-107">The values are enumerated in the sensor's **PossibleValues** property.</span></span> <span data-ttu-id="ba03d-108">Un sensore discreto ha sempre una lettura corrente corrispondente a uno dei valori enumerati.</span><span class="sxs-lookup"><span data-stu-id="ba03d-108">A discrete sensor always has a current reading that corresponds to one of the enumerated values.</span></span>

<span data-ttu-id="ba03d-109">Data l'aggiunta delle proprietà **CurrentState** e **PossibleStates** al [**\_ sensore CIM**](cim-sensor.md), la sottoclasse del sensore discreto non è più necessaria. Tuttavia, viene mantenuta per compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="ba03d-109">Given the addition of the **CurrentState** and **PossibleStates** properties to [**CIM\_Sensor**](cim-sensor.md), the discrete sensor subclass is no longer necessary; however, it is retained for backward compatibility.</span></span> <span data-ttu-id="ba03d-110">Le informazioni nelle proprietà **CurrentReading** e **PossibleValues** in genere hanno gli stessi valori e la stessa semantica delle proprietà **CurrentState** e **PossibleStates** , che vengono ereditate dal **\_ sensore CIM**.</span><span class="sxs-lookup"><span data-stu-id="ba03d-110">Information in the **CurrentReading** and **PossibleValues** properties typically has the same values and semantics as for the **CurrentState** and **PossibleStates** properties, which are inherited from **CIM\_Sensor**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba03d-111">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ba03d-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ba03d-112">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ba03d-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ba03d-113">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ba03d-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ba03d-114">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ba03d-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba03d-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba03d-115">Syntax</span></span>

``` syntax
[Abstract, UUID("{1BF00330-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_DiscreteSensor : CIM_Sensor
{
  string   AcceptableValues[];
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   CurrentReading;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  string   PossibleValues[];
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="ba03d-116">Members</span><span class="sxs-lookup"><span data-stu-id="ba03d-116">Members</span></span>

<span data-ttu-id="ba03d-117">La classe **CIM \_ DiscreteSensor** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ba03d-117">The **CIM\_DiscreteSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="ba03d-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="ba03d-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="ba03d-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba03d-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ba03d-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="ba03d-120">Methods</span></span>

<span data-ttu-id="ba03d-121">La classe **CIM \_ DiscreteSensor** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ba03d-121">The **CIM\_DiscreteSensor** class has these methods.</span></span>



| <span data-ttu-id="ba03d-122">Metodo</span><span class="sxs-lookup"><span data-stu-id="ba03d-122">Method</span></span>                                                                | <span data-ttu-id="ba03d-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba03d-123">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba03d-124">**Reset**</span><span class="sxs-lookup"><span data-stu-id="ba03d-124">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                 | <span data-ttu-id="ba03d-125">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ba03d-125">Requests a reset of the logical device.</span></span> <span data-ttu-id="ba03d-126">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="ba03d-126">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="ba03d-127">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ba03d-127">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-controller.md) | <span data-ttu-id="ba03d-128">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="ba03d-128">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="ba03d-129">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="ba03d-129">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ba03d-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba03d-130">Properties</span></span>

<span data-ttu-id="ba03d-131">La classe **CIM \_ DiscreteSensor** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ba03d-131">The **CIM\_DiscreteSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba03d-132">**AcceptableValues indica**</span><span class="sxs-lookup"><span data-stu-id="ba03d-132">**AcceptableValues**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-133">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ba03d-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-135">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ba03d-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-136">Le stringhe nella proprietà **PossibleValues** sono considerate accettabili, ovvero non sono errori.</span><span class="sxs-lookup"><span data-stu-id="ba03d-136">Strings in the **PossibleValues** property are considered acceptable (that is, they are not errors).</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-137">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="ba03d-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-138">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ba03d-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-140">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="ba03d-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-141">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba03d-141">Availability and status of the device.</span></span>

<span data-ttu-id="ba03d-142">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ba03d-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ba03d-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ba03d-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="ba03d-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="ba03d-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="ba03d-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="ba03d-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="ba03d-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="ba03d-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="ba03d-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ba03d-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="ba03d-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ba03d-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="ba03d-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="ba03d-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="ba03d-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="ba03d-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="ba03d-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ba03d-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="ba03d-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="ba03d-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="ba03d-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="ba03d-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="ba03d-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="ba03d-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="ba03d-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-156">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="ba03d-156">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ba03d-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="ba03d-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-158">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="ba03d-158">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ba03d-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="ba03d-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-160">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="ba03d-160">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ba03d-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="ba03d-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="ba03d-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="ba03d-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-163">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="ba03d-163">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ba03d-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="ba03d-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-165">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="ba03d-165">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="ba03d-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="ba03d-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-167">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="ba03d-167">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="ba03d-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="ba03d-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-169">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="ba03d-169">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="ba03d-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="ba03d-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-171">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="ba03d-171">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ba03d-172">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="ba03d-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba03d-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-175">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ba03d-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-176">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ba03d-176">Short textual description of the object.</span></span>

<span data-ttu-id="ba03d-177">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-178">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ba03d-178">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-179">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba03d-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-181">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ba03d-181">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-182">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ba03d-182">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="ba03d-183">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-183">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="ba03d-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="ba03d-185"> (0)</span><span class="sxs-lookup"><span data-stu-id="ba03d-185">(0)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-186">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="ba03d-186">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="ba03d-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="ba03d-188">(1)</span><span class="sxs-lookup"><span data-stu-id="ba03d-188">(1)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-189">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="ba03d-189">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ba03d-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="ba03d-191">(2)</span><span class="sxs-lookup"><span data-stu-id="ba03d-191">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="ba03d-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="ba03d-193">(3)</span><span class="sxs-lookup"><span data-stu-id="ba03d-193">(3)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-194">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="ba03d-194">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ba03d-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="ba03d-196">(4)</span><span class="sxs-lookup"><span data-stu-id="ba03d-196">(4)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-197">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="ba03d-197">Device is not working properly.</span></span> <span data-ttu-id="ba03d-198">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="ba03d-198">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="ba03d-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="ba03d-200">(5)</span><span class="sxs-lookup"><span data-stu-id="ba03d-200">(5)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-201">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="ba03d-201">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="ba03d-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="ba03d-203"> (6)</span><span class="sxs-lookup"><span data-stu-id="ba03d-203">(6)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-204">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="ba03d-204">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="ba03d-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="ba03d-206">(7)</span><span class="sxs-lookup"><span data-stu-id="ba03d-206">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="ba03d-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="ba03d-208">(8)</span><span class="sxs-lookup"><span data-stu-id="ba03d-208">(8)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-209">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="ba03d-209">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="ba03d-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="ba03d-211">(9)</span><span class="sxs-lookup"><span data-stu-id="ba03d-211">(9)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-212">Il dispositivo non funziona correttamente; il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba03d-212">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="ba03d-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="ba03d-214">(10)</span><span class="sxs-lookup"><span data-stu-id="ba03d-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-215">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba03d-215">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="ba03d-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="ba03d-217">(11)</span><span class="sxs-lookup"><span data-stu-id="ba03d-217">(11)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-218">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba03d-218">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="ba03d-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="ba03d-220">12</span><span class="sxs-lookup"><span data-stu-id="ba03d-220">(12)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-221">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="ba03d-221">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="ba03d-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="ba03d-223">(13)</span><span class="sxs-lookup"><span data-stu-id="ba03d-223">(13)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-224">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba03d-224">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="ba03d-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="ba03d-226">(14)</span><span class="sxs-lookup"><span data-stu-id="ba03d-226">(14)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-227">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="ba03d-227">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="ba03d-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="ba03d-229">(15)</span><span class="sxs-lookup"><span data-stu-id="ba03d-229">(15)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-230">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="ba03d-230">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="ba03d-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="ba03d-232">(16)</span><span class="sxs-lookup"><span data-stu-id="ba03d-232">(16)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-233">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba03d-233">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="ba03d-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="ba03d-235">(17)</span><span class="sxs-lookup"><span data-stu-id="ba03d-235">(17)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-236">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="ba03d-236">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ba03d-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="ba03d-238">(18)</span><span class="sxs-lookup"><span data-stu-id="ba03d-238">(18)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-239">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba03d-239">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="ba03d-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="ba03d-241">(19)</span><span class="sxs-lookup"><span data-stu-id="ba03d-241">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ba03d-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="ba03d-243">(20)</span><span class="sxs-lookup"><span data-stu-id="ba03d-243">(20)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-244">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="ba03d-244">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="ba03d-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="ba03d-246">(21)</span><span class="sxs-lookup"><span data-stu-id="ba03d-246">(21)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-247">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="ba03d-247">System failure.</span></span> <span data-ttu-id="ba03d-248">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="ba03d-248">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="ba03d-249">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba03d-249">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="ba03d-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="ba03d-251">(22)</span><span class="sxs-lookup"><span data-stu-id="ba03d-251">(22)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-252">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="ba03d-252">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="ba03d-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="ba03d-254">(23)</span><span class="sxs-lookup"><span data-stu-id="ba03d-254">(23)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-255">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="ba03d-255">System failure.</span></span> <span data-ttu-id="ba03d-256">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="ba03d-256">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="ba03d-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="ba03d-258">(24)</span><span class="sxs-lookup"><span data-stu-id="ba03d-258">(24)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-259">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="ba03d-259">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ba03d-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ba03d-261">(25)</span><span class="sxs-lookup"><span data-stu-id="ba03d-261">(25)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-262">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba03d-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ba03d-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ba03d-264">(26)</span><span class="sxs-lookup"><span data-stu-id="ba03d-264">(26)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-265">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba03d-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="ba03d-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="ba03d-267">(27)</span><span class="sxs-lookup"><span data-stu-id="ba03d-267">(27)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-268">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="ba03d-268">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="ba03d-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="ba03d-270">(28)</span><span class="sxs-lookup"><span data-stu-id="ba03d-270">(28)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-271">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="ba03d-271">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="ba03d-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="ba03d-273">(29)</span><span class="sxs-lookup"><span data-stu-id="ba03d-273">(29)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-274">Il dispositivo è disabilitato; il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="ba03d-274">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="ba03d-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="ba03d-276">(30)</span><span class="sxs-lookup"><span data-stu-id="ba03d-276">(30)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-277">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba03d-277">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ba03d-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ba03d-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="ba03d-279">31</span><span class="sxs-lookup"><span data-stu-id="ba03d-279">(31)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-280">Il dispositivo non funziona correttamente; Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="ba03d-280">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ba03d-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="ba03d-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-282">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ba03d-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-284">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ba03d-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-285">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ba03d-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="ba03d-286">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ba03d-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba03d-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-290">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ba03d-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-291">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="ba03d-291">Name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="ba03d-292">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="ba03d-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ba03d-293">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-294">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="ba03d-294">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-295">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba03d-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-297">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ba03d-297">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-298">Valore corrente indicato dal sensore.</span><span class="sxs-lookup"><span data-stu-id="ba03d-298">Current value indicated by the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-299">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ba03d-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba03d-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-302">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ba03d-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-303">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ba03d-303">Textual description of the object.</span></span>

<span data-ttu-id="ba03d-304">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ba03d-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-306">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba03d-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-308">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ba03d-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-309">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ba03d-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="ba03d-310">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="ba03d-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-312">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ba03d-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-314">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="ba03d-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="ba03d-315">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ba03d-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-317">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba03d-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-319">Stringa in formato libero che fornisce ulteriori informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="ba03d-319">Free-form string that supplies more information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="ba03d-320">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ba03d-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-322">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ba03d-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-324">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="ba03d-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-325">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ba03d-325">Date and time when the object was installed.</span></span> <span data-ttu-id="ba03d-326">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="ba03d-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ba03d-327">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-328">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ba03d-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-329">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba03d-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-331">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ba03d-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="ba03d-332">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-333">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ba03d-333">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-334">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba03d-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-336">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="ba03d-336">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-337">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="ba03d-337">Label by which the object is known.</span></span> <span data-ttu-id="ba03d-338">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="ba03d-338">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="ba03d-339">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-340">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="ba03d-340">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-341">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba03d-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-343">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ba03d-343">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-344">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ba03d-344">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="ba03d-345">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ba03d-346">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="ba03d-346">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-347">**PossibleValues**</span><span class="sxs-lookup"><span data-stu-id="ba03d-347">**PossibleValues**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-348">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ba03d-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-350">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ba03d-350">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-351">Enumera gli output di stringa dal sensore discreto.</span><span class="sxs-lookup"><span data-stu-id="ba03d-351">Enumerates the string outputs from the discrete sensor.</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-352">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ba03d-352">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-353">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ba03d-353">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-355">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ba03d-355">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="ba03d-356">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="ba03d-356">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ba03d-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ba03d-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="ba03d-358"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="ba03d-358"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ba03d-359"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="ba03d-359"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ba03d-360"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="ba03d-360"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-361">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="ba03d-361">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="ba03d-362"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="ba03d-362"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-363">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="ba03d-363">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="ba03d-364"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="ba03d-364"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-365">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="ba03d-365">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="ba03d-366">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="ba03d-366">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="ba03d-367">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="ba03d-367">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="ba03d-368"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="ba03d-368"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-369">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="ba03d-369">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="ba03d-370"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="ba03d-370"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ba03d-371">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="ba03d-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ba03d-372">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="ba03d-372">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-373">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ba03d-373">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-375">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="ba03d-375">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="ba03d-376">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="ba03d-376">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="ba03d-377">Questa proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="ba03d-377">This property does not indicate that power management features are currently enabled, or if enabled, what features are supported.</span></span> <span data-ttu-id="ba03d-378">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="ba03d-378">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="ba03d-379">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-380">**Status**</span><span class="sxs-lookup"><span data-stu-id="ba03d-380">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-381">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba03d-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-383">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="ba03d-383">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-384">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ba03d-384">String that indicates the current status of the object.</span></span> <span data-ttu-id="ba03d-385">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="ba03d-385">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="ba03d-386">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="ba03d-386">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="ba03d-387">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="ba03d-387">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="ba03d-388">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="ba03d-388">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ba03d-389">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="ba03d-389">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ba03d-390">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="ba03d-390">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ba03d-391">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-391">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ba03d-392">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ba03d-392">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ba03d-393">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ba03d-393">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ba03d-394">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="ba03d-394">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ba03d-395">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="ba03d-395">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ba03d-396">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="ba03d-396">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ba03d-397">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="ba03d-397">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ba03d-398">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="ba03d-398">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ba03d-399">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="ba03d-399">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ba03d-400">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="ba03d-400">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ba03d-401">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="ba03d-401">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ba03d-402">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="ba03d-402">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ba03d-403">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="ba03d-403">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ba03d-404">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="ba03d-404">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ba03d-405">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ba03d-405">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-406">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ba03d-406">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-408">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="ba03d-408">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-409">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ba03d-409">State of the logical device.</span></span> <span data-ttu-id="ba03d-410">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="ba03d-410">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="ba03d-411">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ba03d-412">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ba03d-412">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ba03d-413">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="ba03d-413">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ba03d-414">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="ba03d-414">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ba03d-415">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="ba03d-415">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ba03d-416">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="ba03d-416">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ba03d-417">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ba03d-417">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-418">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba03d-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-419">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-420">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ba03d-420">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-421">Proprietà **CreationClassName** del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="ba03d-421">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="ba03d-422">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-422">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba03d-423">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ba03d-423">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba03d-424">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba03d-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba03d-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba03d-426">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ba03d-426">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ba03d-427">Proprietà **Name** del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="ba03d-427">Scoping system's **Name** property.</span></span>

<span data-ttu-id="ba03d-428">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-428">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba03d-429">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba03d-429">Remarks</span></span>

<span data-ttu-id="ba03d-430">La classe **CIM \_ DiscreteSensor** è derivata dal [**\_ sensore CIM**](cim-sensor.md).</span><span class="sxs-lookup"><span data-stu-id="ba03d-430">The **CIM\_DiscreteSensor** class is derived from [**CIM\_Sensor**](cim-sensor.md).</span></span>

<span data-ttu-id="ba03d-431">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ba03d-431">WMI does not implement this class.</span></span>

<span data-ttu-id="ba03d-432">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ba03d-432">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ba03d-433">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ba03d-433">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba03d-434">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba03d-434">Requirements</span></span>



| <span data-ttu-id="ba03d-435">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba03d-435">Requirement</span></span> | <span data-ttu-id="ba03d-436">Valore</span><span class="sxs-lookup"><span data-stu-id="ba03d-436">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba03d-437">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba03d-437">Minimum supported client</span></span><br/> | <span data-ttu-id="ba03d-438">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba03d-438">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ba03d-439">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba03d-439">Minimum supported server</span></span><br/> | <span data-ttu-id="ba03d-440">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba03d-440">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ba03d-441">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ba03d-441">Namespace</span></span><br/>                | <span data-ttu-id="ba03d-442">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ba03d-442">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ba03d-443">MOF</span><span class="sxs-lookup"><span data-stu-id="ba03d-443">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba03d-444"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba03d-444"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba03d-445">DLL</span><span class="sxs-lookup"><span data-stu-id="ba03d-445">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba03d-446"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba03d-446"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba03d-447">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba03d-447">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba03d-448">**\_Sensore CIM**</span><span class="sxs-lookup"><span data-stu-id="ba03d-448">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

