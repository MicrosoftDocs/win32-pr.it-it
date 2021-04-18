---
description: La \_ classe CIM CoolingDevice rappresenta le funzionalità e la gestione dei dispositivi di raffreddamento.
ms.assetid: ac0f0df4-c174-4306-9325-eaa316ee820a
ms.tgt_platform: multiple
title: Classe CIM_CoolingDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CoolingDevice
- CIM_CoolingDevice.Caption
- CIM_CoolingDevice.Description
- CIM_CoolingDevice.InstallDate
- CIM_CoolingDevice.Name
- CIM_CoolingDevice.Status
- CIM_CoolingDevice.Availability
- CIM_CoolingDevice.ConfigManagerErrorCode
- CIM_CoolingDevice.ConfigManagerUserConfig
- CIM_CoolingDevice.CreationClassName
- CIM_CoolingDevice.DeviceID
- CIM_CoolingDevice.PowerManagementCapabilities
- CIM_CoolingDevice.ErrorCleared
- CIM_CoolingDevice.ErrorDescription
- CIM_CoolingDevice.LastErrorCode
- CIM_CoolingDevice.PNPDeviceID
- CIM_CoolingDevice.PowerManagementSupported
- CIM_CoolingDevice.StatusInfo
- CIM_CoolingDevice.SystemCreationClassName
- CIM_CoolingDevice.SystemName
- CIM_CoolingDevice.ActiveCooling
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f6c480e910cf72a319856942fda28d2139d0a6ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304782"
---
# <a name="cim_coolingdevice-class"></a><span data-ttu-id="23ab4-103">CIM \_ CoolingDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="23ab4-103">CIM\_CoolingDevice class</span></span>

<span data-ttu-id="23ab4-104">La classe **CIM \_ CoolingDevice** rappresenta le funzionalità e la gestione dei dispositivi di raffreddamento.</span><span class="sxs-lookup"><span data-stu-id="23ab4-104">The **CIM\_CoolingDevice** class represents the capabilities and management of cooling devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23ab4-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="23ab4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="23ab4-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="23ab4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="23ab4-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="23ab4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="23ab4-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="23ab4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="23ab4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23ab4-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979A-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_CoolingDevice : CIM_LogicalDevice
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
  boolean  ActiveCooling;
};
```

## <a name="members"></a><span data-ttu-id="23ab4-110">Members</span><span class="sxs-lookup"><span data-stu-id="23ab4-110">Members</span></span>

<span data-ttu-id="23ab4-111">La classe **CIM \_ CoolingDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="23ab4-111">The **CIM\_CoolingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="23ab4-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="23ab4-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="23ab4-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23ab4-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="23ab4-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="23ab4-114">Methods</span></span>

<span data-ttu-id="23ab4-115">La classe **CIM \_ CoolingDevice** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="23ab4-115">The **CIM\_CoolingDevice** class has these methods.</span></span>



| <span data-ttu-id="23ab4-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="23ab4-116">Method</span></span>                                                                   | <span data-ttu-id="23ab4-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23ab4-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23ab4-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="23ab4-118">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                    | <span data-ttu-id="23ab4-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="23ab4-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="23ab4-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="23ab4-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="23ab4-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="23ab4-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-coolingdevice.md) | <span data-ttu-id="23ab4-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="23ab4-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="23ab4-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="23ab4-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="23ab4-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23ab4-124">Properties</span></span>

<span data-ttu-id="23ab4-125">La classe **CIM \_ CoolingDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="23ab4-125">The **CIM\_CoolingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23ab4-126">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="23ab4-126">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-127">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="23ab4-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-129">Se **true**, il dispositivo di raffreddamento fornisce il raffreddamento attivo (anziché passivo).</span><span class="sxs-lookup"><span data-stu-id="23ab4-129">If **TRUE**, the cooling device provides active (as opposed to passive) cooling.</span></span>

</dd> <dt>

<span data-ttu-id="23ab4-130">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="23ab4-130">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-131">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23ab4-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-133">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="23ab4-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-134">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23ab4-134">Availability and status of the device.</span></span>

<span data-ttu-id="23ab4-135">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-135">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="23ab4-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="23ab4-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="23ab4-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="23ab4-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="23ab4-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="23ab4-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="23ab4-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="23ab4-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="23ab4-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="23ab4-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="23ab4-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="23ab4-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="23ab4-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="23ab4-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="23ab4-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="23ab4-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="23ab4-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="23ab4-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="23ab4-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="23ab4-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="23ab4-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="23ab4-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="23ab4-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="23ab4-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="23ab4-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="23ab4-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-149">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="23ab4-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="23ab4-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="23ab4-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-151">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="23ab4-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="23ab4-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="23ab4-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-153">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="23ab4-153">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="23ab4-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="23ab4-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="23ab4-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="23ab4-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-156">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="23ab4-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="23ab4-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="23ab4-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-158">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="23ab4-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="23ab4-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="23ab4-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-160">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="23ab4-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="23ab4-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="23ab4-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-162">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="23ab4-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="23ab4-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="23ab4-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-164">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="23ab4-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="23ab4-165">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="23ab4-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23ab4-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-168">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="23ab4-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-169">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23ab4-169">A short textual description of the object.</span></span>

<span data-ttu-id="23ab4-170">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="23ab4-171">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="23ab4-171">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-172">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="23ab4-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-174">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="23ab4-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-175">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="23ab4-175">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="23ab4-176">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-176">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="23ab4-177">**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-177">**This device is working properly.**</span></span> <span data-ttu-id="23ab4-178"> (0)</span><span class="sxs-lookup"><span data-stu-id="23ab4-178">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="23ab4-179">**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-179">**This device is not configured correctly.**</span></span> <span data-ttu-id="23ab4-180">(1)</span><span class="sxs-lookup"><span data-stu-id="23ab4-180">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="23ab4-181">**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-181">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="23ab4-182">(2)</span><span class="sxs-lookup"><span data-stu-id="23ab4-182">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="23ab4-183">**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-183">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="23ab4-184">(3)</span><span class="sxs-lookup"><span data-stu-id="23ab4-184">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="23ab4-185">**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-185">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="23ab4-186">(4)</span><span class="sxs-lookup"><span data-stu-id="23ab4-186">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="23ab4-187">**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-187">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="23ab4-188">(5)</span><span class="sxs-lookup"><span data-stu-id="23ab4-188">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="23ab4-189">**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-189">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="23ab4-190"> (6)</span><span class="sxs-lookup"><span data-stu-id="23ab4-190">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="23ab4-191">**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-191">**Cannot filter.**</span></span> <span data-ttu-id="23ab4-192">(7)</span><span class="sxs-lookup"><span data-stu-id="23ab4-192">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="23ab4-193">**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-193">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="23ab4-194">(8)</span><span class="sxs-lookup"><span data-stu-id="23ab4-194">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="23ab4-195">**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-195">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="23ab4-196">(9)</span><span class="sxs-lookup"><span data-stu-id="23ab4-196">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="23ab4-197">**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-197">**This device cannot start.**</span></span> <span data-ttu-id="23ab4-198">(10)</span><span class="sxs-lookup"><span data-stu-id="23ab4-198">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="23ab4-199">**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-199">**This device failed.**</span></span> <span data-ttu-id="23ab4-200">(11)</span><span class="sxs-lookup"><span data-stu-id="23ab4-200">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="23ab4-201">**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-201">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="23ab4-202">12</span><span class="sxs-lookup"><span data-stu-id="23ab4-202">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="23ab4-203">**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-203">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="23ab4-204">(13)</span><span class="sxs-lookup"><span data-stu-id="23ab4-204">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="23ab4-205">**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-205">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="23ab4-206">(14)</span><span class="sxs-lookup"><span data-stu-id="23ab4-206">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="23ab4-207">**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-207">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="23ab4-208">(15)</span><span class="sxs-lookup"><span data-stu-id="23ab4-208">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="23ab4-209">**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-209">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="23ab4-210">(16)</span><span class="sxs-lookup"><span data-stu-id="23ab4-210">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="23ab4-211">**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-211">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="23ab4-212">(17)</span><span class="sxs-lookup"><span data-stu-id="23ab4-212">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="23ab4-213">**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-213">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="23ab4-214">(18)</span><span class="sxs-lookup"><span data-stu-id="23ab4-214">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="23ab4-215">**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-215">**Failure using the VxD loader.**</span></span> <span data-ttu-id="23ab4-216">(19)</span><span class="sxs-lookup"><span data-stu-id="23ab4-216">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="23ab4-217">**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-217">**Your registry might be corrupted.**</span></span> <span data-ttu-id="23ab4-218">(20)</span><span class="sxs-lookup"><span data-stu-id="23ab4-218">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="23ab4-219">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-219">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="23ab4-220">(21)</span><span class="sxs-lookup"><span data-stu-id="23ab4-220">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="23ab4-221">**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-221">**This device is disabled.**</span></span> <span data-ttu-id="23ab4-222">(22)</span><span class="sxs-lookup"><span data-stu-id="23ab4-222">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="23ab4-223">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-223">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="23ab4-224">(23)</span><span class="sxs-lookup"><span data-stu-id="23ab4-224">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="23ab4-225">**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-225">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="23ab4-226">(24)</span><span class="sxs-lookup"><span data-stu-id="23ab4-226">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="23ab4-227">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-227">**Windows is still setting up this device.**</span></span> <span data-ttu-id="23ab4-228">(25)</span><span class="sxs-lookup"><span data-stu-id="23ab4-228">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="23ab4-229">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-229">**Windows is still setting up this device.**</span></span> <span data-ttu-id="23ab4-230">(26)</span><span class="sxs-lookup"><span data-stu-id="23ab4-230">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="23ab4-231">**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-231">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="23ab4-232">(27)</span><span class="sxs-lookup"><span data-stu-id="23ab4-232">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="23ab4-233">**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-233">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="23ab4-234">(28)</span><span class="sxs-lookup"><span data-stu-id="23ab4-234">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="23ab4-235">**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-235">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="23ab4-236">(29)</span><span class="sxs-lookup"><span data-stu-id="23ab4-236">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="23ab4-237">**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-237">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="23ab4-238">(30)</span><span class="sxs-lookup"><span data-stu-id="23ab4-238">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="23ab4-239">**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23ab4-239">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="23ab4-240">31</span><span class="sxs-lookup"><span data-stu-id="23ab4-240">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="23ab4-241">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="23ab4-241">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-242">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="23ab4-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-244">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="23ab4-244">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-245">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="23ab4-245">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="23ab4-246">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-246">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23ab4-247">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="23ab4-247">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-248">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23ab4-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-250">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="23ab4-250">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-251">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="23ab4-251">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="23ab4-252">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="23ab4-252">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="23ab4-253">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-253">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23ab4-254">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="23ab4-254">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-255">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23ab4-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-257">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="23ab4-257">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-258">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23ab4-258">A textual description of the object.</span></span>

<span data-ttu-id="23ab4-259">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="23ab4-260">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="23ab4-260">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23ab4-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-263">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="23ab4-263">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-264">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="23ab4-264">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="23ab4-265">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-265">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23ab4-266">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="23ab4-266">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-267">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="23ab4-267">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-269">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="23ab4-269">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="23ab4-270">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23ab4-271">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="23ab4-271">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-272">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23ab4-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-273">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-274">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="23ab4-274">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="23ab4-275">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-275">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23ab4-276">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="23ab4-276">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-277">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="23ab4-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-279">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="23ab4-279">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-280">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="23ab4-280">Indicates when the object was installed.</span></span> <span data-ttu-id="23ab4-281">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="23ab4-281">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="23ab4-282">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-282">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="23ab4-283">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="23ab4-283">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-284">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="23ab4-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-286">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="23ab4-286">Last error code reported by the logical device.</span></span>

<span data-ttu-id="23ab4-287">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23ab4-288">**Nome**</span><span class="sxs-lookup"><span data-stu-id="23ab4-288">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-289">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23ab4-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-291">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="23ab4-291">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-292">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="23ab4-292">Label by which the object is known.</span></span> <span data-ttu-id="23ab4-293">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="23ab4-293">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="23ab4-294">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-294">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="23ab4-295">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="23ab4-295">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-296">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23ab4-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-298">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="23ab4-298">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-299">Indica l'identificatore del dispositivo Plug and Play Win32 del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="23ab4-299">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="23ab4-300">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="23ab4-300">Example: "\*PNP030b"</span></span>

<span data-ttu-id="23ab4-301">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23ab4-302">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="23ab4-302">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-303">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23ab4-303">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-305">Indica le funzionalità specifiche relative al risparmio di energia del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="23ab4-305">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="23ab4-306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="23ab4-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="23ab4-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-308">Le capacità relative al risparmio di energia sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="23ab4-308">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="23ab4-309"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="23ab4-309"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-310">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23ab4-310">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="23ab4-311"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="23ab4-311"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-312">Le capacità correlate all'alimentazione sono state disabilitate.</span><span class="sxs-lookup"><span data-stu-id="23ab4-312">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="23ab4-313"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="23ab4-313"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-314">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="23ab4-314">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="23ab4-315"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="23ab4-315"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-316">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="23ab4-316">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="23ab4-317"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="23ab4-317"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-318">Il metodo **SetPowerState** è supportato.</span><span class="sxs-lookup"><span data-stu-id="23ab4-318">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="23ab4-319">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="23ab4-319">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="23ab4-320">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="23ab4-320">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="23ab4-321"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="23ab4-321"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-322">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").</span><span class="sxs-lookup"><span data-stu-id="23ab4-322">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="23ab4-323"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="23ab4-323"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="23ab4-324">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e il parametro *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="23ab4-324">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="23ab4-325">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="23ab4-325">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-326">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="23ab4-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-328">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="23ab4-328">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="23ab4-329">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="23ab4-329">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="23ab4-330">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="23ab4-330">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="23ab4-331">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="23ab4-331">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="23ab4-332">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23ab4-333">**Status**</span><span class="sxs-lookup"><span data-stu-id="23ab4-333">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-334">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23ab4-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-336">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="23ab4-336">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-337">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23ab4-337">String that indicates the current status of the object.</span></span> <span data-ttu-id="23ab4-338">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="23ab4-338">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="23ab4-339">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="23ab4-339">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="23ab4-340">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="23ab4-340">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="23ab4-341">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="23ab4-341">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="23ab4-342">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="23ab4-342">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="23ab4-343">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="23ab4-343">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="23ab4-344">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="23ab4-345">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="23ab4-345">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="23ab4-346">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="23ab4-346">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="23ab4-347">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="23ab4-347">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="23ab4-348">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="23ab4-348">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="23ab4-349">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="23ab4-349">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="23ab4-350">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="23ab4-350">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="23ab4-351">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="23ab4-351">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="23ab4-352">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="23ab4-352">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="23ab4-353">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="23ab4-353">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="23ab4-354">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="23ab4-354">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="23ab4-355">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="23ab4-355">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="23ab4-356">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="23ab4-356">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="23ab4-357">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="23ab4-357">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="23ab4-358">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="23ab4-358">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-359">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23ab4-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-360">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-361">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="23ab4-361">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-362">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="23ab4-362">State of the logical device.</span></span> <span data-ttu-id="23ab4-363">Se questa proprietà non è applicabile al dispositivo logico, è necessario utilizzare il valore 5 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="23ab4-363">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="23ab4-364">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="23ab4-365">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="23ab4-365">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="23ab4-366">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="23ab4-366">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="23ab4-367">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="23ab4-367">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="23ab4-368">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="23ab4-368">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="23ab4-369">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="23ab4-369">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="23ab4-370">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="23ab4-370">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-371">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23ab4-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-373">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="23ab4-373">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-374">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="23ab4-374">The scoping system's creation class name.</span></span>

<span data-ttu-id="23ab4-375">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23ab4-376">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="23ab4-376">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23ab4-377">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23ab4-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-378">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23ab4-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23ab4-379">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="23ab4-379">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="23ab4-380">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="23ab4-380">The scoping system's name.</span></span>

<span data-ttu-id="23ab4-381">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23ab4-382">Commenti</span><span class="sxs-lookup"><span data-stu-id="23ab4-382">Remarks</span></span>

<span data-ttu-id="23ab4-383">La classe **CIM \_ CoolingDevice** è derivata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-383">The **CIM\_CoolingDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="23ab4-384">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="23ab4-384">WMI does not implement this class.</span></span> <span data-ttu-id="23ab4-385">Per le classi derivate da **CIM \_ CoolingDevice**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="23ab4-385">For classes derived from **CIM\_CoolingDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="23ab4-386">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="23ab4-386">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="23ab4-387">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="23ab4-387">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="23ab4-388">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23ab4-388">Requirements</span></span>



| <span data-ttu-id="23ab4-389">Requisito</span><span class="sxs-lookup"><span data-stu-id="23ab4-389">Requirement</span></span> | <span data-ttu-id="23ab4-390">Valore</span><span class="sxs-lookup"><span data-stu-id="23ab4-390">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23ab4-391">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23ab4-391">Minimum supported client</span></span><br/> | <span data-ttu-id="23ab4-392">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23ab4-392">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23ab4-393">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23ab4-393">Minimum supported server</span></span><br/> | <span data-ttu-id="23ab4-394">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23ab4-394">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23ab4-395">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="23ab4-395">Namespace</span></span><br/>                | <span data-ttu-id="23ab4-396">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="23ab4-396">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="23ab4-397">MOF</span><span class="sxs-lookup"><span data-stu-id="23ab4-397">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23ab4-398"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23ab4-398"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="23ab4-399">DLL</span><span class="sxs-lookup"><span data-stu-id="23ab4-399">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23ab4-400"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23ab4-400"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23ab4-401">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23ab4-401">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23ab4-402">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="23ab4-402">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

