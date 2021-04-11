---
description: La \_ classe CIM HeatPipe rappresenta le funzionalità e la gestione di un dispositivo di raffreddamento con pipe di calore.
ms.assetid: 55cbf645-12d8-4f17-a894-43195d42de0e
ms.tgt_platform: multiple
title: Classe CIM_HeatPipe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HeatPipe
- CIM_HeatPipe.ActiveCooling
- CIM_HeatPipe.Availability
- CIM_HeatPipe.Caption
- CIM_HeatPipe.ConfigManagerErrorCode
- CIM_HeatPipe.ConfigManagerUserConfig
- CIM_HeatPipe.CreationClassName
- CIM_HeatPipe.Description
- CIM_HeatPipe.DeviceID
- CIM_HeatPipe.ErrorCleared
- CIM_HeatPipe.ErrorDescription
- CIM_HeatPipe.InstallDate
- CIM_HeatPipe.LastErrorCode
- CIM_HeatPipe.Name
- CIM_HeatPipe.PNPDeviceID
- CIM_HeatPipe.PowerManagementCapabilities
- CIM_HeatPipe.PowerManagementSupported
- CIM_HeatPipe.Status
- CIM_HeatPipe.StatusInfo
- CIM_HeatPipe.SystemCreationClassName
- CIM_HeatPipe.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9502509e5a48f4d2f407fddbb6b57766b5f7bffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342231"
---
# <a name="cim_heatpipe-class"></a><span data-ttu-id="2bd2e-103">CIM \_ HeatPipe (classe)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-103">CIM\_HeatPipe class</span></span>

<span data-ttu-id="2bd2e-104">La classe **CIM \_ HeatPipe** rappresenta le funzionalità e la gestione di un dispositivo di raffreddamento con pipe di calore.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-104">The **CIM\_HeatPipe** class represents the capabilities and management of a heat pipe cooling device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2bd2e-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2bd2e-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2bd2e-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2bd2e-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bd2e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2bd2e-109">Syntax</span></span>

``` syntax
[UUID("{FE5D55E0-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_HeatPipe : CIM_CoolingDevice
{
  boolean  ActiveCooling;
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
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="2bd2e-110">Members</span><span class="sxs-lookup"><span data-stu-id="2bd2e-110">Members</span></span>

<span data-ttu-id="2bd2e-111">La classe **CIM \_ HeatPipe** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2bd2e-111">The **CIM\_HeatPipe** class has these types of members:</span></span>

-   [<span data-ttu-id="2bd2e-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="2bd2e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2bd2e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2bd2e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2bd2e-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="2bd2e-114">Methods</span></span>

<span data-ttu-id="2bd2e-115">La classe **CIM \_ HeatPipe** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-115">The **CIM\_HeatPipe** class has these methods.</span></span>



| <span data-ttu-id="2bd2e-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="2bd2e-116">Method</span></span>                                                              | <span data-ttu-id="2bd2e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bd2e-117">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2bd2e-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-118">**Reset**</span></span>](reset-method-in-class-cim-heatpipe.md)                 | <span data-ttu-id="2bd2e-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="2bd2e-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="2bd2e-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-heatpipe.md) | <span data-ttu-id="2bd2e-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="2bd2e-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2bd2e-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2bd2e-124">Properties</span></span>

<span data-ttu-id="2bd2e-125">La classe **CIM \_ HeatPipe** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-125">The **CIM\_HeatPipe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2bd2e-126">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-126">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-127">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-129">Se **true**, il dispositivo di raffreddamento fornisce il raffreddamento attivo (anziché passivo).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-129">If **TRUE**, the cooling device provides active (as opposed to passive) cooling.</span></span>

<span data-ttu-id="2bd2e-130">Questa proprietà viene ereditata da [**CIM \_ CoolingDevice**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-130">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bd2e-131">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-132">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-134">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-135">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-135">Availability and status of the device.</span></span>

<span data-ttu-id="2bd2e-136">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2bd2e-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2bd2e-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2bd2e-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2bd2e-140"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-140"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2bd2e-141"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-141"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2bd2e-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2bd2e-143"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="2bd2e-143"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2bd2e-144"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="2bd2e-144"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2bd2e-145"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-145"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2bd2e-146"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-146"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2bd2e-147"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-147"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2bd2e-148"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-148"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2bd2e-149"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-149"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-150">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-150">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2bd2e-151"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-151"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-152">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-152">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2bd2e-153"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-153"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-154">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-154">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2bd2e-155"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-155"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2bd2e-156"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-156"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-157">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-157">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2bd2e-158"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-158"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-159">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-159">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2bd2e-160"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-160"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-161">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-161">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2bd2e-162"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-162"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-163">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-163">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2bd2e-164"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-164"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-165">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-165">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2bd2e-166">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-166">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-169">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-169">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-170">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-170">Short textual description of the object.</span></span>

<span data-ttu-id="2bd2e-171">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-171">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bd2e-172">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-172">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-173">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-175">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-175">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-176">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-176">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="2bd2e-177">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-177">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2bd2e-178"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-178"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="2bd2e-179"> (0)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-179">(0)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-180">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-180">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2bd2e-181"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-181"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="2bd2e-182">(1)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-182">(1)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-183">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-183">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2bd2e-184"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-184"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2bd2e-185">(2)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-185">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2bd2e-186"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-186"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2bd2e-187">(3)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-187">(3)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-188">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-188">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2bd2e-189"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-189"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2bd2e-190">(4)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-190">(4)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-191">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-191">Device is not working properly.</span></span> <span data-ttu-id="2bd2e-192">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-192">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2bd2e-193"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-193"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2bd2e-194">(5)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-194">(5)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-195">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-195">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2bd2e-196"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-196"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2bd2e-197"> (6)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-197">(6)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-198">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-198">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2bd2e-199"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-199"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="2bd2e-200">(7)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-200">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2bd2e-201"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-201"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2bd2e-202">(8)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-202">(8)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-203">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-203">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2bd2e-204"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-204"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2bd2e-205">(9)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-205">(9)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-206">Il dispositivo non funziona correttamente; il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-206">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2bd2e-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="2bd2e-208">(10)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-208">(10)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-209">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-209">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2bd2e-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="2bd2e-211">(11)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-211">(11)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-212">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-212">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2bd2e-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2bd2e-214">12</span><span class="sxs-lookup"><span data-stu-id="2bd2e-214">(12)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-215">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-215">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2bd2e-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2bd2e-217">(13)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-217">(13)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-218">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-218">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2bd2e-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2bd2e-220">(14)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-220">(14)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-221">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-221">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2bd2e-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2bd2e-223">(15)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-223">(15)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-224">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-224">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2bd2e-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2bd2e-226">(16)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-227">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-227">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2bd2e-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2bd2e-229">(17)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-229">(17)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-230">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-230">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2bd2e-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2bd2e-232">(18)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-232">(18)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-233">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-233">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2bd2e-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="2bd2e-235">(19)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2bd2e-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="2bd2e-237">(20)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-237">(20)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-238">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-238">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2bd2e-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2bd2e-240">(21)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-240">(21)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-241">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-241">System failure.</span></span> <span data-ttu-id="2bd2e-242">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-242">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="2bd2e-243">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-243">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2bd2e-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="2bd2e-245">(22)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-245">(22)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-246">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-246">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2bd2e-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2bd2e-248">(23)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-248">(23)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-249">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-249">System failure.</span></span> <span data-ttu-id="2bd2e-250">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-250">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2bd2e-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2bd2e-252">(24)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-252">(24)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-253">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-253">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2bd2e-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2bd2e-255">(25)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-255">(25)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-256">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2bd2e-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2bd2e-258">(26)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-258">(26)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-259">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2bd2e-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2bd2e-261">(27)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-261">(27)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-262">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-262">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2bd2e-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2bd2e-264">(28)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-264">(28)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-265">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-265">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2bd2e-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2bd2e-267">(29)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-267">(29)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-268">Il dispositivo è disabilitato; il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-268">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2bd2e-269"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-269"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2bd2e-270">(30)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-270">(30)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-271">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-271">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2bd2e-272"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-272"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2bd2e-273">31</span><span class="sxs-lookup"><span data-stu-id="2bd2e-273">(31)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-274">Il dispositivo non funziona correttamente; Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-274">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2bd2e-275">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-275">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-276">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-277">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-278">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-278">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-279">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-279">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2bd2e-280">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-280">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bd2e-281">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-281">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-282">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-284">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-284">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-285">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-285">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2bd2e-286">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-286">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2bd2e-287">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bd2e-288">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-288">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-289">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-291">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-291">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-292">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-292">Textual description of the object.</span></span>

<span data-ttu-id="2bd2e-293">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-293">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bd2e-294">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-294">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-295">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-297">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-298">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-298">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="2bd2e-299">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bd2e-300">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-300">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-301">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-303">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-303">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="2bd2e-304">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bd2e-305">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-305">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-306">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-308">Stringa in formato libero che fornisce ulteriori informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-308">Free-form string that supplies more information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="2bd2e-309">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bd2e-310">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-310">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-311">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-313">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-314">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-314">Date and time the object was installed.</span></span> <span data-ttu-id="2bd2e-315">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-315">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2bd2e-316">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bd2e-317">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-317">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-318">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-320">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-320">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2bd2e-321">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bd2e-322">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-322">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-323">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-325">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-325">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-326">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-326">Label by which the object is known.</span></span> <span data-ttu-id="2bd2e-327">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-327">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2bd2e-328">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bd2e-329">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-329">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-330">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-332">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-332">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-333">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-333">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="2bd2e-334">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2bd2e-335">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="2bd2e-335">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="2bd2e-336">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-336">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-337">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-339">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-339">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="2bd2e-340">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-340">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2bd2e-341"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-341"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2bd2e-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-343">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-343">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2bd2e-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2bd2e-345"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-345"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-346">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-346">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2bd2e-347"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-347"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-348">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-348">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2bd2e-349"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-349"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-350">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-350">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="2bd2e-351">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-351">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="2bd2e-352">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-352">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2bd2e-353"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-353"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-354">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-354">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2bd2e-355"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-355"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2bd2e-356">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-356">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2bd2e-357">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-357">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-358">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-358">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-360">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-360">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="2bd2e-361">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2bd2e-361">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2bd2e-362">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-362">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="2bd2e-363">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2bd2e-363">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="2bd2e-364">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bd2e-365">**Status**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-366">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-368">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-368">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-369">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-369">Current status of the object.</span></span> <span data-ttu-id="2bd2e-370">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-370">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2bd2e-371">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2bd2e-371">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2bd2e-372">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-372">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2bd2e-373">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-373">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2bd2e-374">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="2bd2e-374">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2bd2e-375">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-375">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2bd2e-376">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-376">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2bd2e-377">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-377">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2bd2e-378">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-378">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2bd2e-379">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-379">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2bd2e-380">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-380">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2bd2e-381">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-381">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2bd2e-382">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-382">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2bd2e-383">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-383">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2bd2e-384">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-384">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-385">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-385">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-386">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-387">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2bd2e-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-388">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-388">State of the logical device.</span></span> <span data-ttu-id="2bd2e-389">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-389">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="2bd2e-390">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2bd2e-391">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-391">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2bd2e-392">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-392">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2bd2e-393">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-393">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2bd2e-394">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-394">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2bd2e-395">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-395">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2bd2e-396">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-396">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-397">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-398">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-399">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-399">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-400">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-400">Scoping system's creation class name.</span></span>

<span data-ttu-id="2bd2e-401">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-401">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bd2e-402">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-402">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd2e-403">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bd2e-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd2e-405">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bd2e-405">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bd2e-406">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-406">Scoping system's name.</span></span>

<span data-ttu-id="2bd2e-407">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-407">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bd2e-408">Commenti</span><span class="sxs-lookup"><span data-stu-id="2bd2e-408">Remarks</span></span>

<span data-ttu-id="2bd2e-409">La classe **CIM \_ HeatPipe** è derivata da [**CIM \_ CoolingDevice**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-409">The **CIM\_HeatPipe** class is derived from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

<span data-ttu-id="2bd2e-410">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-410">WMI does not implement this class.</span></span> <span data-ttu-id="2bd2e-411">Per le classi derivate da **CIM \_ HeatPipe**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2bd2e-411">For classes derived from **CIM\_HeatPipe**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2bd2e-412">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-412">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2bd2e-413">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="2bd2e-413">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bd2e-414">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bd2e-414">Requirements</span></span>



| <span data-ttu-id="2bd2e-415">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bd2e-415">Requirement</span></span> | <span data-ttu-id="2bd2e-416">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd2e-416">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd2e-417">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bd2e-417">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd2e-418">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bd2e-418">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2bd2e-419">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bd2e-419">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd2e-420">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2bd2e-420">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2bd2e-421">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2bd2e-421">Namespace</span></span><br/>                | <span data-ttu-id="2bd2e-422">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2bd2e-422">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2bd2e-423">MOF</span><span class="sxs-lookup"><span data-stu-id="2bd2e-423">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bd2e-424"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2bd2e-424"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2bd2e-425">DLL</span><span class="sxs-lookup"><span data-stu-id="2bd2e-425">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bd2e-426"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bd2e-426"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bd2e-427">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2bd2e-427">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bd2e-428">**\_COOLINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2bd2e-428">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> </dl>

 

