---
description: La \_ classe CIM POTSModem rappresenta un dispositivo che converte i dati binari in modulazioni Wave per la trasmissione basata su audio connettendosi alla rete Plain Old Phone System (POTS).
ms.assetid: 2740f305-769d-464c-910a-998522f5121b
ms.tgt_platform: multiple
title: Classe CIM_POTSModem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_POTSModem
- CIM_POTSModem.AnswerMode
- CIM_POTSModem.Availability
- CIM_POTSModem.Caption
- CIM_POTSModem.CompressionInfo
- CIM_POTSModem.ConfigManagerErrorCode
- CIM_POTSModem.ConfigManagerUserConfig
- CIM_POTSModem.CountriesSupported
- CIM_POTSModem.CountrySelected
- CIM_POTSModem.CreationClassName
- CIM_POTSModem.CurrentPasswords
- CIM_POTSModem.Description
- CIM_POTSModem.DeviceID
- CIM_POTSModem.DialType
- CIM_POTSModem.ErrorCleared
- CIM_POTSModem.ErrorControlInfo
- CIM_POTSModem.ErrorDescription
- CIM_POTSModem.InactivityTimeout
- CIM_POTSModem.InstallDate
- CIM_POTSModem.LastErrorCode
- CIM_POTSModem.MaxBaudRateToPhone
- CIM_POTSModem.MaxBaudRateToSerialPort
- CIM_POTSModem.MaxNumberOfPasswords
- CIM_POTSModem.ModulationScheme
- CIM_POTSModem.Name
- CIM_POTSModem.PNPDeviceID
- CIM_POTSModem.PowerManagementCapabilities
- CIM_POTSModem.PowerManagementSupported
- CIM_POTSModem.RingsBeforeAnswer
- CIM_POTSModem.SpeakerVolumeInfo
- CIM_POTSModem.Status
- CIM_POTSModem.StatusInfo
- CIM_POTSModem.SupportsCallback
- CIM_POTSModem.SupportsSynchronousConnect
- CIM_POTSModem.SystemCreationClassName
- CIM_POTSModem.SystemName
- CIM_POTSModem.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7fbaeedd1de4006dfdccbcec313a7428d7b7f03
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966187"
---
# <a name="cim_potsmodem-class"></a><span data-ttu-id="5827f-103">CIM \_ POTSModem (classe)</span><span class="sxs-lookup"><span data-stu-id="5827f-103">CIM\_POTSModem class</span></span>

<span data-ttu-id="5827f-104">La classe **CIM \_ POTSModem** rappresenta un dispositivo che converte i dati binari in modulazioni Wave per la trasmissione basata su audio connettendosi alla rete Plain Old Phone System (POTS).</span><span class="sxs-lookup"><span data-stu-id="5827f-104">The **CIM\_POTSModem** class represents a device that translates binary data into wave modulations for sound-based transmission by connecting to the Plain Old Telephone System (POTS) network.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5827f-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="5827f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5827f-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5827f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5827f-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5827f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5827f-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5827f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5827f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5827f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C546-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_POTSModem : CIM_LogicalDevice
{
  uint16   AnswerMode;
  uint16   Availability;
  string   Caption;
  uint16   CompressionInfo;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CountriesSupported[];
  string   CountrySelected;
  string   CreationClassName;
  string   CurrentPasswords[];
  string   Description;
  string   DeviceID;
  uint16   DialType;
  boolean  ErrorCleared;
  uint16   ErrorControlInfo;
  string   ErrorDescription;
  uint32   InactivityTimeout;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRateToPhone;
  uint32   MaxBaudRateToSerialPort;
  uint16   MaxNumberOfPasswords;
  uint16   ModulationScheme;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint8    RingsBeforeAnswer;
  uint16   SpeakerVolumeInfo;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsCallback;
  boolean  SupportsSynchronousConnect;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="5827f-110">Members</span><span class="sxs-lookup"><span data-stu-id="5827f-110">Members</span></span>

<span data-ttu-id="5827f-111">La classe **CIM \_ POTSModem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5827f-111">The **CIM\_POTSModem** class has these types of members:</span></span>

-   [<span data-ttu-id="5827f-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="5827f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="5827f-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5827f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5827f-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="5827f-114">Methods</span></span>

<span data-ttu-id="5827f-115">La classe **CIM \_ POTSModem** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5827f-115">The **CIM\_POTSModem** class has these methods.</span></span>



| <span data-ttu-id="5827f-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="5827f-116">Method</span></span>                                                               | <span data-ttu-id="5827f-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5827f-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5827f-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="5827f-118">**Reset**</span></span>](reset-method-in-class-cim-potsmodem.md)                 | <span data-ttu-id="5827f-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5827f-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="5827f-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="5827f-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="5827f-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5827f-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-potsmodem.md) | <span data-ttu-id="5827f-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="5827f-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="5827f-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="5827f-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5827f-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5827f-124">Properties</span></span>

<span data-ttu-id="5827f-125">La classe **CIM \_ POTSModem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5827f-125">The **CIM\_POTSModem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5827f-126">**AnswerMode**</span><span class="sxs-lookup"><span data-stu-id="5827f-126">**AnswerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5827f-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-129">Impostazione della risposta automatica o della chiamata per il modem corrente.</span><span class="sxs-lookup"><span data-stu-id="5827f-129">Current auto-answer or call-back setting for the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5827f-130">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5827f-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5827f-131">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5827f-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5827f-132">**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="5827f-132">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

<span data-ttu-id="5827f-133">**Risposta manuale** (3)</span><span class="sxs-lookup"><span data-stu-id="5827f-133">**Manual Answer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

<span data-ttu-id="5827f-134">**Risposta automatica** (4)</span><span class="sxs-lookup"><span data-stu-id="5827f-134">**Auto Answer** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

<span data-ttu-id="5827f-135">**Risposta automatica con Call-back** (5)</span><span class="sxs-lookup"><span data-stu-id="5827f-135">**Auto Answer with Call-Back** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5827f-136">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="5827f-136">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-137">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5827f-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-139">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="5827f-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="5827f-140">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5827f-140">Availability and status of the device.</span></span>

<span data-ttu-id="5827f-141">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-141">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5827f-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5827f-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5827f-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="5827f-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="5827f-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="5827f-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="5827f-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="5827f-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="5827f-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="5827f-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5827f-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="5827f-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="5827f-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="5827f-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="5827f-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="5827f-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="5827f-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="5827f-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5827f-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="5827f-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="5827f-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="5827f-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="5827f-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="5827f-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="5827f-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="5827f-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-155">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="5827f-155">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="5827f-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="5827f-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-157">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="5827f-157">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="5827f-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="5827f-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-159">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="5827f-159">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="5827f-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="5827f-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="5827f-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="5827f-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-162">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="5827f-162">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="5827f-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="5827f-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-164">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="5827f-164">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="5827f-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="5827f-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-166">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="5827f-166">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="5827f-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="5827f-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-168">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="5827f-168">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="5827f-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="5827f-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-170">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="5827f-170">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5827f-171">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="5827f-171">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5827f-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-174">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5827f-174">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5827f-175">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5827f-175">Short textual description of the object.</span></span>

<span data-ttu-id="5827f-176">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5827f-177">**CompressionInfo**</span><span class="sxs-lookup"><span data-stu-id="5827f-177">**CompressionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-178">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5827f-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-180">Caratteristiche di compressione dei dati del modem.</span><span class="sxs-lookup"><span data-stu-id="5827f-180">Data compression characteristics of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5827f-181">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5827f-181">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5827f-182">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5827f-182">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span data-ttu-id="5827f-183">**Nessuna compressione** (2)</span><span class="sxs-lookup"><span data-stu-id="5827f-183">**No Compression** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span data-ttu-id="5827f-184">**MNP 5** (3)</span><span class="sxs-lookup"><span data-stu-id="5827f-184">**MNP 5** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span data-ttu-id="5827f-185">**V. 42bis** (4)</span><span class="sxs-lookup"><span data-stu-id="5827f-185">**V.42bis** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5827f-186">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5827f-186">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-187">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5827f-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-189">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5827f-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5827f-190">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5827f-190">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="5827f-191">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-191">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="5827f-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="5827f-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="5827f-193"> (0)</span><span class="sxs-lookup"><span data-stu-id="5827f-193">(0)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-194">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="5827f-194">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="5827f-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="5827f-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="5827f-196">(1)</span><span class="sxs-lookup"><span data-stu-id="5827f-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-197">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="5827f-197">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5827f-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5827f-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="5827f-199">(2)</span><span class="sxs-lookup"><span data-stu-id="5827f-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="5827f-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="5827f-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="5827f-201">(3)</span><span class="sxs-lookup"><span data-stu-id="5827f-201">(3)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-202">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="5827f-202">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5827f-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="5827f-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="5827f-204">(4)</span><span class="sxs-lookup"><span data-stu-id="5827f-204">(4)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-205">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="5827f-205">Device is not working properly.</span></span> <span data-ttu-id="5827f-206">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="5827f-206">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="5827f-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="5827f-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="5827f-208">(5)</span><span class="sxs-lookup"><span data-stu-id="5827f-208">(5)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-209">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="5827f-209">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="5827f-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="5827f-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="5827f-211"> (6)</span><span class="sxs-lookup"><span data-stu-id="5827f-211">(6)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-212">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="5827f-212">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="5827f-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="5827f-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="5827f-214">(7)</span><span class="sxs-lookup"><span data-stu-id="5827f-214">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="5827f-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="5827f-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="5827f-216">(8)</span><span class="sxs-lookup"><span data-stu-id="5827f-216">(8)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-217">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="5827f-217">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="5827f-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="5827f-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="5827f-219">(9)</span><span class="sxs-lookup"><span data-stu-id="5827f-219">(9)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-220">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="5827f-220">Device is not working properly.</span></span> <span data-ttu-id="5827f-221">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5827f-221">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="5827f-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5827f-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="5827f-223">(10)</span><span class="sxs-lookup"><span data-stu-id="5827f-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-224">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5827f-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="5827f-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5827f-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="5827f-226">(11)</span><span class="sxs-lookup"><span data-stu-id="5827f-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-227">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5827f-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="5827f-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="5827f-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="5827f-229">12</span><span class="sxs-lookup"><span data-stu-id="5827f-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-230">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="5827f-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="5827f-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5827f-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="5827f-232">(13)</span><span class="sxs-lookup"><span data-stu-id="5827f-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-233">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5827f-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="5827f-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="5827f-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="5827f-235">(14)</span><span class="sxs-lookup"><span data-stu-id="5827f-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-236">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="5827f-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="5827f-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="5827f-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="5827f-238">(15)</span><span class="sxs-lookup"><span data-stu-id="5827f-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-239">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="5827f-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="5827f-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5827f-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="5827f-241">(16)</span><span class="sxs-lookup"><span data-stu-id="5827f-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-242">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5827f-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="5827f-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="5827f-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="5827f-244">(17)</span><span class="sxs-lookup"><span data-stu-id="5827f-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-245">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="5827f-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5827f-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5827f-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="5827f-247">(18)</span><span class="sxs-lookup"><span data-stu-id="5827f-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-248">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5827f-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="5827f-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="5827f-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="5827f-250">(19)</span><span class="sxs-lookup"><span data-stu-id="5827f-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5827f-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="5827f-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="5827f-252">(20)</span><span class="sxs-lookup"><span data-stu-id="5827f-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-253">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="5827f-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="5827f-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5827f-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="5827f-255">(21)</span><span class="sxs-lookup"><span data-stu-id="5827f-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-256">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="5827f-256">System failure.</span></span> <span data-ttu-id="5827f-257">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="5827f-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="5827f-258">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5827f-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="5827f-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="5827f-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="5827f-260">(22)</span><span class="sxs-lookup"><span data-stu-id="5827f-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-261">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="5827f-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="5827f-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="5827f-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="5827f-263">(23)</span><span class="sxs-lookup"><span data-stu-id="5827f-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-264">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="5827f-264">System failure.</span></span> <span data-ttu-id="5827f-265">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="5827f-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="5827f-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="5827f-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="5827f-267">(24)</span><span class="sxs-lookup"><span data-stu-id="5827f-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-268">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="5827f-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5827f-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5827f-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5827f-270">(25)</span><span class="sxs-lookup"><span data-stu-id="5827f-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-271">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5827f-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5827f-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5827f-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5827f-273">(26)</span><span class="sxs-lookup"><span data-stu-id="5827f-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-274">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5827f-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="5827f-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="5827f-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="5827f-276">(27)</span><span class="sxs-lookup"><span data-stu-id="5827f-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-277">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="5827f-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="5827f-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="5827f-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="5827f-279">(28)</span><span class="sxs-lookup"><span data-stu-id="5827f-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-280">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="5827f-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="5827f-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="5827f-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="5827f-282">(29)</span><span class="sxs-lookup"><span data-stu-id="5827f-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-283">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="5827f-283">Device is disabled.</span></span> <span data-ttu-id="5827f-284">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="5827f-284">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="5827f-285"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5827f-285"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="5827f-286">(30)</span><span class="sxs-lookup"><span data-stu-id="5827f-286">(30)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-287">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5827f-287">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5827f-288"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5827f-288"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="5827f-289">31</span><span class="sxs-lookup"><span data-stu-id="5827f-289">(31)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-290">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="5827f-290">Device is not working properly.</span></span> <span data-ttu-id="5827f-291">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="5827f-291">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5827f-292">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="5827f-292">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-293">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5827f-293">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-295">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5827f-295">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5827f-296">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="5827f-296">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="5827f-297">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5827f-298">**CountriesSupported**</span><span class="sxs-lookup"><span data-stu-id="5827f-298">**CountriesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-299">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="5827f-299">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5827f-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-301">Paesi o aree geografiche in cui il modem può funzionare.</span><span class="sxs-lookup"><span data-stu-id="5827f-301">Countries or regions in which the modem can operate.</span></span>

</dd> <dt>

<span data-ttu-id="5827f-302">**CountrySelected**</span><span class="sxs-lookup"><span data-stu-id="5827f-302">**CountrySelected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-303">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5827f-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-305">Paese o area geografica del modem attualmente programmato.</span><span class="sxs-lookup"><span data-stu-id="5827f-305">Country or region for which the modem is currently programmed.</span></span> <span data-ttu-id="5827f-306">Quando sono supportati più paesi o aree geografiche, questa proprietà definisce quello attualmente selezionato per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="5827f-306">When multiple countries or regions are supported, this property defines which one is currently selected for use.</span></span>

</dd> <dt>

<span data-ttu-id="5827f-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5827f-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-308">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5827f-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-310">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5827f-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5827f-311">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="5827f-311">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5827f-312">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="5827f-312">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5827f-313">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5827f-314">**CurrentPasswords**</span><span class="sxs-lookup"><span data-stu-id="5827f-314">**CurrentPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-315">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="5827f-315">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5827f-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-317">Password attualmente definite per il modem.</span><span class="sxs-lookup"><span data-stu-id="5827f-317">Currently defined passwords for the modem.</span></span> <span data-ttu-id="5827f-318">Questa matrice può essere lasciata vuota per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="5827f-318">This array can be left blank for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="5827f-319">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5827f-319">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-320">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5827f-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-322">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="5827f-322">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5827f-323">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5827f-323">Textual description of the object.</span></span>

<span data-ttu-id="5827f-324">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-324">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5827f-325">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5827f-325">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-326">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5827f-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-328">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5827f-328">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5827f-329">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5827f-329">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="5827f-330">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5827f-331">**DialType**</span><span class="sxs-lookup"><span data-stu-id="5827f-331">**DialType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-332">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5827f-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-334">Tipo di connessione utilizzato.</span><span class="sxs-lookup"><span data-stu-id="5827f-334">Type of dialing that is used.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5827f-335">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5827f-335">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

<span data-ttu-id="5827f-336">**Tono** (1)</span><span class="sxs-lookup"><span data-stu-id="5827f-336">**Tone** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

<span data-ttu-id="5827f-337">**Impulsi** (2)</span><span class="sxs-lookup"><span data-stu-id="5827f-337">**Pulse** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5827f-338">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5827f-338">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-339">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5827f-339">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-341">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="5827f-341">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="5827f-342">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-342">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5827f-343">**ErrorControlInfo**</span><span class="sxs-lookup"><span data-stu-id="5827f-343">**ErrorControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-344">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5827f-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-346">Caratteristiche di correzione degli errori del modem.</span><span class="sxs-lookup"><span data-stu-id="5827f-346">Error correction characteristics of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5827f-347">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5827f-347">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5827f-348">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5827f-348">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

<span data-ttu-id="5827f-349">**Nessuna correzione errori** (2)</span><span class="sxs-lookup"><span data-stu-id="5827f-349">**No Error Correction** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

<span data-ttu-id="5827f-350">**MNP 4** (3)</span><span class="sxs-lookup"><span data-stu-id="5827f-350">**MNP 4** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

<span data-ttu-id="5827f-351">**LAPM** (4)</span><span class="sxs-lookup"><span data-stu-id="5827f-351">**LAPM** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5827f-352">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5827f-352">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-353">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5827f-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-355">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="5827f-355">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="5827f-356">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5827f-357">**InactivityTimeout**</span><span class="sxs-lookup"><span data-stu-id="5827f-357">**InactivityTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-358">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5827f-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-360">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("secondi")</span><span class="sxs-lookup"><span data-stu-id="5827f-360">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="5827f-361">Limite di tempo (in secondi) per la disconnessione automatica della linea telefonica se non vengono scambiati dati.</span><span class="sxs-lookup"><span data-stu-id="5827f-361">Time limit (in seconds) for automatic disconnection of the phone line if no data is exchanged.</span></span> <span data-ttu-id="5827f-362">Il valore 0 (zero) indica che questa funzionalità è presente ma non abilitata.</span><span class="sxs-lookup"><span data-stu-id="5827f-362">A value of 0 (zero) indicates that this feature is present but not enabled.</span></span>

</dd> <dt>

<span data-ttu-id="5827f-363">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5827f-363">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-364">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5827f-364">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-366">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="5827f-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5827f-367">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5827f-367">Date and time the object was installed.</span></span> <span data-ttu-id="5827f-368">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="5827f-368">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5827f-369">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-369">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5827f-370">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5827f-370">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-371">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5827f-371">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-373">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5827f-373">Last error code reported by the logical device.</span></span>

<span data-ttu-id="5827f-374">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5827f-375">**MaxBaudRateToPhone**</span><span class="sxs-lookup"><span data-stu-id="5827f-375">**MaxBaudRateToPhone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-376">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5827f-376">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-378">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="5827f-378">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="5827f-379">Velocità di comunicazione massima impostabile per l'accesso al sistema telefonico.</span><span class="sxs-lookup"><span data-stu-id="5827f-379">Maximum settable communication speed for accessing the phone system.</span></span>

</dd> <dt>

<span data-ttu-id="5827f-380">**MaxBaudRateToSerialPort**</span><span class="sxs-lookup"><span data-stu-id="5827f-380">**MaxBaudRateToSerialPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-381">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5827f-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-383">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="5827f-383">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="5827f-384">Velocità di comunicazione massima impostabile per la porta COM per un modem esterno.</span><span class="sxs-lookup"><span data-stu-id="5827f-384">Maximum settable communication speed to the COM port for an external modem.</span></span> <span data-ttu-id="5827f-385">Immettere 0 (zero) se non è applicabile.</span><span class="sxs-lookup"><span data-stu-id="5827f-385">Enter 0 (zero) if not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="5827f-386">**MaxNumberOfPasswords**</span><span class="sxs-lookup"><span data-stu-id="5827f-386">**MaxNumberOfPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-387">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5827f-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-389">Numero massimo di password definibili nel modem.</span><span class="sxs-lookup"><span data-stu-id="5827f-389">Maximum number of passwords definable in the modem itself.</span></span> <span data-ttu-id="5827f-390">Se questa funzionalità non è supportata, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="5827f-390">If this feature is not supported, enter 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="5827f-391">**ModulationScheme**</span><span class="sxs-lookup"><span data-stu-id="5827f-391">**ModulationScheme**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-392">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5827f-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-394">Schema di modulazione del modem.</span><span class="sxs-lookup"><span data-stu-id="5827f-394">Modulation scheme of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5827f-395">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5827f-395">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5827f-396">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5827f-396">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5827f-397">**Non supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="5827f-397">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

<span data-ttu-id="5827f-398">**Campana 103** (3)</span><span class="sxs-lookup"><span data-stu-id="5827f-398">**Bell 103** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

<span data-ttu-id="5827f-399">**Bell 212A** (4)</span><span class="sxs-lookup"><span data-stu-id="5827f-399">**Bell 212A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

<span data-ttu-id="5827f-400">**V. 22bis** (5)</span><span class="sxs-lookup"><span data-stu-id="5827f-400">**V.22bis** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

<span data-ttu-id="5827f-401">**V. 32** (6)</span><span class="sxs-lookup"><span data-stu-id="5827f-401">**V.32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

<span data-ttu-id="5827f-402">**V. 32bis** (7)</span><span class="sxs-lookup"><span data-stu-id="5827f-402">**V.32bis** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

<span data-ttu-id="5827f-403">**V. Turbo** (8)</span><span class="sxs-lookup"><span data-stu-id="5827f-403">**V.turbo** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

<span data-ttu-id="5827f-404">**V. FC** (9)</span><span class="sxs-lookup"><span data-stu-id="5827f-404">**V.FC** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

<span data-ttu-id="5827f-405">**V. 34** (10)</span><span class="sxs-lookup"><span data-stu-id="5827f-405">**V.34** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

<span data-ttu-id="5827f-406">**V. 34bis** (11)</span><span class="sxs-lookup"><span data-stu-id="5827f-406">**V.34bis** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5827f-407">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5827f-407">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-408">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5827f-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-409">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-410">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5827f-410">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5827f-411">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="5827f-411">Label by which the object is known.</span></span> <span data-ttu-id="5827f-412">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="5827f-412">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5827f-413">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-413">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5827f-414">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="5827f-414">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-415">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5827f-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-417">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5827f-417">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5827f-418">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5827f-418">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="5827f-419">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="5827f-420">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="5827f-420">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="5827f-421">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5827f-421">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-422">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5827f-422">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5827f-423">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-424">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5827f-424">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="5827f-425">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="5827f-425">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5827f-426"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5827f-426"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5827f-427"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="5827f-427"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5827f-428"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="5827f-428"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5827f-429"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="5827f-429"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-430">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="5827f-430">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="5827f-431"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="5827f-431"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-432">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="5827f-432">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="5827f-433"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="5827f-433"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-434">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="5827f-434">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="5827f-435">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="5827f-435">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="5827f-436">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="5827f-436">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="5827f-437"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="5827f-437"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-438">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="5827f-438">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="5827f-439"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="5827f-439"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5827f-440">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="5827f-440">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5827f-441">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5827f-441">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-442">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5827f-442">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-443">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-444">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="5827f-444">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="5827f-445">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="5827f-445">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="5827f-446">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="5827f-446">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="5827f-447">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="5827f-447">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="5827f-448">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-448">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5827f-449">**RingsBeforeAnswer**</span><span class="sxs-lookup"><span data-stu-id="5827f-449">**RingsBeforeAnswer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-450">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5827f-450">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-451">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-452">Numero di anelli prima che il modem risponda a una chiamata in ingresso.</span><span class="sxs-lookup"><span data-stu-id="5827f-452">Number of rings before the modem answers an incoming call.</span></span>

</dd> <dt>

<span data-ttu-id="5827f-453">**SpeakerVolumeInfo**</span><span class="sxs-lookup"><span data-stu-id="5827f-453">**SpeakerVolumeInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-454">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5827f-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-455">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-456">Livello del volume dei toni acustici dal modem.</span><span class="sxs-lookup"><span data-stu-id="5827f-456">Volume level of the audible tones from the modem.</span></span> <span data-ttu-id="5827f-457">Ad esempio, è possibile segnalare un volume elevato, medio o basso.</span><span class="sxs-lookup"><span data-stu-id="5827f-457">For example, high, medium, or low volume can be reported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5827f-458">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5827f-458">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5827f-459">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5827f-459">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5827f-460">**Non supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="5827f-460">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="5827f-461">**Alta** (3)</span><span class="sxs-lookup"><span data-stu-id="5827f-461">**High** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="5827f-462">**Media** (4)</span><span class="sxs-lookup"><span data-stu-id="5827f-462">**Medium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="5827f-463">**Bassa** (5)</span><span class="sxs-lookup"><span data-stu-id="5827f-463">**Low** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="5827f-464">**Disattivato** (6)</span><span class="sxs-lookup"><span data-stu-id="5827f-464">**Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="5827f-465">**Automatico** (7)</span><span class="sxs-lookup"><span data-stu-id="5827f-465">**Auto** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5827f-466">**Status**</span><span class="sxs-lookup"><span data-stu-id="5827f-466">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-467">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5827f-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-468">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-469">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5827f-469">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5827f-470">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5827f-470">Current status of the object.</span></span> <span data-ttu-id="5827f-471">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-471">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5827f-472">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="5827f-472">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5827f-473">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5827f-473">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5827f-474">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="5827f-474">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5827f-475">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="5827f-475">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5827f-476">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="5827f-476">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5827f-477">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="5827f-477">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5827f-478">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="5827f-478">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5827f-479">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="5827f-479">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5827f-480">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="5827f-480">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5827f-481">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="5827f-481">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5827f-482">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="5827f-482">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5827f-483">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="5827f-483">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5827f-484">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="5827f-484">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5827f-485">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5827f-485">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-486">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5827f-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-487">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-488">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="5827f-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5827f-489">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5827f-489">State of the logical device.</span></span> <span data-ttu-id="5827f-490">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="5827f-490">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="5827f-491">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5827f-492">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5827f-492">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5827f-493">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="5827f-493">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5827f-494">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="5827f-494">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5827f-495">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="5827f-495">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5827f-496">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="5827f-496">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5827f-497">**SupportsCallback**</span><span class="sxs-lookup"><span data-stu-id="5827f-497">**SupportsCallback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-498">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5827f-498">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-499">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-500">Se **true**, il modem supporta il call-back.</span><span class="sxs-lookup"><span data-stu-id="5827f-500">If **TRUE**, the modem supports call-back.</span></span>

</dd> <dt>

<span data-ttu-id="5827f-501">**SupportsSynchronousConnect**</span><span class="sxs-lookup"><span data-stu-id="5827f-501">**SupportsSynchronousConnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-502">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5827f-502">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-503">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-504">Se **true**, sincrona e asincrona, la comunicazione è supportata.</span><span class="sxs-lookup"><span data-stu-id="5827f-504">If **TRUE**, synchronous, as well as asynchronous, communication is supported.</span></span>

</dd> <dt>

<span data-ttu-id="5827f-505">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5827f-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-506">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5827f-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-507">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-508">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5827f-508">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5827f-509">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="5827f-509">Scoping system's creation class name.</span></span>

<span data-ttu-id="5827f-510">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5827f-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5827f-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-512">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5827f-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-513">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5827f-514">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5827f-514">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5827f-515">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="5827f-515">Scoping system's name.</span></span>

<span data-ttu-id="5827f-516">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5827f-517">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="5827f-517">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5827f-518">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5827f-518">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5827f-519">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5827f-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5827f-520">Data e ora dell'ultima reimpostazione del controller.</span><span class="sxs-lookup"><span data-stu-id="5827f-520">Date and time this controller was last reset.</span></span> <span data-ttu-id="5827f-521">Questo potrebbe significare che il controller è stato spento o reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="5827f-521">This could mean the controller was powered down, or reinitialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5827f-522">Commenti</span><span class="sxs-lookup"><span data-stu-id="5827f-522">Remarks</span></span>

<span data-ttu-id="5827f-523">La classe **CIM \_ POTSModem** è derivata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-523">The **CIM\_POTSModem** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="5827f-524">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="5827f-524">WMI does not implement this class.</span></span> <span data-ttu-id="5827f-525">Per le classi WMI derivate da **CIM \_ POTSModem**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5827f-525">For WMI classes derived from **CIM\_POTSModem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5827f-526">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="5827f-526">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5827f-527">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="5827f-527">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5827f-528">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5827f-528">Requirements</span></span>



| <span data-ttu-id="5827f-529">Requisito</span><span class="sxs-lookup"><span data-stu-id="5827f-529">Requirement</span></span> | <span data-ttu-id="5827f-530">Valore</span><span class="sxs-lookup"><span data-stu-id="5827f-530">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5827f-531">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5827f-531">Minimum supported client</span></span><br/> | <span data-ttu-id="5827f-532">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5827f-532">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5827f-533">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5827f-533">Minimum supported server</span></span><br/> | <span data-ttu-id="5827f-534">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5827f-534">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5827f-535">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5827f-535">Namespace</span></span><br/>                | <span data-ttu-id="5827f-536">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5827f-536">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5827f-537">MOF</span><span class="sxs-lookup"><span data-stu-id="5827f-537">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5827f-538"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5827f-538"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5827f-539">DLL</span><span class="sxs-lookup"><span data-stu-id="5827f-539">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5827f-540"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5827f-540"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5827f-541">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5827f-541">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5827f-542">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="5827f-542">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

