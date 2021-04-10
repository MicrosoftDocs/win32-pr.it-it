---
description: La \_ classe CIM USBController rappresenta le funzionalità e la gestione di un controller USB.
ms.assetid: fa891db5-9995-4532-895f-bded8dd0bdac
ms.tgt_platform: multiple
title: Classe CIM_USBController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBController
- CIM_USBController.Availability
- CIM_USBController.Caption
- CIM_USBController.ConfigManagerErrorCode
- CIM_USBController.ConfigManagerUserConfig
- CIM_USBController.CreationClassName
- CIM_USBController.Description
- CIM_USBController.DeviceID
- CIM_USBController.ErrorCleared
- CIM_USBController.ErrorDescription
- CIM_USBController.InstallDate
- CIM_USBController.LastErrorCode
- CIM_USBController.Manufacturer
- CIM_USBController.MaxNumberControlled
- CIM_USBController.Name
- CIM_USBController.PNPDeviceID
- CIM_USBController.PowerManagementCapabilities
- CIM_USBController.PowerManagementSupported
- CIM_USBController.ProtocolSupported
- CIM_USBController.Status
- CIM_USBController.StatusInfo
- CIM_USBController.SystemCreationClassName
- CIM_USBController.SystemName
- CIM_USBController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4c636ae977dc0145b9e4b243c6903a687a525d15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225521"
---
# <a name="cim_usbcontroller-class"></a><span data-ttu-id="23df6-103">CIM \_ USBController (classe)</span><span class="sxs-lookup"><span data-stu-id="23df6-103">CIM\_USBController class</span></span>

<span data-ttu-id="23df6-104">La classe **CIM \_ USBController** rappresenta le funzionalità e la gestione di un controller USB.</span><span class="sxs-lookup"><span data-stu-id="23df6-104">The **CIM\_USBController** class represents the capabilities and management of a USB controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23df6-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="23df6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="23df6-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="23df6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="23df6-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="23df6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="23df6-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="23df6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="23df6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23df6-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B5B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_USBController : CIM_Controller
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

## <a name="members"></a><span data-ttu-id="23df6-110">Members</span><span class="sxs-lookup"><span data-stu-id="23df6-110">Members</span></span>

<span data-ttu-id="23df6-111">La classe **CIM \_ USBController** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="23df6-111">The **CIM\_USBController** class has these types of members:</span></span>

-   [<span data-ttu-id="23df6-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="23df6-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="23df6-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23df6-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="23df6-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="23df6-114">Methods</span></span>

<span data-ttu-id="23df6-115">La classe **CIM \_ USBController** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="23df6-115">The **CIM\_USBController** class has these methods.</span></span>



| <span data-ttu-id="23df6-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="23df6-116">Method</span></span>                                                                   | <span data-ttu-id="23df6-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23df6-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23df6-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="23df6-118">**Reset**</span></span>](reset-method-in-class-cim-usbcontroller.md)                 | <span data-ttu-id="23df6-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="23df6-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="23df6-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="23df6-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="23df6-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="23df6-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-usbcontroller.md) | <span data-ttu-id="23df6-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="23df6-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="23df6-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="23df6-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="23df6-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23df6-124">Properties</span></span>

<span data-ttu-id="23df6-125">La classe **CIM \_ USBController** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="23df6-125">The **CIM\_USBController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23df6-126">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="23df6-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23df6-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-129">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="23df6-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="23df6-130">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23df6-130">Availability and status of the device.</span></span>

<span data-ttu-id="23df6-131">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="23df6-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="23df6-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="23df6-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="23df6-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="23df6-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="23df6-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-135">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="23df6-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="23df6-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="23df6-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="23df6-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="23df6-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="23df6-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="23df6-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="23df6-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="23df6-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="23df6-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="23df6-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="23df6-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="23df6-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="23df6-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="23df6-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="23df6-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="23df6-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="23df6-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="23df6-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="23df6-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="23df6-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-146">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="23df6-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="23df6-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="23df6-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-148">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="23df6-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="23df6-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="23df6-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-150">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="23df6-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="23df6-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="23df6-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="23df6-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="23df6-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-153">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="23df6-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="23df6-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="23df6-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-155">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="23df6-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="23df6-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="23df6-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-157">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="23df6-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="23df6-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="23df6-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-159">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="23df6-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="23df6-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="23df6-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-161">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="23df6-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="23df6-162">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="23df6-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23df6-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-165">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="23df6-165">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="23df6-166">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23df6-166">Short textual description of the object.</span></span>

<span data-ttu-id="23df6-167">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="23df6-168">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="23df6-168">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-169">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="23df6-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-171">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="23df6-171">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="23df6-172">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="23df6-172">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="23df6-173">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-173">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="23df6-174"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="23df6-174"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="23df6-175"> (0)</span><span class="sxs-lookup"><span data-stu-id="23df6-175">(0)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-176">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="23df6-176">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="23df6-177"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="23df6-177"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="23df6-178">(1)</span><span class="sxs-lookup"><span data-stu-id="23df6-178">(1)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-179">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="23df6-179">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="23df6-180"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23df6-180"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="23df6-181">(2)</span><span class="sxs-lookup"><span data-stu-id="23df6-181">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="23df6-182"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="23df6-182"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="23df6-183">(3)</span><span class="sxs-lookup"><span data-stu-id="23df6-183">(3)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-184">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="23df6-184">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="23df6-185"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="23df6-185"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="23df6-186">(4)</span><span class="sxs-lookup"><span data-stu-id="23df6-186">(4)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-187">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="23df6-187">Device is not working properly.</span></span> <span data-ttu-id="23df6-188">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="23df6-188">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="23df6-189"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="23df6-189"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="23df6-190">(5)</span><span class="sxs-lookup"><span data-stu-id="23df6-190">(5)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-191">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="23df6-191">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="23df6-192"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="23df6-192"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="23df6-193"> (6)</span><span class="sxs-lookup"><span data-stu-id="23df6-193">(6)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-194">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="23df6-194">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="23df6-195"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="23df6-195"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="23df6-196">(7)</span><span class="sxs-lookup"><span data-stu-id="23df6-196">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="23df6-197"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="23df6-197"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="23df6-198">(8)</span><span class="sxs-lookup"><span data-stu-id="23df6-198">(8)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-199">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="23df6-199">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="23df6-200"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="23df6-200"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="23df6-201">(9)</span><span class="sxs-lookup"><span data-stu-id="23df6-201">(9)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-202">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="23df6-202">Device is not working properly.</span></span> <span data-ttu-id="23df6-203">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23df6-203">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="23df6-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23df6-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="23df6-205">(10)</span><span class="sxs-lookup"><span data-stu-id="23df6-205">(10)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-206">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23df6-206">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="23df6-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23df6-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="23df6-208">(11)</span><span class="sxs-lookup"><span data-stu-id="23df6-208">(11)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-209">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23df6-209">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="23df6-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="23df6-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="23df6-211">12</span><span class="sxs-lookup"><span data-stu-id="23df6-211">(12)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-212">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="23df6-212">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="23df6-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23df6-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="23df6-214">(13)</span><span class="sxs-lookup"><span data-stu-id="23df6-214">(13)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-215">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23df6-215">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="23df6-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="23df6-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="23df6-217">(14)</span><span class="sxs-lookup"><span data-stu-id="23df6-217">(14)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-218">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="23df6-218">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="23df6-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="23df6-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="23df6-220">(15)</span><span class="sxs-lookup"><span data-stu-id="23df6-220">(15)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-221">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="23df6-221">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="23df6-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23df6-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="23df6-223">(16)</span><span class="sxs-lookup"><span data-stu-id="23df6-223">(16)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-224">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23df6-224">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="23df6-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="23df6-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="23df6-226">(17)</span><span class="sxs-lookup"><span data-stu-id="23df6-226">(17)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-227">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="23df6-227">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="23df6-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23df6-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="23df6-229">(18)</span><span class="sxs-lookup"><span data-stu-id="23df6-229">(18)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-230">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23df6-230">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="23df6-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="23df6-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="23df6-232">(19)</span><span class="sxs-lookup"><span data-stu-id="23df6-232">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="23df6-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="23df6-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="23df6-234">(20)</span><span class="sxs-lookup"><span data-stu-id="23df6-234">(20)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-235">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="23df6-235">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="23df6-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23df6-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="23df6-237">(21)</span><span class="sxs-lookup"><span data-stu-id="23df6-237">(21)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-238">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="23df6-238">System failure.</span></span> <span data-ttu-id="23df6-239">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="23df6-239">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="23df6-240">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23df6-240">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="23df6-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="23df6-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="23df6-242">(22)</span><span class="sxs-lookup"><span data-stu-id="23df6-242">(22)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-243">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="23df6-243">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="23df6-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="23df6-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="23df6-245">(23)</span><span class="sxs-lookup"><span data-stu-id="23df6-245">(23)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-246">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="23df6-246">System failure.</span></span> <span data-ttu-id="23df6-247">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="23df6-247">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="23df6-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="23df6-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="23df6-249">(24)</span><span class="sxs-lookup"><span data-stu-id="23df6-249">(24)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-250">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="23df6-250">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="23df6-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23df6-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="23df6-252">(25)</span><span class="sxs-lookup"><span data-stu-id="23df6-252">(25)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-253">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23df6-253">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="23df6-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23df6-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="23df6-255">(26)</span><span class="sxs-lookup"><span data-stu-id="23df6-255">(26)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-256">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23df6-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="23df6-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="23df6-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="23df6-258">(27)</span><span class="sxs-lookup"><span data-stu-id="23df6-258">(27)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-259">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="23df6-259">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="23df6-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="23df6-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="23df6-261">(28)</span><span class="sxs-lookup"><span data-stu-id="23df6-261">(28)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-262">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="23df6-262">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="23df6-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="23df6-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="23df6-264">(29)</span><span class="sxs-lookup"><span data-stu-id="23df6-264">(29)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-265">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="23df6-265">Device is disabled.</span></span> <span data-ttu-id="23df6-266">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="23df6-266">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="23df6-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23df6-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="23df6-268">(30)</span><span class="sxs-lookup"><span data-stu-id="23df6-268">(30)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-269">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23df6-269">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="23df6-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="23df6-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="23df6-271">31</span><span class="sxs-lookup"><span data-stu-id="23df6-271">(31)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-272">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="23df6-272">Device is not working properly.</span></span> <span data-ttu-id="23df6-273">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="23df6-273">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="23df6-274">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="23df6-274">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-275">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="23df6-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-277">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="23df6-277">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="23df6-278">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="23df6-278">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="23df6-279">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-279">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23df6-280">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="23df6-280">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-281">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23df6-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-283">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="23df6-283">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="23df6-284">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="23df6-284">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="23df6-285">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="23df6-285">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="23df6-286">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23df6-287">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="23df6-287">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23df6-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-290">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="23df6-290">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="23df6-291">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23df6-291">Textual description of the object.</span></span>

<span data-ttu-id="23df6-292">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-292">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="23df6-293">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="23df6-293">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-294">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23df6-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-296">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="23df6-296">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="23df6-297">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="23df6-297">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="23df6-298">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23df6-299">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="23df6-299">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-300">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="23df6-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23df6-302">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="23df6-302">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="23df6-303">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23df6-304">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="23df6-304">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-305">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23df6-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23df6-307">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="23df6-307">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="23df6-308">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23df6-309">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="23df6-309">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-310">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="23df6-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-312">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="23df6-312">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="23df6-313">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23df6-313">Date and time the object was installed.</span></span> <span data-ttu-id="23df6-314">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="23df6-314">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="23df6-315">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-315">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="23df6-316">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="23df6-316">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-317">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="23df6-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23df6-319">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="23df6-319">Last error code reported by the logical device.</span></span>

<span data-ttu-id="23df6-320">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23df6-321">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="23df6-321">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-322">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23df6-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-324">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="23df6-324">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="23df6-325">Nome del produttore del controller USB.</span><span class="sxs-lookup"><span data-stu-id="23df6-325">Name of the USB controller manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="23df6-326">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="23df6-326">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-327">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="23df6-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-329">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="23df6-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="23df6-330">Numero massimo di entità indirizzabili direttamente supportate dal controller.</span><span class="sxs-lookup"><span data-stu-id="23df6-330">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="23df6-331">Se il numero è sconosciuto o illimitato, è necessario utilizzare il valore 0.</span><span class="sxs-lookup"><span data-stu-id="23df6-331">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="23df6-332">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-332">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="23df6-333">**Nome**</span><span class="sxs-lookup"><span data-stu-id="23df6-333">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-334">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23df6-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-336">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="23df6-336">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="23df6-337">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="23df6-337">Label by which the object is known.</span></span> <span data-ttu-id="23df6-338">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="23df6-338">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="23df6-339">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="23df6-340">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="23df6-340">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-341">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23df6-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-343">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="23df6-343">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="23df6-344">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="23df6-344">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="23df6-345">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="23df6-346">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="23df6-346">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="23df6-347">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="23df6-347">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-348">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23df6-348">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="23df6-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23df6-350">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="23df6-350">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="23df6-351">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="23df6-351">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="23df6-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="23df6-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="23df6-353"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="23df6-353"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="23df6-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="23df6-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="23df6-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="23df6-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-356">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="23df6-356">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="23df6-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="23df6-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-358">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="23df6-358">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="23df6-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="23df6-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-360">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="23df6-360">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="23df6-361">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="23df6-361">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="23df6-362">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="23df6-362">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="23df6-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="23df6-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-364">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="23df6-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="23df6-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="23df6-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="23df6-366">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="23df6-366">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="23df6-367">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="23df6-367">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-368">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="23df6-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23df6-370">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="23df6-370">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="23df6-371">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="23df6-371">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="23df6-372">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="23df6-372">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="23df6-373">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="23df6-373">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="23df6-374">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23df6-375">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="23df6-375">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-376">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23df6-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-378">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,2 "," MIF. \|Dischi DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="23df6-378">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="23df6-379">Protocollo usato dal controller per accedere ai dispositivi "controllati".</span><span class="sxs-lookup"><span data-stu-id="23df6-379">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="23df6-380">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-380">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="23df6-381">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="23df6-381">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="23df6-382">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="23df6-382">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="23df6-383">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="23df6-383">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="23df6-384">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="23df6-384">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="23df6-385">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="23df6-385">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="23df6-386">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="23df6-386">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="23df6-387">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="23df6-387">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="23df6-388">**Dischetto flessibile** (7)</span><span class="sxs-lookup"><span data-stu-id="23df6-388">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="23df6-389">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="23df6-389">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="23df6-390">**Interfaccia parallela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="23df6-390">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="23df6-391">**Protocollo di Fibre Channel SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="23df6-391">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="23df6-392">**Protocollo bus seriale SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="23df6-392">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="23df6-393">**Protocollo bus seriale SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="23df6-393">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="23df6-394">**Architettura di archiviazione seriale SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="23df6-394">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="23df6-395">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="23df6-395">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="23df6-396">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="23df6-396">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="23df6-397">**Bus seriale universale** (16)</span><span class="sxs-lookup"><span data-stu-id="23df6-397">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="23df6-398">**Protocollo parallelo** (17)</span><span class="sxs-lookup"><span data-stu-id="23df6-398">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="23df6-399">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="23df6-399">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="23df6-400">**Diagnostica** (19)</span><span class="sxs-lookup"><span data-stu-id="23df6-400">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="23df6-401">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="23df6-401">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="23df6-402">**Potenza** (21)</span><span class="sxs-lookup"><span data-stu-id="23df6-402">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="23df6-403">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="23df6-403">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="23df6-404">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="23df6-404">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="23df6-405">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="23df6-405">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="23df6-406">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="23df6-406">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="23df6-407">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="23df6-407">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="23df6-408">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="23df6-408">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="23df6-409">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="23df6-409">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="23df6-410">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="23df6-410">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="23df6-411">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="23df6-411">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="23df6-412">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="23df6-412">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="23df6-413">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="23df6-413">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="23df6-414">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="23df6-414">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="23df6-415">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="23df6-415">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="23df6-416">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="23df6-416">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="23df6-417">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="23df6-417">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="23df6-418">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="23df6-418">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="23df6-419">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="23df6-419">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="23df6-420">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="23df6-420">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="23df6-421">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="23df6-421">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="23df6-422">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="23df6-422">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="23df6-423">**ATA/IDE avanzato** (42)</span><span class="sxs-lookup"><span data-stu-id="23df6-423">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="23df6-424">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="23df6-424">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="23df6-425">**TWIRP (infrarossi bidirezionali)** (44)</span><span class="sxs-lookup"><span data-stu-id="23df6-425">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="23df6-426">**FIR (infrarossi veloci)** (45)</span><span class="sxs-lookup"><span data-stu-id="23df6-426">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="23df6-427">**Sir (Serial Infrared)** (46)</span><span class="sxs-lookup"><span data-stu-id="23df6-427">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="23df6-428">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="23df6-428">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="23df6-429">**Status**</span><span class="sxs-lookup"><span data-stu-id="23df6-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-430">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23df6-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-431">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-432">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="23df6-432">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="23df6-433">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23df6-433">Current status of the object.</span></span> <span data-ttu-id="23df6-434">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-434">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="23df6-435">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="23df6-435">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="23df6-436">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="23df6-436">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="23df6-437">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="23df6-437">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="23df6-438">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="23df6-438">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="23df6-439">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="23df6-439">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="23df6-440">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="23df6-440">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="23df6-441">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="23df6-441">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="23df6-442">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="23df6-442">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="23df6-443">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="23df6-443">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="23df6-444">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="23df6-444">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="23df6-445">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="23df6-445">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="23df6-446">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="23df6-446">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="23df6-447">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="23df6-447">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="23df6-448">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="23df6-448">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-449">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23df6-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-450">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-451">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="23df6-451">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="23df6-452">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="23df6-452">State of the logical device.</span></span> <span data-ttu-id="23df6-453">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="23df6-453">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="23df6-454">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-454">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="23df6-455">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="23df6-455">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="23df6-456">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="23df6-456">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="23df6-457">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="23df6-457">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="23df6-458">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="23df6-458">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="23df6-459">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="23df6-459">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="23df6-460">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="23df6-460">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-461">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23df6-461">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-462">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-463">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="23df6-463">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="23df6-464">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="23df6-464">Scoping system's creation class name.</span></span>

<span data-ttu-id="23df6-465">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-465">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23df6-466">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="23df6-466">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-467">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23df6-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-468">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23df6-469">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="23df6-469">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="23df6-470">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="23df6-470">Scoping system's name.</span></span>

<span data-ttu-id="23df6-471">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-471">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="23df6-472">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="23df6-472">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23df6-473">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="23df6-473">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="23df6-474">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23df6-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23df6-475">Data e ora dell'ultima reimpostazione del controller, ovvero il controller è stato spento o reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="23df6-475">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="23df6-476">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-476">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23df6-477">Commenti</span><span class="sxs-lookup"><span data-stu-id="23df6-477">Remarks</span></span>

<span data-ttu-id="23df6-478">La classe **CIM \_ USBController** è derivata dal [**\_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-478">The **CIM\_USBController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="23df6-479">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="23df6-479">WMI does not implement this class.</span></span> <span data-ttu-id="23df6-480">Per le classi WMI derivate da **CIM \_ USBController**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="23df6-480">For WMI classes derived from **CIM\_USBController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="23df6-481">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="23df6-481">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="23df6-482">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="23df6-482">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="23df6-483">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23df6-483">Requirements</span></span>



| <span data-ttu-id="23df6-484">Requisito</span><span class="sxs-lookup"><span data-stu-id="23df6-484">Requirement</span></span> | <span data-ttu-id="23df6-485">Valore</span><span class="sxs-lookup"><span data-stu-id="23df6-485">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23df6-486">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23df6-486">Minimum supported client</span></span><br/> | <span data-ttu-id="23df6-487">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23df6-487">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23df6-488">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23df6-488">Minimum supported server</span></span><br/> | <span data-ttu-id="23df6-489">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23df6-489">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23df6-490">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="23df6-490">Namespace</span></span><br/>                | <span data-ttu-id="23df6-491">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="23df6-491">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="23df6-492">MOF</span><span class="sxs-lookup"><span data-stu-id="23df6-492">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23df6-493"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23df6-493"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="23df6-494">DLL</span><span class="sxs-lookup"><span data-stu-id="23df6-494">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23df6-495"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23df6-495"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23df6-496">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23df6-496">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23df6-497">**\_Controller CIM**</span><span class="sxs-lookup"><span data-stu-id="23df6-497">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

