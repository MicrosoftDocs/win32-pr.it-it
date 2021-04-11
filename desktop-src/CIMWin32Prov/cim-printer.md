---
description: La \_ classe CIM Printer rappresenta le funzionalità e la gestione del dispositivo logico Printer.
ms.assetid: e41ff580-0202-4d3f-8d78-4705d5fb41b3
ms.tgt_platform: multiple
title: Classe CIM_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Printer
- CIM_Printer.Availability
- CIM_Printer.AvailableJobSheets
- CIM_Printer.Capabilities
- CIM_Printer.CapabilityDescriptions
- CIM_Printer.Caption
- CIM_Printer.CharSetsSupported
- CIM_Printer.ConfigManagerErrorCode
- CIM_Printer.ConfigManagerUserConfig
- CIM_Printer.CreationClassName
- CIM_Printer.CurrentCapabilities
- CIM_Printer.CurrentCharSet
- CIM_Printer.CurrentLanguage
- CIM_Printer.CurrentMimeType
- CIM_Printer.CurrentNaturalLanguage
- CIM_Printer.CurrentPaperType
- CIM_Printer.DefaultCapabilities
- CIM_Printer.DefaultCopies
- CIM_Printer.DefaultLanguage
- CIM_Printer.DefaultMimeType
- CIM_Printer.DefaultNumberUp
- CIM_Printer.DefaultPaperType
- CIM_Printer.Description
- CIM_Printer.DetectedErrorState
- CIM_Printer.DeviceID
- CIM_Printer.ErrorCleared
- CIM_Printer.ErrorDescription
- CIM_Printer.ErrorInformation
- CIM_Printer.HorizontalResolution
- CIM_Printer.InstallDate
- CIM_Printer.JobCountSinceLastReset
- CIM_Printer.LanguagesSupported
- CIM_Printer.LastErrorCode
- CIM_Printer.MarkingTechnology
- CIM_Printer.MaxCopies
- CIM_Printer.MaxNumberUp
- CIM_Printer.MaxSizeSupported
- CIM_Printer.MimeTypesSupported
- CIM_Printer.Name
- CIM_Printer.NaturalLanguagesSupported
- CIM_Printer.PaperSizesSupported
- CIM_Printer.PaperTypesAvailable
- CIM_Printer.PNPDeviceID
- CIM_Printer.PowerManagementCapabilities
- CIM_Printer.PowerManagementSupported
- CIM_Printer.PrinterStatus
- CIM_Printer.Status
- CIM_Printer.StatusInfo
- CIM_Printer.SystemCreationClassName
- CIM_Printer.SystemName
- CIM_Printer.TimeOfLastReset
- CIM_Printer.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c673d6c58e6235e782a718b3b258a15790046eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127658"
---
# <a name="cim_printer-class"></a><span data-ttu-id="a943d-103">\_Classe stampante CIM</span><span class="sxs-lookup"><span data-stu-id="a943d-103">CIM\_Printer class</span></span>

<span data-ttu-id="a943d-104">La classe **CIM \_ Printer** rappresenta le funzionalità e la gestione del dispositivo logico Printer.</span><span class="sxs-lookup"><span data-stu-id="a943d-104">The **CIM\_Printer** class represents the capabilities and management of the printer logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a943d-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a943d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a943d-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a943d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a943d-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a943d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a943d-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a943d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a943d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a943d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Printer : CIM_LogicalDevice
{
  uint16   Availability;
  string   AvailableJobSheets[];
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PrinterStatus;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="a943d-110">Members</span><span class="sxs-lookup"><span data-stu-id="a943d-110">Members</span></span>

<span data-ttu-id="a943d-111">La classe **CIM \_ Printer** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a943d-111">The **CIM\_Printer** class has these types of members:</span></span>

-   [<span data-ttu-id="a943d-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="a943d-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="a943d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a943d-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a943d-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="a943d-114">Methods</span></span>

<span data-ttu-id="a943d-115">Per la classe **CIM \_ Printer** sono disponibili questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a943d-115">The **CIM\_Printer** class has these methods.</span></span>



| <span data-ttu-id="a943d-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="a943d-116">Method</span></span>                                                             | <span data-ttu-id="a943d-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a943d-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a943d-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="a943d-118">**Reset**</span></span>](reset-method-in-class-cim-printer.md)                 | <span data-ttu-id="a943d-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a943d-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="a943d-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="a943d-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="a943d-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a943d-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-printer.md) | <span data-ttu-id="a943d-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="a943d-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="a943d-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="a943d-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a943d-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a943d-124">Properties</span></span>

<span data-ttu-id="a943d-125">La **classe \_ Printer CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a943d-125">The **CIM\_Printer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a943d-126">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="a943d-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a943d-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-129">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="a943d-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-130">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a943d-130">Availability and status of the device.</span></span>

<span data-ttu-id="a943d-131">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a943d-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a943d-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a943d-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a943d-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a943d-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="a943d-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-135">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="a943d-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a943d-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="a943d-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a943d-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="a943d-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a943d-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="a943d-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a943d-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="a943d-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a943d-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="a943d-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a943d-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="a943d-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a943d-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="a943d-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a943d-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="a943d-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a943d-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="a943d-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a943d-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="a943d-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-146">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="a943d-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a943d-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="a943d-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-148">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="a943d-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a943d-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="a943d-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-150">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="a943d-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a943d-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="a943d-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a943d-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="a943d-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-153">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="a943d-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a943d-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="a943d-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-155">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="a943d-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a943d-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="a943d-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-157">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="a943d-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a943d-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="a943d-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-159">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="a943d-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a943d-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="a943d-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-161">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="a943d-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a943d-162">**AvailableJobSheets**</span><span class="sxs-lookup"><span data-stu-id="a943d-162">**AvailableJobSheets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-163">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="a943d-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a943d-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-165">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. RequiredJobSheets")</span><span class="sxs-lookup"><span data-stu-id="a943d-165">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.RequiredJobSheets")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-166">Vengono descritti tutti i fogli di processo disponibili sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="a943d-166">Describes all of the job sheets that are available on the printer.</span></span> <span data-ttu-id="a943d-167">Questo può essere usato anche per descrivere il banner che può essere fornito da una stampante all'inizio di ogni processo oppure può descrivere altre opzioni specificate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a943d-167">This can also be used to describe the banner that a printer might provide at the beginning of each job, or can describe other user specified options.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-168">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="a943d-168">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-169">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a943d-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a943d-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-171">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**. CapabilityDescriptions "," CIM \_ PrintJob. finishing "," CIM \_ printservice. Capabilities ")</span><span class="sxs-lookup"><span data-stu-id="a943d-171">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.CapabilityDescriptions", "CIM\_PrintJob.Finishing", "CIM\_PrintService.Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-172">Funzionalità della stampante.</span><span class="sxs-lookup"><span data-stu-id="a943d-172">Printer capabilities.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a943d-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a943d-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a943d-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a943d-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="a943d-175"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Stampa a colori** (2)</span><span class="sxs-lookup"><span data-stu-id="a943d-175"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="a943d-176"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Stampa duplex** (3)</span><span class="sxs-lookup"><span data-stu-id="a943d-176"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="a943d-177"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copie** (4)</span><span class="sxs-lookup"><span data-stu-id="a943d-177"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="a943d-178"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Regole di confronto** (5)</span><span class="sxs-lookup"><span data-stu-id="a943d-178"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="a943d-179"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Graffatura** (6)</span><span class="sxs-lookup"><span data-stu-id="a943d-179"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="a943d-180"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Stampa trasparenza** (7)</span><span class="sxs-lookup"><span data-stu-id="a943d-180"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="a943d-181"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span><span class="sxs-lookup"><span data-stu-id="a943d-181"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="a943d-182"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Copertura** (9)</span><span class="sxs-lookup"><span data-stu-id="a943d-182"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="a943d-183"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Binding** (10)</span><span class="sxs-lookup"><span data-stu-id="a943d-183"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="a943d-184"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Stampa in bianco e nero** (11)</span><span class="sxs-lookup"><span data-stu-id="a943d-184"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="a943d-185"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un lato** (12)</span><span class="sxs-lookup"><span data-stu-id="a943d-185"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-186">Lato singolo</span><span class="sxs-lookup"><span data-stu-id="a943d-186">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="a943d-187"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bordo lungo due lati** (13)</span><span class="sxs-lookup"><span data-stu-id="a943d-187"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-188">Bordo lungo lato due</span><span class="sxs-lookup"><span data-stu-id="a943d-188">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="a943d-189"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bordo corto a due lati** (14)</span><span class="sxs-lookup"><span data-stu-id="a943d-189"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-190">Bordo corto bilaterale</span><span class="sxs-lookup"><span data-stu-id="a943d-190">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="a943d-191"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Verticale** (15)</span><span class="sxs-lookup"><span data-stu-id="a943d-191"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="a943d-192"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Orizzontale** (16)</span><span class="sxs-lookup"><span data-stu-id="a943d-192"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="a943d-193"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Verticale inverso** (17)</span><span class="sxs-lookup"><span data-stu-id="a943d-193"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="a943d-194"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Orizzontale inverso** (18)</span><span class="sxs-lookup"><span data-stu-id="a943d-194"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="a943d-195"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualità elevata** (19)</span><span class="sxs-lookup"><span data-stu-id="a943d-195"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-196">Qualità elevata</span><span class="sxs-lookup"><span data-stu-id="a943d-196">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="a943d-197"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Normale qualità** (20)</span><span class="sxs-lookup"><span data-stu-id="a943d-197"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-198">Qualità normale</span><span class="sxs-lookup"><span data-stu-id="a943d-198">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="a943d-199"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualità bassa** (21)</span><span class="sxs-lookup"><span data-stu-id="a943d-199"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-200">Qualità bassa</span><span class="sxs-lookup"><span data-stu-id="a943d-200">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a943d-201">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a943d-201">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-202">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="a943d-202">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a943d-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-204">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="a943d-204">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-205">Stringhe in formato libero che forniscono spiegazioni dettagliate per tutte le funzionalità della stampante indicate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="a943d-205">Free-form strings that provide detailed explanations for any of the printer features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="a943d-206">Ogni voce di questa matrice è correlata alla voce nella matrice delle **funzionalità** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="a943d-206">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="a943d-207">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a943d-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-210">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a943d-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-211">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a943d-211">Short textual description of the object.</span></span>

<span data-ttu-id="a943d-212">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-212">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a943d-213">**CharSetsSupported**</span><span class="sxs-lookup"><span data-stu-id="a943d-213">**CharSetsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-214">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="a943d-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a943d-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-216">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. charset"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtLocalizationCharacterSet ")</span><span class="sxs-lookup"><span data-stu-id="a943d-216">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.CharSet"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtLocalizationCharacterSet")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-217">Set di caratteri disponibili per l'output del testo correlato alla gestione della stampante.</span><span class="sxs-lookup"><span data-stu-id="a943d-217">Available character sets for the output of text related to managing the printer.</span></span> <span data-ttu-id="a943d-218">Le stringhe fornite in questa proprietà devono essere conformi alla semantica e alla sintassi specificate dalla sezione 4.1.2 ("charset parametro") in RFC 2046 (MIME Part 2) e contenute nel registro di sistema del set di caratteri IANA.</span><span class="sxs-lookup"><span data-stu-id="a943d-218">Strings provided in this property should conform to the semantics and syntax specified by section 4.1.2 ("Charset parameter") in RFC 2046 (MIME Part 2), and contained in the IANA character-set registry.</span></span> <span data-ttu-id="a943d-219">Gli esempi includono "UTF-8", "US-ASCII" e "ISO-8859-1".</span><span class="sxs-lookup"><span data-stu-id="a943d-219">Examples include "utf-8", "us-ascii", and "iso-8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="a943d-220">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a943d-220">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-221">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a943d-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-223">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a943d-223">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-224">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a943d-224">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a943d-225">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-225">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a943d-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="a943d-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="a943d-227"> (0)</span><span class="sxs-lookup"><span data-stu-id="a943d-227">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-228">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="a943d-228">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a943d-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="a943d-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="a943d-230">(1)</span><span class="sxs-lookup"><span data-stu-id="a943d-230">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-231">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="a943d-231">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a943d-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a943d-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a943d-233">(2)</span><span class="sxs-lookup"><span data-stu-id="a943d-233">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a943d-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="a943d-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a943d-235">(3)</span><span class="sxs-lookup"><span data-stu-id="a943d-235">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-236">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="a943d-236">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a943d-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="a943d-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a943d-238">(4)</span><span class="sxs-lookup"><span data-stu-id="a943d-238">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-239">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="a943d-239">Device is not working properly.</span></span> <span data-ttu-id="a943d-240">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="a943d-240">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a943d-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="a943d-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a943d-242">(5)</span><span class="sxs-lookup"><span data-stu-id="a943d-242">(5)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-243">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="a943d-243">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a943d-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="a943d-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a943d-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="a943d-245">(6)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-246">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="a943d-246">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a943d-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="a943d-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="a943d-248">(7)</span><span class="sxs-lookup"><span data-stu-id="a943d-248">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a943d-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="a943d-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a943d-250">(8)</span><span class="sxs-lookup"><span data-stu-id="a943d-250">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-251">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="a943d-251">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a943d-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="a943d-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a943d-253">(9)</span><span class="sxs-lookup"><span data-stu-id="a943d-253">(9)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-254">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="a943d-254">Device is not working properly.</span></span> <span data-ttu-id="a943d-255">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a943d-255">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a943d-256"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a943d-256"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="a943d-257">(10)</span><span class="sxs-lookup"><span data-stu-id="a943d-257">(10)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-258">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a943d-258">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a943d-259"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a943d-259"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="a943d-260">(11)</span><span class="sxs-lookup"><span data-stu-id="a943d-260">(11)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-261">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a943d-261">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a943d-262"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="a943d-262"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a943d-263">12</span><span class="sxs-lookup"><span data-stu-id="a943d-263">(12)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-264">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="a943d-264">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a943d-265"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a943d-265"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a943d-266">(13)</span><span class="sxs-lookup"><span data-stu-id="a943d-266">(13)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-267">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a943d-267">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a943d-268"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="a943d-268"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a943d-269">(14)</span><span class="sxs-lookup"><span data-stu-id="a943d-269">(14)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-270">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="a943d-270">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a943d-271"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="a943d-271"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a943d-272">(15)</span><span class="sxs-lookup"><span data-stu-id="a943d-272">(15)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-273">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="a943d-273">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a943d-274"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a943d-274"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a943d-275">(16)</span><span class="sxs-lookup"><span data-stu-id="a943d-275">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-276">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a943d-276">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a943d-277"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="a943d-277"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a943d-278">(17)</span><span class="sxs-lookup"><span data-stu-id="a943d-278">(17)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-279">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="a943d-279">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a943d-280"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a943d-280"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a943d-281">(18)</span><span class="sxs-lookup"><span data-stu-id="a943d-281">(18)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-282">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a943d-282">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a943d-283"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="a943d-283"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="a943d-284">(19)</span><span class="sxs-lookup"><span data-stu-id="a943d-284">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a943d-285"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="a943d-285"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="a943d-286">(20)</span><span class="sxs-lookup"><span data-stu-id="a943d-286">(20)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-287">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="a943d-287">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a943d-288"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a943d-288"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a943d-289">(21)</span><span class="sxs-lookup"><span data-stu-id="a943d-289">(21)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-290">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="a943d-290">System failure.</span></span> <span data-ttu-id="a943d-291">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="a943d-291">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="a943d-292">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a943d-292">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a943d-293"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="a943d-293"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="a943d-294">(22)</span><span class="sxs-lookup"><span data-stu-id="a943d-294">(22)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-295">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="a943d-295">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a943d-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="a943d-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a943d-297">(23)</span><span class="sxs-lookup"><span data-stu-id="a943d-297">(23)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-298">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="a943d-298">System failure.</span></span> <span data-ttu-id="a943d-299">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="a943d-299">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a943d-300"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="a943d-300"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a943d-301">(24)</span><span class="sxs-lookup"><span data-stu-id="a943d-301">(24)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-302">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="a943d-302">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a943d-303"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a943d-303"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a943d-304">(25)</span><span class="sxs-lookup"><span data-stu-id="a943d-304">(25)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-305">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a943d-305">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a943d-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a943d-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a943d-307">(26)</span><span class="sxs-lookup"><span data-stu-id="a943d-307">(26)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-308">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a943d-308">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a943d-309"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="a943d-309"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a943d-310">(27)</span><span class="sxs-lookup"><span data-stu-id="a943d-310">(27)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-311">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="a943d-311">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a943d-312"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="a943d-312"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a943d-313">(28)</span><span class="sxs-lookup"><span data-stu-id="a943d-313">(28)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-314">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="a943d-314">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a943d-315"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="a943d-315"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a943d-316">(29)</span><span class="sxs-lookup"><span data-stu-id="a943d-316">(29)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-317">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="a943d-317">Device is disabled.</span></span> <span data-ttu-id="a943d-318">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="a943d-318">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a943d-319"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a943d-319"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a943d-320">(30)</span><span class="sxs-lookup"><span data-stu-id="a943d-320">(30)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-321">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a943d-321">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a943d-322"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a943d-322"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a943d-323">31</span><span class="sxs-lookup"><span data-stu-id="a943d-323">(31)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-324">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="a943d-324">Device is not working properly.</span></span> <span data-ttu-id="a943d-325">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="a943d-325">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a943d-326">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="a943d-326">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-327">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a943d-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-329">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a943d-329">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-330">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a943d-330">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a943d-331">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a943d-332">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a943d-332">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-333">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-335">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a943d-335">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a943d-336">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="a943d-336">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a943d-337">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a943d-337">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a943d-338">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a943d-339">**CurrentCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a943d-339">**CurrentCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-340">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a943d-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a943d-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-342">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="a943d-342">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-343">Finiture e altre funzionalità della stampante attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="a943d-343">Finishings and other capabilities of the printer that are currently in use.</span></span> <span data-ttu-id="a943d-344">Ogni voce in questa proprietà deve essere elencata anche nella matrice delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="a943d-344">Each entry in this property should also be listed in the **Capabilities** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a943d-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a943d-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a943d-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a943d-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="a943d-347"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Stampa a colori** (2)</span><span class="sxs-lookup"><span data-stu-id="a943d-347"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="a943d-348"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Stampa duplex** (3)</span><span class="sxs-lookup"><span data-stu-id="a943d-348"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="a943d-349"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copie** (4)</span><span class="sxs-lookup"><span data-stu-id="a943d-349"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="a943d-350"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Regole di confronto** (5)</span><span class="sxs-lookup"><span data-stu-id="a943d-350"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="a943d-351"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Graffatura** (6)</span><span class="sxs-lookup"><span data-stu-id="a943d-351"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="a943d-352"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Stampa trasparenza** (7)</span><span class="sxs-lookup"><span data-stu-id="a943d-352"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="a943d-353"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span><span class="sxs-lookup"><span data-stu-id="a943d-353"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="a943d-354"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Copertura** (9)</span><span class="sxs-lookup"><span data-stu-id="a943d-354"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="a943d-355"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Binding** (10)</span><span class="sxs-lookup"><span data-stu-id="a943d-355"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="a943d-356"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Stampa in bianco e nero** (11)</span><span class="sxs-lookup"><span data-stu-id="a943d-356"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="a943d-357"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un lato** (12)</span><span class="sxs-lookup"><span data-stu-id="a943d-357"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-358">Lato singolo</span><span class="sxs-lookup"><span data-stu-id="a943d-358">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="a943d-359"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bordo lungo due lati** (13)</span><span class="sxs-lookup"><span data-stu-id="a943d-359"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-360">Bordo lungo lato due</span><span class="sxs-lookup"><span data-stu-id="a943d-360">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="a943d-361"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bordo corto a due lati** (14)</span><span class="sxs-lookup"><span data-stu-id="a943d-361"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-362">Bordo corto bilaterale</span><span class="sxs-lookup"><span data-stu-id="a943d-362">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="a943d-363"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Verticale** (15)</span><span class="sxs-lookup"><span data-stu-id="a943d-363"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="a943d-364"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Orizzontale** (16)</span><span class="sxs-lookup"><span data-stu-id="a943d-364"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="a943d-365"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Verticale inverso** (17)</span><span class="sxs-lookup"><span data-stu-id="a943d-365"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="a943d-366"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Orizzontale inverso** (18)</span><span class="sxs-lookup"><span data-stu-id="a943d-366"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="a943d-367"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualità elevata** (19)</span><span class="sxs-lookup"><span data-stu-id="a943d-367"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-368">Qualità elevata</span><span class="sxs-lookup"><span data-stu-id="a943d-368">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="a943d-369"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Normale qualità** (20)</span><span class="sxs-lookup"><span data-stu-id="a943d-369"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-370">Qualità normale</span><span class="sxs-lookup"><span data-stu-id="a943d-370">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="a943d-371"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualità bassa** (21)</span><span class="sxs-lookup"><span data-stu-id="a943d-371"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-372">Qualità bassa</span><span class="sxs-lookup"><span data-stu-id="a943d-372">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a943d-373">**CurrentCharSet**</span><span class="sxs-lookup"><span data-stu-id="a943d-373">**CurrentCharSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-374">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-376">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**CharSetsSupported**")</span><span class="sxs-lookup"><span data-stu-id="a943d-376">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**CharSetsSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-377">Set di caratteri corrente utilizzato per l'output del testo relativo alla gestione della stampante.</span><span class="sxs-lookup"><span data-stu-id="a943d-377">Current character set used for the output of text relating to management of the printer.</span></span> <span data-ttu-id="a943d-378">Il set di caratteri descritto da questa proprietà deve essere elencato anche nella proprietà **CharsetsSupported** .</span><span class="sxs-lookup"><span data-stu-id="a943d-378">The character set described by this property should also be listed in the **CharsetsSupported** property.</span></span> <span data-ttu-id="a943d-379">La stringa specificata da questa proprietà deve essere conforme alla semantica e alla sintassi specificate dalla sezione 4.1.2 ("charset parametro") in RFC 2046 (MIME Part 2) e contenuta nel registro di sistema del set di caratteri IANA.</span><span class="sxs-lookup"><span data-stu-id="a943d-379">The string specified by this property should conform to the semantics and syntax specified by section 4.1.2 ("Charset parameter") in RFC 2046 (MIME Part 2), and contained in the IANA character-set registry.</span></span> <span data-ttu-id="a943d-380">Gli esempi includono "UTF-8", "US-ASCII" e "ISO-8859-1".</span><span class="sxs-lookup"><span data-stu-id="a943d-380">Examples include "utf-8", "us-ascii", and "iso-8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="a943d-381">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="a943d-381">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-382">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a943d-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-384">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**. LanguagesSupported "," CIM \_ Printer. CurrentMimeType ")</span><span class="sxs-lookup"><span data-stu-id="a943d-384">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_Printer.CurrentMimeType")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-385">Lingua corrente della stampante in uso; la lingua deve essere elencata anche nella proprietà **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="a943d-385">Current printer language being used; the language should also be listed in the **LanguagesSupported** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a943d-386">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a943d-386">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a943d-387">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a943d-387">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="a943d-388">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="a943d-388">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="a943d-389">**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="a943d-389">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="a943d-390">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="a943d-390">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="a943d-391">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="a943d-391">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="a943d-392">**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="a943d-392">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="a943d-393">**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="a943d-393">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="a943d-394">**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="a943d-394">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="a943d-395">**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="a943d-395">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="a943d-396">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="a943d-396">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="a943d-397">**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="a943d-397">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="a943d-398">**Interstampa** (13)</span><span class="sxs-lookup"><span data-stu-id="a943d-398">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="a943d-399">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="a943d-399">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="a943d-400">**Dati riga** (15)</span><span class="sxs-lookup"><span data-stu-id="a943d-400">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="a943d-401">**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="a943d-401">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="a943d-402">**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="a943d-402">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="a943d-403">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="a943d-403">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="a943d-404">**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="a943d-404">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="a943d-405">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="a943d-405">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="a943d-406">**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="a943d-406">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="a943d-407">**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="a943d-407">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="a943d-408">**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="a943d-408">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="a943d-409">**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="a943d-409">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="a943d-410">**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="a943d-410">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="a943d-411">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="a943d-411">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="a943d-412">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="a943d-412">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="a943d-413">**Quic** (28)</span><span class="sxs-lookup"><span data-stu-id="a943d-413">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="a943d-414">**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="a943d-414">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="a943d-415">**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="a943d-415">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="a943d-416">**Testo semplice** (31)</span><span class="sxs-lookup"><span data-stu-id="a943d-416">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="a943d-417">**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="a943d-417">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="a943d-418">**Documento** (33)</span><span class="sxs-lookup"><span data-stu-id="a943d-418">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="a943d-419">**impressione** (34)</span><span class="sxs-lookup"><span data-stu-id="a943d-419">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="a943d-420">**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="a943d-420">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="a943d-421">**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="a943d-421">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="a943d-422">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="a943d-422">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="a943d-423">**Automatico** (38)</span><span class="sxs-lookup"><span data-stu-id="a943d-423">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="a943d-424">**Pagine** (39)</span><span class="sxs-lookup"><span data-stu-id="a943d-424">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="a943d-425">**Lip** (40)</span><span class="sxs-lookup"><span data-stu-id="a943d-425">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="a943d-426">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="a943d-426">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="a943d-427">**Diagnostica** (42)</span><span class="sxs-lookup"><span data-stu-id="a943d-427">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="a943d-428">**Capsal** (43)</span><span class="sxs-lookup"><span data-stu-id="a943d-428">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="a943d-429">**Escl** (44)</span><span class="sxs-lookup"><span data-stu-id="a943d-429">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="a943d-430">**LCD** (45)</span><span class="sxs-lookup"><span data-stu-id="a943d-430">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="a943d-431">**XES** (46)</span><span class="sxs-lookup"><span data-stu-id="a943d-431">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="a943d-432">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="a943d-432">**MIME** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a943d-433">**CurrentMimeType**</span><span class="sxs-lookup"><span data-stu-id="a943d-433">**CurrentMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-434">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-435">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-436">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**CurrentLanguage**")</span><span class="sxs-lookup"><span data-stu-id="a943d-436">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**CurrentLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-437">Tipo MIME attualmente utilizzato dalla stampante quando la proprietà **CurrentLanguage** è impostata per indicare che un tipo MIME è in uso.</span><span class="sxs-lookup"><span data-stu-id="a943d-437">Mime type currently in use by the printer when the **CurrentLanguage** property is set to indicate that a mime type is in use.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-438">**CurrentNaturalLanguage**</span><span class="sxs-lookup"><span data-stu-id="a943d-438">**CurrentNaturalLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-439">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-440">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-441">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**NaturalLanguagesSupported**")</span><span class="sxs-lookup"><span data-stu-id="a943d-441">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**NaturalLanguagesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-442">Lingua corrente utilizzata dalla stampante per la gestione.</span><span class="sxs-lookup"><span data-stu-id="a943d-442">Current language in use by the printer for management.</span></span> <span data-ttu-id="a943d-443">La lingua elencata qui deve essere elencata anche in **NaturalLanguagesSupported**.</span><span class="sxs-lookup"><span data-stu-id="a943d-443">The language listed here should also be listed in **NaturalLanguagesSupported**.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-444">**CurrentPaperType**</span><span class="sxs-lookup"><span data-stu-id="a943d-444">**CurrentPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-445">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-446">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-447">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="a943d-447">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-448">Tipo di carta attualmente utilizzato dalla stampante.</span><span class="sxs-lookup"><span data-stu-id="a943d-448">Paper type currently in use by the printer.</span></span> <span data-ttu-id="a943d-449">La stringa deve essere espressa nel formato specificato dall'applicazione di stampa documenti ISO/IEC 10175, anch ' essa riepilogata nell'Appendice C di RFC 1759 (Printer MIB).</span><span class="sxs-lookup"><span data-stu-id="a943d-449">The string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

</dd> <dt>

<span data-ttu-id="a943d-450">**DefaultCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a943d-450">**DefaultCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-451">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a943d-451">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a943d-452">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-453">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="a943d-453">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-454">Finiture predefinite e altre funzionalità della stampante.</span><span class="sxs-lookup"><span data-stu-id="a943d-454">Default finishings and other capabilities of the printer.</span></span> <span data-ttu-id="a943d-455">Ogni voce in questa proprietà deve essere elencata anche nella matrice delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="a943d-455">Each entry in this property should also be listed in the **Capabilities** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a943d-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a943d-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a943d-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a943d-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="a943d-458"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Stampa a colori** (2)</span><span class="sxs-lookup"><span data-stu-id="a943d-458"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="a943d-459"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Stampa duplex** (3)</span><span class="sxs-lookup"><span data-stu-id="a943d-459"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="a943d-460"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copie** (4)</span><span class="sxs-lookup"><span data-stu-id="a943d-460"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="a943d-461"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Regole di confronto** (5)</span><span class="sxs-lookup"><span data-stu-id="a943d-461"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="a943d-462"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Graffatura** (6)</span><span class="sxs-lookup"><span data-stu-id="a943d-462"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="a943d-463"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Stampa trasparenza** (7)</span><span class="sxs-lookup"><span data-stu-id="a943d-463"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="a943d-464"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span><span class="sxs-lookup"><span data-stu-id="a943d-464"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="a943d-465"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Copertura** (9)</span><span class="sxs-lookup"><span data-stu-id="a943d-465"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="a943d-466"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Binding** (10)</span><span class="sxs-lookup"><span data-stu-id="a943d-466"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="a943d-467"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Stampa in bianco e nero** (11)</span><span class="sxs-lookup"><span data-stu-id="a943d-467"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="a943d-468"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un lato** (12)</span><span class="sxs-lookup"><span data-stu-id="a943d-468"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-469">Lato singolo</span><span class="sxs-lookup"><span data-stu-id="a943d-469">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="a943d-470"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bordo lungo due lati** (13)</span><span class="sxs-lookup"><span data-stu-id="a943d-470"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-471">Bordo lungo lato due</span><span class="sxs-lookup"><span data-stu-id="a943d-471">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="a943d-472"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bordo corto a due lati** (14)</span><span class="sxs-lookup"><span data-stu-id="a943d-472"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-473">Bordo corto bilaterale</span><span class="sxs-lookup"><span data-stu-id="a943d-473">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="a943d-474"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Verticale** (15)</span><span class="sxs-lookup"><span data-stu-id="a943d-474"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="a943d-475"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Orizzontale** (16)</span><span class="sxs-lookup"><span data-stu-id="a943d-475"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="a943d-476"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Verticale inverso** (17)</span><span class="sxs-lookup"><span data-stu-id="a943d-476"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="a943d-477"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Orizzontale inverso** (18)</span><span class="sxs-lookup"><span data-stu-id="a943d-477"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="a943d-478"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualità elevata** (19)</span><span class="sxs-lookup"><span data-stu-id="a943d-478"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-479">Qualità elevata</span><span class="sxs-lookup"><span data-stu-id="a943d-479">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="a943d-480"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Normale qualità** (20)</span><span class="sxs-lookup"><span data-stu-id="a943d-480"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-481">Qualità normale</span><span class="sxs-lookup"><span data-stu-id="a943d-481">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="a943d-482"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualità bassa** (21)</span><span class="sxs-lookup"><span data-stu-id="a943d-482"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-483">Qualità bassa</span><span class="sxs-lookup"><span data-stu-id="a943d-483">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a943d-484">**DefaultCopies**</span><span class="sxs-lookup"><span data-stu-id="a943d-484">**DefaultCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-485">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a943d-485">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-486">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a943d-487">Numero di copie che un singolo processo produrrà, salvo diversa indicazione.</span><span class="sxs-lookup"><span data-stu-id="a943d-487">Number of copies that a single job will produce, unless otherwise specified.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-488">**DefaultLanguage**</span><span class="sxs-lookup"><span data-stu-id="a943d-488">**DefaultLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-489">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a943d-489">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-490">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-490">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-491">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**. LanguagesSupported "," CIM \_ Printer. DefaultMimeType ")</span><span class="sxs-lookup"><span data-stu-id="a943d-491">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_Printer.DefaultMimeType")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-492">Lingua predefinita della stampante.</span><span class="sxs-lookup"><span data-stu-id="a943d-492">Default printer language.</span></span> <span data-ttu-id="a943d-493">La lingua deve essere elencata anche nella proprietà **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="a943d-493">The language should also be listed in the **LanguagesSupported** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a943d-494">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a943d-494">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a943d-495">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a943d-495">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="a943d-496">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="a943d-496">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="a943d-497">**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="a943d-497">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="a943d-498">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="a943d-498">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="a943d-499">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="a943d-499">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="a943d-500">**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="a943d-500">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="a943d-501">**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="a943d-501">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="a943d-502">**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="a943d-502">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="a943d-503">**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="a943d-503">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="a943d-504">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="a943d-504">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="a943d-505">**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="a943d-505">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="a943d-506">**Interstampa** (13)</span><span class="sxs-lookup"><span data-stu-id="a943d-506">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="a943d-507">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="a943d-507">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="a943d-508">**Dati riga** (15)</span><span class="sxs-lookup"><span data-stu-id="a943d-508">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="a943d-509">**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="a943d-509">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="a943d-510">**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="a943d-510">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="a943d-511">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="a943d-511">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="a943d-512">**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="a943d-512">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="a943d-513">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="a943d-513">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="a943d-514">**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="a943d-514">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="a943d-515">**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="a943d-515">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="a943d-516">**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="a943d-516">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="a943d-517">**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="a943d-517">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="a943d-518">**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="a943d-518">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="a943d-519">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="a943d-519">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="a943d-520">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="a943d-520">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="a943d-521">**Quic** (28)</span><span class="sxs-lookup"><span data-stu-id="a943d-521">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="a943d-522">**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="a943d-522">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="a943d-523">**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="a943d-523">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="a943d-524">**Testo semplice** (31)</span><span class="sxs-lookup"><span data-stu-id="a943d-524">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="a943d-525">**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="a943d-525">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="a943d-526">**Documento** (33)</span><span class="sxs-lookup"><span data-stu-id="a943d-526">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="a943d-527">**impressione** (34)</span><span class="sxs-lookup"><span data-stu-id="a943d-527">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="a943d-528">**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="a943d-528">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="a943d-529">**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="a943d-529">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="a943d-530">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="a943d-530">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="a943d-531">**Automatico** (38)</span><span class="sxs-lookup"><span data-stu-id="a943d-531">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="a943d-532">**Pagine** (39)</span><span class="sxs-lookup"><span data-stu-id="a943d-532">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="a943d-533">**Lip** (40)</span><span class="sxs-lookup"><span data-stu-id="a943d-533">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="a943d-534">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="a943d-534">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="a943d-535">**Diagnostica** (42)</span><span class="sxs-lookup"><span data-stu-id="a943d-535">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="a943d-536">**Capsal** (43)</span><span class="sxs-lookup"><span data-stu-id="a943d-536">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="a943d-537">**Escl** (44)</span><span class="sxs-lookup"><span data-stu-id="a943d-537">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="a943d-538">**LCD** (45)</span><span class="sxs-lookup"><span data-stu-id="a943d-538">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="a943d-539">**XES** (46)</span><span class="sxs-lookup"><span data-stu-id="a943d-539">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="a943d-540">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="a943d-540">**MIME** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a943d-541">**DefaultMimeType**</span><span class="sxs-lookup"><span data-stu-id="a943d-541">**DefaultMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-542">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-543">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-544">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**DefaultLanguage**")</span><span class="sxs-lookup"><span data-stu-id="a943d-544">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**DefaultLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-545">Tipo MIME predefinito utilizzato dalla stampante quando la proprietà **defaultLanguage** è impostata per indicare che un tipo MIME è in uso.</span><span class="sxs-lookup"><span data-stu-id="a943d-545">Default mime type used by the printer when the **DefaultLanguage** property is set to indicate that a mime type is in use.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-546">**DefaultNumberUp**</span><span class="sxs-lookup"><span data-stu-id="a943d-546">**DefaultNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-547">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a943d-547">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-548">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a943d-549">Numero di pagine del flusso di stampa che la stampante eseguirà il rendering su un solo foglio multimediale, a meno che un processo non specifichi diversamente.</span><span class="sxs-lookup"><span data-stu-id="a943d-549">Number of print-stream pages that the printer will render onto a single media sheet, unless a job specifies otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-550">**DefaultPaperType**</span><span class="sxs-lookup"><span data-stu-id="a943d-550">**DefaultPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-551">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-551">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-552">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-553">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="a943d-553">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-554">Tipo di carta che la stampante utilizzerà se PrintJob non specifica un tipo particolare.</span><span class="sxs-lookup"><span data-stu-id="a943d-554">Paper type that the printer will use if PrintJob does not specify a particular type.</span></span> <span data-ttu-id="a943d-555">La stringa deve essere espressa nel formato specificato dall'applicazione di stampa documenti ISO/IEC 10175, anch ' essa riepilogata nell'Appendice C di RFC 1759 (Printer MIB).</span><span class="sxs-lookup"><span data-stu-id="a943d-555">The string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

</dd> <dt>

<span data-ttu-id="a943d-556">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a943d-556">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-557">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-558">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-559">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a943d-559">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-560">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a943d-560">Textual description of the object.</span></span>

<span data-ttu-id="a943d-561">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-561">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a943d-562">**DetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="a943d-562">**DetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-563">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a943d-563">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-564">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-565">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**ErrorInformation**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIB. IETF \| Printer-MIB. hrPrinterDetectedErrorState ")</span><span class="sxs-lookup"><span data-stu-id="a943d-565">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**ErrorInformation**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.hrPrinterDetectedErrorState")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-566">Informazioni sull'errore della stampante.</span><span class="sxs-lookup"><span data-stu-id="a943d-566">Printer error information.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a943d-567">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a943d-567">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a943d-568">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a943d-568">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

<span data-ttu-id="a943d-569">**Nessun errore** (2)</span><span class="sxs-lookup"><span data-stu-id="a943d-569">**No Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

<span data-ttu-id="a943d-570">**Carta bassa** (3)</span><span class="sxs-lookup"><span data-stu-id="a943d-570">**Low Paper** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

<span data-ttu-id="a943d-571">**Nessun documento** (4)</span><span class="sxs-lookup"><span data-stu-id="a943d-571">**No Paper** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

<span data-ttu-id="a943d-572">**Toner basso** (5)</span><span class="sxs-lookup"><span data-stu-id="a943d-572">**Low Toner** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

<span data-ttu-id="a943d-573">**Nessun toner** (6)</span><span class="sxs-lookup"><span data-stu-id="a943d-573">**No Toner** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

<span data-ttu-id="a943d-574">**Sportello aperto** (7)</span><span class="sxs-lookup"><span data-stu-id="a943d-574">**Door Open** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

<span data-ttu-id="a943d-575">**Bloccato** (8)</span><span class="sxs-lookup"><span data-stu-id="a943d-575">**Jammed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="a943d-576">**Offline** (9)</span><span class="sxs-lookup"><span data-stu-id="a943d-576">**Offline** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

<span data-ttu-id="a943d-577">**Servizio richiesto** (10)</span><span class="sxs-lookup"><span data-stu-id="a943d-577">**Service Requested** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

<span data-ttu-id="a943d-578">**Bin di output completo** (11)</span><span class="sxs-lookup"><span data-stu-id="a943d-578">**Output Bin Full** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a943d-579">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a943d-579">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-580">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-581">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-582">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a943d-582">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a943d-583">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a943d-583">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="a943d-584">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-584">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a943d-585">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a943d-585">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-586">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a943d-586">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-587">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-587">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a943d-588">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="a943d-588">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="a943d-589">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-589">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a943d-590">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a943d-590">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-591">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-592">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-592">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a943d-593">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="a943d-593">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="a943d-594">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-594">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a943d-595">**ErrorInformation**</span><span class="sxs-lookup"><span data-stu-id="a943d-595">**ErrorInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-596">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="a943d-596">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a943d-597">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a943d-597">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a943d-598">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**.**DetectedErrorState**")</span><span class="sxs-lookup"><span data-stu-id="a943d-598">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**DetectedErrorState**")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-599">Matrice che fornisce informazioni aggiuntive per lo stato di errore corrente, indicato nella proprietà **DetectedErrorState** .</span><span class="sxs-lookup"><span data-stu-id="a943d-599">Array that provides supplemental information for the current error state, indicated in the **DetectedErrorState** property.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-600">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="a943d-600">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-601">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a943d-601">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-602">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-603">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. HorizontalResolution"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixel per pollice")</span><span class="sxs-lookup"><span data-stu-id="a943d-603">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-604">Risoluzione orizzontale in pixel per pollice.</span><span class="sxs-lookup"><span data-stu-id="a943d-604">Horizontal resolution in pixels-per-inch.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-605">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a943d-605">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-606">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a943d-606">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-607">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-608">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="a943d-608">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-609">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a943d-609">Date and time the object was installed.</span></span> <span data-ttu-id="a943d-610">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="a943d-610">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a943d-611">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-611">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a943d-612">**JobCountSinceLastReset**</span><span class="sxs-lookup"><span data-stu-id="a943d-612">**JobCountSinceLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-613">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a943d-613">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-614">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-614">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-615">Qualificatori: **contatore**</span><span class="sxs-lookup"><span data-stu-id="a943d-615">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="a943d-616">Processi di stampa elaborati dopo l'ultima reimpostazione.</span><span class="sxs-lookup"><span data-stu-id="a943d-616">Printer jobs processed since the last reset.</span></span> <span data-ttu-id="a943d-617">Questi processi possono essere elaborati da una o più code di stampa.</span><span class="sxs-lookup"><span data-stu-id="a943d-617">These jobs can be processed from one or more print queues.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-618">**LanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="a943d-618">**LanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-619">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a943d-619">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a943d-620">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-620">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-621">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtInterpreterLangFamily "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**. MimeTypesSupported "," CIM \_ PrintJob. Language "," CIM \_ printservice. LanguagesSupported ")</span><span class="sxs-lookup"><span data-stu-id="a943d-621">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.MimeTypesSupported", "CIM\_PrintJob.Language", "CIM\_PrintService.LanguagesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-622">Lingue di stampa supportate in modo nativo.</span><span class="sxs-lookup"><span data-stu-id="a943d-622">Print languages that are natively supported.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a943d-623">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a943d-623">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a943d-624">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a943d-624">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="a943d-625">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="a943d-625">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="a943d-626">**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="a943d-626">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="a943d-627">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="a943d-627">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="a943d-628">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="a943d-628">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="a943d-629">**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="a943d-629">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="a943d-630">**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="a943d-630">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="a943d-631">**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="a943d-631">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="a943d-632">**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="a943d-632">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="a943d-633">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="a943d-633">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="a943d-634">**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="a943d-634">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="a943d-635">**Interstampa** (13)</span><span class="sxs-lookup"><span data-stu-id="a943d-635">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="a943d-636">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="a943d-636">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="a943d-637">**Dati riga** (15)</span><span class="sxs-lookup"><span data-stu-id="a943d-637">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="a943d-638">**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="a943d-638">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="a943d-639">**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="a943d-639">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="a943d-640">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="a943d-640">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="a943d-641">**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="a943d-641">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="a943d-642">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="a943d-642">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="a943d-643">**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="a943d-643">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="a943d-644">**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="a943d-644">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="a943d-645">**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="a943d-645">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="a943d-646">**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="a943d-646">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="a943d-647">**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="a943d-647">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="a943d-648">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="a943d-648">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="a943d-649">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="a943d-649">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="a943d-650">**Quic** (28)</span><span class="sxs-lookup"><span data-stu-id="a943d-650">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="a943d-651">**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="a943d-651">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="a943d-652">**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="a943d-652">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="a943d-653">**Testo semplice** (31)</span><span class="sxs-lookup"><span data-stu-id="a943d-653">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="a943d-654">**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="a943d-654">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="a943d-655">**Documento** (33)</span><span class="sxs-lookup"><span data-stu-id="a943d-655">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="a943d-656">**impressione** (34)</span><span class="sxs-lookup"><span data-stu-id="a943d-656">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="a943d-657">**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="a943d-657">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="a943d-658">**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="a943d-658">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="a943d-659">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="a943d-659">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="a943d-660">**Automatico** (38)</span><span class="sxs-lookup"><span data-stu-id="a943d-660">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="a943d-661">**Pagine** (39)</span><span class="sxs-lookup"><span data-stu-id="a943d-661">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="a943d-662">**Lip** (40)</span><span class="sxs-lookup"><span data-stu-id="a943d-662">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="a943d-663">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="a943d-663">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="a943d-664">**Diagnostica** (42)</span><span class="sxs-lookup"><span data-stu-id="a943d-664">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="a943d-665">**Capsal** (43)</span><span class="sxs-lookup"><span data-stu-id="a943d-665">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="a943d-666">**Escl** (44)</span><span class="sxs-lookup"><span data-stu-id="a943d-666">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="a943d-667">**LCD** (45)</span><span class="sxs-lookup"><span data-stu-id="a943d-667">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="a943d-668">**XES** (46)</span><span class="sxs-lookup"><span data-stu-id="a943d-668">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="a943d-669">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="a943d-669">**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span data-ttu-id="a943d-670">**XPS** (48)</span><span class="sxs-lookup"><span data-stu-id="a943d-670">**XPS** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span data-ttu-id="a943d-671">**HPGL2** (49)</span><span class="sxs-lookup"><span data-stu-id="a943d-671">**HPGL2** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span data-ttu-id="a943d-672">**PCLXL** (50)</span><span class="sxs-lookup"><span data-stu-id="a943d-672">**PCLXL** (50)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a943d-673">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a943d-673">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-674">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a943d-674">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-675">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-675">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a943d-676">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a943d-676">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a943d-677">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-677">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a943d-678">**MarkingTechnology**</span><span class="sxs-lookup"><span data-stu-id="a943d-678">**MarkingTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-679">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a943d-679">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-680">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-680">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-681">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtMarkerMarkTech ")</span><span class="sxs-lookup"><span data-stu-id="a943d-681">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtMarkerMarkTech")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-682">Contrassegno della tecnologia utilizzata dalla stampante.</span><span class="sxs-lookup"><span data-stu-id="a943d-682">Marking technology used by the printer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a943d-683">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a943d-683">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a943d-684">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a943d-684">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

<span data-ttu-id="a943d-685">**LED elettrofotografica** (3)</span><span class="sxs-lookup"><span data-stu-id="a943d-685">**Electrophotographic LED** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

<span data-ttu-id="a943d-686">**Elettrofotografica laser** (4)</span><span class="sxs-lookup"><span data-stu-id="a943d-686">**Electrophotographic Laser** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="a943d-687">**Elettrofotografica other** (5)</span><span class="sxs-lookup"><span data-stu-id="a943d-687">**Electrophotographic Other** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

<span data-ttu-id="a943d-688">**Influisca sulla matrice del punto principale 9pin** (6)</span><span class="sxs-lookup"><span data-stu-id="a943d-688">**Impact Moving Head Dot Matrix 9pin** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

<span data-ttu-id="a943d-689">**Influisca sulla matrice del punto principale 24pin** (7)</span><span class="sxs-lookup"><span data-stu-id="a943d-689">**Impact Moving Head Dot Matrix 24pin** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

<span data-ttu-id="a943d-690">Effetto sullo stato di una **matrice del punto principale** (8)</span><span class="sxs-lookup"><span data-stu-id="a943d-690">**Impact Moving Head Dot Matrix Other** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

<span data-ttu-id="a943d-691">**Effetto della testa di trasferimento completamente formato** (9)</span><span class="sxs-lookup"><span data-stu-id="a943d-691">**Impact Moving Head Fully Formed** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

<span data-ttu-id="a943d-692">**Gruppo di effetti** (10)</span><span class="sxs-lookup"><span data-stu-id="a943d-692">**Impact Band** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

<span data-ttu-id="a943d-693">**Altro effetto** (11)</span><span class="sxs-lookup"><span data-stu-id="a943d-693">**Impact Other** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

<span data-ttu-id="a943d-694">**Inkjet acquoso** (12)</span><span class="sxs-lookup"><span data-stu-id="a943d-694">**Inkjet Aqueous** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

<span data-ttu-id="a943d-695">**Solido Inkjet** (13)</span><span class="sxs-lookup"><span data-stu-id="a943d-695">**Inkjet Solid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

<span data-ttu-id="a943d-696">**Altro Inkjet** (14)</span><span class="sxs-lookup"><span data-stu-id="a943d-696">**Inkjet Other** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

<span data-ttu-id="a943d-697">**Penna** (15)</span><span class="sxs-lookup"><span data-stu-id="a943d-697">**Pen** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

<span data-ttu-id="a943d-698">**Trasferimento termico** (16)</span><span class="sxs-lookup"><span data-stu-id="a943d-698">**Thermal Transfer** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

<span data-ttu-id="a943d-699">**Sensibile alla temperatura** (17)</span><span class="sxs-lookup"><span data-stu-id="a943d-699">**Thermal Sensitive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

<span data-ttu-id="a943d-700">**Diffusione termica** (18)</span><span class="sxs-lookup"><span data-stu-id="a943d-700">**Thermal Diffusion** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

<span data-ttu-id="a943d-701">**Altro termico** (19)</span><span class="sxs-lookup"><span data-stu-id="a943d-701">**Thermal Other** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

<span data-ttu-id="a943d-702">**Elettroerosione** (20)</span><span class="sxs-lookup"><span data-stu-id="a943d-702">**Electroerosion** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

<span data-ttu-id="a943d-703">**Elettrostatica** (21)</span><span class="sxs-lookup"><span data-stu-id="a943d-703">**Electrostatic** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

<span data-ttu-id="a943d-704">**Microscheda fotografica** (22)</span><span class="sxs-lookup"><span data-stu-id="a943d-704">**Photographic Microfiche** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

<span data-ttu-id="a943d-705">**Fotounità fotografico** (23)</span><span class="sxs-lookup"><span data-stu-id="a943d-705">**Photographic Imagesetter** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="a943d-706">**Altro fotografico** (24)</span><span class="sxs-lookup"><span data-stu-id="a943d-706">**Photographic Other** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

<span data-ttu-id="a943d-707">**Deposizione degli ioni** (25)</span><span class="sxs-lookup"><span data-stu-id="a943d-707">**Ion Deposition** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

<span data-ttu-id="a943d-708">**eBeam** (26)</span><span class="sxs-lookup"><span data-stu-id="a943d-708">**eBeam** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

<span data-ttu-id="a943d-709">**Tipografo** (27)</span><span class="sxs-lookup"><span data-stu-id="a943d-709">**Typesetter** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a943d-710">**MaxCopies**</span><span class="sxs-lookup"><span data-stu-id="a943d-710">**MaxCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-711">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a943d-711">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-712">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-712">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-713">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. Copies")</span><span class="sxs-lookup"><span data-stu-id="a943d-713">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.Copies")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-714">Numero massimo di copie che possono essere generate dalla stampante da un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="a943d-714">Maximum number of copies that can be produced by the printer from a single job.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-715">**MaxNumberUp**</span><span class="sxs-lookup"><span data-stu-id="a943d-715">**MaxNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-716">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a943d-716">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-717">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-717">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-718">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. NumberUp")</span><span class="sxs-lookup"><span data-stu-id="a943d-718">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.NumberUp")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-719">Numero massimo di pagine del flusso di stampa che la stampante è in grado di eseguire il rendering su un solo foglio multimediale.</span><span class="sxs-lookup"><span data-stu-id="a943d-719">Maximum number of print-stream pages that the printer can render onto a single media sheet.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-720">**MaxSizeSupported**</span><span class="sxs-lookup"><span data-stu-id="a943d-720">**MaxSizeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-721">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a943d-721">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-722">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-722">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-723">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. JobSize"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="a943d-723">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.JobSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-724">Il processo più grande (come flusso di byte) che la stampante accetterà in unità di kilobyte.</span><span class="sxs-lookup"><span data-stu-id="a943d-724">Largest job (as a byte stream) that the printer will accept in units of kilobytes.</span></span> <span data-ttu-id="a943d-725">Il valore 0 (zero) indica che non è stato impostato alcun limite.</span><span class="sxs-lookup"><span data-stu-id="a943d-725">A value of 0 (zero) indicates that no limit has been set.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-726">**MimeTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="a943d-726">**MimeTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-727">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="a943d-727">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a943d-728">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-728">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-729">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Printer**. LanguagesSupported "," CIM \_ PrintJob. mimetypes "," CIM \_ printservice. MimeTypesSupported ")</span><span class="sxs-lookup"><span data-stu-id="a943d-729">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_PrintJob.MimeTypes", "CIM\_PrintService.MimeTypesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-730">Stringhe in formato libero che forniscono spiegazioni dettagliate dei tipi MIME supportati dalla stampante.</span><span class="sxs-lookup"><span data-stu-id="a943d-730">Free-form strings that provide detailed explanations of mime types that are supported by the printer.</span></span> <span data-ttu-id="a943d-731">Se per questa proprietà vengono forniti dati, il valore 47 ("MIME") deve essere incluso nella proprietà **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="a943d-731">If data is provided for this property, then the value 47 ("Mime"), should be included in the **LanguagesSupported** property.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-732">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a943d-732">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-733">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-733">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-734">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-734">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-735">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a943d-735">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-736">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="a943d-736">Label by which the object is known.</span></span> <span data-ttu-id="a943d-737">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="a943d-737">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a943d-738">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-738">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a943d-739">**NaturalLanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="a943d-739">**NaturalLanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-740">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="a943d-740">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a943d-741">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-741">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-742">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtLocalizationLanguage "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ PrintJob. naturallanguage ")</span><span class="sxs-lookup"><span data-stu-id="a943d-742">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.NaturalLanguage")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-743">Lingue disponibili per le stringhe utilizzate dalla stampante per l'output delle informazioni di gestione.</span><span class="sxs-lookup"><span data-stu-id="a943d-743">Available languages for strings used by the printer for management information output.</span></span> <span data-ttu-id="a943d-744">Le stringhe devono essere conformi allo standard RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="a943d-744">The strings should conform to RFC 1766.</span></span> <span data-ttu-id="a943d-745">Ad esempio, "en" viene usato per la lingua inglese.</span><span class="sxs-lookup"><span data-stu-id="a943d-745">For example, "en" is used for English.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-746">**PaperSizesSupported**</span><span class="sxs-lookup"><span data-stu-id="a943d-746">**PaperSizesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-747">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a943d-747">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a943d-748">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-748">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a943d-749">Tipi di carta supportati.</span><span class="sxs-lookup"><span data-stu-id="a943d-749">Types of paper supported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a943d-750">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a943d-750">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a943d-751">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a943d-751">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span data-ttu-id="a943d-752">**A** (2)</span><span class="sxs-lookup"><span data-stu-id="a943d-752">**A** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="a943d-753">**B** (3)</span><span class="sxs-lookup"><span data-stu-id="a943d-753">**B** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span data-ttu-id="a943d-754">**C** (4)</span><span class="sxs-lookup"><span data-stu-id="a943d-754">**C** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span data-ttu-id="a943d-755">**D** (5)</span><span class="sxs-lookup"><span data-stu-id="a943d-755">**D** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="a943d-756">**E** (6)</span><span class="sxs-lookup"><span data-stu-id="a943d-756">**E** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span data-ttu-id="a943d-757">**Lettera** (7)</span><span class="sxs-lookup"><span data-stu-id="a943d-757">**Letter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span data-ttu-id="a943d-758">**Legal** (8)</span><span class="sxs-lookup"><span data-stu-id="a943d-758">**Legal** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span data-ttu-id="a943d-759">**Na-10x13-envelope** (9)</span><span class="sxs-lookup"><span data-stu-id="a943d-759">**NA-10x13-Envelope** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span data-ttu-id="a943d-760">**Na-9x12-envelope** (10)</span><span class="sxs-lookup"><span data-stu-id="a943d-760">**NA-9x12-Envelope** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span data-ttu-id="a943d-761">**Na-Number-10-busta** (11)</span><span class="sxs-lookup"><span data-stu-id="a943d-761">**NA-Number-10-Envelope** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span data-ttu-id="a943d-762">**Na-7x9-envelope** (12)</span><span class="sxs-lookup"><span data-stu-id="a943d-762">**NA-7x9-Envelope** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span data-ttu-id="a943d-763">**Na-9x11-envelope** (13)</span><span class="sxs-lookup"><span data-stu-id="a943d-763">**NA-9x11-Envelope** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span data-ttu-id="a943d-764">**Na-10x14-envelope** (14)</span><span class="sxs-lookup"><span data-stu-id="a943d-764">**NA-10x14-Envelope** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span data-ttu-id="a943d-765">**Na-Number-9-busta** (15)</span><span class="sxs-lookup"><span data-stu-id="a943d-765">**NA-Number-9-Envelope** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span data-ttu-id="a943d-766">**Na-6x9-envelope** (16)</span><span class="sxs-lookup"><span data-stu-id="a943d-766">**NA-6x9-Envelope** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span data-ttu-id="a943d-767">**Na-10x15-envelope** (17)</span><span class="sxs-lookup"><span data-stu-id="a943d-767">**NA-10x15-Envelope** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span data-ttu-id="a943d-768">**A0** (18)</span><span class="sxs-lookup"><span data-stu-id="a943d-768">**A0** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span data-ttu-id="a943d-769">**A1** (19)</span><span class="sxs-lookup"><span data-stu-id="a943d-769">**A1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span data-ttu-id="a943d-770">**A2** (20)</span><span class="sxs-lookup"><span data-stu-id="a943d-770">**A2** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span data-ttu-id="a943d-771">**A3** (21)</span><span class="sxs-lookup"><span data-stu-id="a943d-771">**A3** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span data-ttu-id="a943d-772">**A4** (22)</span><span class="sxs-lookup"><span data-stu-id="a943d-772">**A4** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span data-ttu-id="a943d-773">**A5** (23)</span><span class="sxs-lookup"><span data-stu-id="a943d-773">**A5** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span data-ttu-id="a943d-774">**A6** (24)</span><span class="sxs-lookup"><span data-stu-id="a943d-774">**A6** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span data-ttu-id="a943d-775">**A7** (25)</span><span class="sxs-lookup"><span data-stu-id="a943d-775">**A7** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span data-ttu-id="a943d-776">**A8** (26)</span><span class="sxs-lookup"><span data-stu-id="a943d-776">**A8** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span data-ttu-id="a943d-777">**A9A10** (27)</span><span class="sxs-lookup"><span data-stu-id="a943d-777">**A9A10** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span data-ttu-id="a943d-778">**B0** (28)</span><span class="sxs-lookup"><span data-stu-id="a943d-778">**B0** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span data-ttu-id="a943d-779">**B1** (29)</span><span class="sxs-lookup"><span data-stu-id="a943d-779">**B1** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span data-ttu-id="a943d-780">**B2** (30)</span><span class="sxs-lookup"><span data-stu-id="a943d-780">**B2** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span data-ttu-id="a943d-781">**B3** (31)</span><span class="sxs-lookup"><span data-stu-id="a943d-781">**B3** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span data-ttu-id="a943d-782">**B4** (32)</span><span class="sxs-lookup"><span data-stu-id="a943d-782">**B4** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span data-ttu-id="a943d-783">**B5** (33)</span><span class="sxs-lookup"><span data-stu-id="a943d-783">**B5** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span data-ttu-id="a943d-784">**B6** (34)</span><span class="sxs-lookup"><span data-stu-id="a943d-784">**B6** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span data-ttu-id="a943d-785">**B7** (35)</span><span class="sxs-lookup"><span data-stu-id="a943d-785">**B7** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span data-ttu-id="a943d-786">**B8** (36)</span><span class="sxs-lookup"><span data-stu-id="a943d-786">**B8** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span data-ttu-id="a943d-787">**B9** (37)</span><span class="sxs-lookup"><span data-stu-id="a943d-787">**B9** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span data-ttu-id="a943d-788">**B10** (38)</span><span class="sxs-lookup"><span data-stu-id="a943d-788">**B10** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span data-ttu-id="a943d-789">**C0** (39)</span><span class="sxs-lookup"><span data-stu-id="a943d-789">**C0** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span data-ttu-id="a943d-790">**C1** (40)</span><span class="sxs-lookup"><span data-stu-id="a943d-790">**C1** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span data-ttu-id="a943d-791">**C2C3** (41)</span><span class="sxs-lookup"><span data-stu-id="a943d-791">**C2C3** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span data-ttu-id="a943d-792">**C4** (42)</span><span class="sxs-lookup"><span data-stu-id="a943d-792">**C4** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span data-ttu-id="a943d-793">**C5** (43)</span><span class="sxs-lookup"><span data-stu-id="a943d-793">**C5** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span data-ttu-id="a943d-794">**C6** (44)</span><span class="sxs-lookup"><span data-stu-id="a943d-794">**C6** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span data-ttu-id="a943d-795">**C7** (45)</span><span class="sxs-lookup"><span data-stu-id="a943d-795">**C7** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span data-ttu-id="a943d-796">**C8** (46)</span><span class="sxs-lookup"><span data-stu-id="a943d-796">**C8** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span data-ttu-id="a943d-797">**Designato da ISO** (47)</span><span class="sxs-lookup"><span data-stu-id="a943d-797">**ISO-Designated** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span data-ttu-id="a943d-798">**JIS B0** (48)</span><span class="sxs-lookup"><span data-stu-id="a943d-798">**JIS B0** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span data-ttu-id="a943d-799">**JIS B1** (49)</span><span class="sxs-lookup"><span data-stu-id="a943d-799">**JIS B1** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span data-ttu-id="a943d-800">**JIS B2** (50)</span><span class="sxs-lookup"><span data-stu-id="a943d-800">**JIS B2** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span data-ttu-id="a943d-801">**JIS B3** (51)</span><span class="sxs-lookup"><span data-stu-id="a943d-801">**JIS B3** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span data-ttu-id="a943d-802">**JIS B4** (52)</span><span class="sxs-lookup"><span data-stu-id="a943d-802">**JIS B4** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span data-ttu-id="a943d-803">**JIS B5** (53)</span><span class="sxs-lookup"><span data-stu-id="a943d-803">**JIS B5** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span data-ttu-id="a943d-804">**JIS B6** (54)</span><span class="sxs-lookup"><span data-stu-id="a943d-804">**JIS B6** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span data-ttu-id="a943d-805">**JIS B7** (55)</span><span class="sxs-lookup"><span data-stu-id="a943d-805">**JIS B7** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span data-ttu-id="a943d-806">**JIS B8** (56)</span><span class="sxs-lookup"><span data-stu-id="a943d-806">**JIS B8** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span data-ttu-id="a943d-807">**JIS B9** (57)</span><span class="sxs-lookup"><span data-stu-id="a943d-807">**JIS B9** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span data-ttu-id="a943d-808">**JIS B10** (58)</span><span class="sxs-lookup"><span data-stu-id="a943d-808">**JIS B10** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span data-ttu-id="a943d-809">**Na-Letter** (59)</span><span class="sxs-lookup"><span data-stu-id="a943d-809">**NA-Letter** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span data-ttu-id="a943d-810">**Na-Legal** (60)</span><span class="sxs-lookup"><span data-stu-id="a943d-810">**NA-Legal** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span data-ttu-id="a943d-811">**B4-busta** (61)</span><span class="sxs-lookup"><span data-stu-id="a943d-811">**B4-Envelope** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span data-ttu-id="a943d-812">**B5-Busta** (62)</span><span class="sxs-lookup"><span data-stu-id="a943d-812">**B5-Envelope** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span data-ttu-id="a943d-813">**Busta C3** (63)</span><span class="sxs-lookup"><span data-stu-id="a943d-813">**C3-Envelope** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span data-ttu-id="a943d-814">**Busta C4** (64)</span><span class="sxs-lookup"><span data-stu-id="a943d-814">**C4-Envelope** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span data-ttu-id="a943d-815">**C5-busta** (65)</span><span class="sxs-lookup"><span data-stu-id="a943d-815">**C5-Envelope** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span data-ttu-id="a943d-816">**Busta C6** (66)</span><span class="sxs-lookup"><span data-stu-id="a943d-816">**C6-Envelope** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span data-ttu-id="a943d-817">**Designata-busta lunga** (67)</span><span class="sxs-lookup"><span data-stu-id="a943d-817">**Designated-Long-Envelope** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span data-ttu-id="a943d-818">**Monarca-busta** (68)</span><span class="sxs-lookup"><span data-stu-id="a943d-818">**Monarch-Envelope** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="a943d-819">**Dirigente** (69)</span><span class="sxs-lookup"><span data-stu-id="a943d-819">**Executive** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span data-ttu-id="a943d-820">**Folio** (70)</span><span class="sxs-lookup"><span data-stu-id="a943d-820">**Folio** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span data-ttu-id="a943d-821">**Fattura** (71)</span><span class="sxs-lookup"><span data-stu-id="a943d-821">**Invoice** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span data-ttu-id="a943d-822">**Ledger** (72)</span><span class="sxs-lookup"><span data-stu-id="a943d-822">**Ledger** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span data-ttu-id="a943d-823">**Quarto** (73)</span><span class="sxs-lookup"><span data-stu-id="a943d-823">**Quarto** (73)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a943d-824">**PaperTypesAvailable**</span><span class="sxs-lookup"><span data-stu-id="a943d-824">**PaperTypesAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-825">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="a943d-825">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a943d-826">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-826">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-827">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. RequiredPaperType", "CIM \_ printservice. PaperTypesAvailable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtInputMediaName ")</span><span class="sxs-lookup"><span data-stu-id="a943d-827">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.RequiredPaperType", "CIM\_PrintService.PaperTypesAvailable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtInputMediaName")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-828">Stringhe in formato libero che specificano i tipi di carta attualmente disponibili per la stampante.</span><span class="sxs-lookup"><span data-stu-id="a943d-828">Free-form strings that specify the types of paper that are currently available for the printer.</span></span> <span data-ttu-id="a943d-829">Ogni stringa deve essere espressa nel formato specificato da ISO/IEC 10175 Document Printing Application (DPA), che viene anche riepilogato nell'Appendice C di RFC 1759 (Printer MIB).</span><span class="sxs-lookup"><span data-stu-id="a943d-829">Each string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span> <span data-ttu-id="a943d-830">Esempi di stringhe valide sono "ISO-a4-colored" e "na-10x14-envelope".</span><span class="sxs-lookup"><span data-stu-id="a943d-830">Examples of valid strings are "iso-a4-colored" and "na-10x14-envelope".</span></span> <span data-ttu-id="a943d-831">Per definizione, il formato della carta disponibile ed elencato nella proprietà **PaperTypesAvailable** deve essere presente anche nella proprietà **PaperSizesSupported** .</span><span class="sxs-lookup"><span data-stu-id="a943d-831">By definition, a paper size that is available and listed in the **PaperTypesAvailable** property should also appear in the **PaperSizesSupported** property.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-832">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a943d-832">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-833">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-834">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-834">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-835">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a943d-835">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-836">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a943d-836">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="a943d-837">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-837">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a943d-838">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a943d-838">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="a943d-839">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a943d-839">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-840">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a943d-840">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a943d-841">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-841">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a943d-842">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a943d-842">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="a943d-843">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="a943d-843">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a943d-844"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a943d-844"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a943d-845"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="a943d-845"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a943d-846"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="a943d-846"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a943d-847"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="a943d-847"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-848">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="a943d-848">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a943d-849"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="a943d-849"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-850">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="a943d-850">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a943d-851"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="a943d-851"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-852">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="a943d-852">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="a943d-853">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="a943d-853">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="a943d-854">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="a943d-854">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a943d-855"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="a943d-855"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-856">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="a943d-856">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a943d-857"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="a943d-857"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a943d-858">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="a943d-858">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a943d-859">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a943d-859">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-860">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a943d-860">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-861">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-861">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a943d-862">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="a943d-862">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="a943d-863">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="a943d-863">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="a943d-864">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="a943d-864">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="a943d-865">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="a943d-865">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="a943d-866">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-866">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a943d-867">**PrinterStatus**</span><span class="sxs-lookup"><span data-stu-id="a943d-867">**PrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-868">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a943d-868">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-869">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-869">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-870">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. hrPrinterStatus ")</span><span class="sxs-lookup"><span data-stu-id="a943d-870">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.hrPrinterStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-871">Informazioni sullo stato, oltre a quelle specificate nella proprietà **Availability** , per una stampante.</span><span class="sxs-lookup"><span data-stu-id="a943d-871">Status information, beyond that specified in the **Availability** property, for a printer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a943d-872">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a943d-872">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a943d-873">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a943d-873">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="a943d-874">**Inattivo** (3)</span><span class="sxs-lookup"><span data-stu-id="a943d-874">**Idle** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span data-ttu-id="a943d-875">**Stampa** (4)</span><span class="sxs-lookup"><span data-stu-id="a943d-875">**Printing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span data-ttu-id="a943d-876">**Riscaldamento** (5)</span><span class="sxs-lookup"><span data-stu-id="a943d-876">**Warmup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span data-ttu-id="a943d-877">**Stampa interrotta** (6)</span><span class="sxs-lookup"><span data-stu-id="a943d-877">**Stopped Printing** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="a943d-878">**Offline** (7)</span><span class="sxs-lookup"><span data-stu-id="a943d-878">**Offline** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a943d-879">**Status**</span><span class="sxs-lookup"><span data-stu-id="a943d-879">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-880">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-880">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-881">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-881">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-882">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a943d-882">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-883">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a943d-883">Current status of the object.</span></span> <span data-ttu-id="a943d-884">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-884">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a943d-885">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a943d-885">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a943d-886">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a943d-886">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a943d-887">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="a943d-887">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a943d-888">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="a943d-888">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a943d-889">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a943d-889">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a943d-890">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="a943d-890">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a943d-891">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="a943d-891">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a943d-892">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="a943d-892">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a943d-893">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="a943d-893">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a943d-894">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="a943d-894">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a943d-895">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="a943d-895">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a943d-896">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="a943d-896">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a943d-897">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="a943d-897">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a943d-898">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a943d-898">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-899">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a943d-899">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-900">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-900">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-901">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a943d-901">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-902">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a943d-902">State of the logical device.</span></span> <span data-ttu-id="a943d-903">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="a943d-903">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="a943d-904">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-904">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a943d-905">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a943d-905">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a943d-906">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a943d-906">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a943d-907">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="a943d-907">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a943d-908">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="a943d-908">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a943d-909">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="a943d-909">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a943d-910">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a943d-910">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-911">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-911">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-912">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-912">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-913">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a943d-913">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a943d-914">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="a943d-914">Scoping system's creation class name.</span></span>

<span data-ttu-id="a943d-915">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-915">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a943d-916">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a943d-916">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-917">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a943d-917">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-918">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-918">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-919">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a943d-919">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a943d-920">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="a943d-920">Scoping system's name.</span></span>

<span data-ttu-id="a943d-921">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-921">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a943d-922">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="a943d-922">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-923">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a943d-923">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-924">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-924">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a943d-925">Ora dell'ultima reimpostazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="a943d-925">Time of last printer reset.</span></span>

</dd> <dt>

<span data-ttu-id="a943d-926">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="a943d-926">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a943d-927">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a943d-927">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a943d-928">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a943d-928">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a943d-929">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. HorizontalResolution"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixel per pollice")</span><span class="sxs-lookup"><span data-stu-id="a943d-929">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="a943d-930">Risoluzione verticale in pixel per pollice.</span><span class="sxs-lookup"><span data-stu-id="a943d-930">Vertical resolution in pixels-per-inch.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a943d-931">Commenti</span><span class="sxs-lookup"><span data-stu-id="a943d-931">Remarks</span></span>

<span data-ttu-id="a943d-932">La classe **CIM \_ Printer** è derivata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-932">The **CIM\_Printer** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a943d-933">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a943d-933">WMI does not implement this class.</span></span> <span data-ttu-id="a943d-934">Per WMI con classi derivate dalla **\_ stampante CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a943d-934">For WMI classed derived from **CIM\_Printer**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a943d-935">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a943d-935">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a943d-936">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a943d-936">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a943d-937">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a943d-937">Requirements</span></span>



| <span data-ttu-id="a943d-938">Requisito</span><span class="sxs-lookup"><span data-stu-id="a943d-938">Requirement</span></span> | <span data-ttu-id="a943d-939">Valore</span><span class="sxs-lookup"><span data-stu-id="a943d-939">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a943d-940">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a943d-940">Minimum supported client</span></span><br/> | <span data-ttu-id="a943d-941">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a943d-941">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a943d-942">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a943d-942">Minimum supported server</span></span><br/> | <span data-ttu-id="a943d-943">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a943d-943">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a943d-944">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a943d-944">Namespace</span></span><br/>                | <span data-ttu-id="a943d-945">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a943d-945">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a943d-946">MOF</span><span class="sxs-lookup"><span data-stu-id="a943d-946">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a943d-947"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a943d-947"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a943d-948">DLL</span><span class="sxs-lookup"><span data-stu-id="a943d-948">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a943d-949"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a943d-949"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a943d-950">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a943d-950">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a943d-951">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="a943d-951">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

