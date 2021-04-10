---
description: La \_ classe del controller CIM è una classe padre per il raggruppamento di dispositivi correlati al controllo. Esempi di controller sono controller SCSI, controller USB e controller seriali.
ms.assetid: 526d58bb-cdf4-42c2-ae89-7b86d99e2017
ms.tgt_platform: multiple
title: Classe CIM_Controller (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Controller
- CIM_Controller.Caption
- CIM_Controller.Description
- CIM_Controller.InstallDate
- CIM_Controller.Name
- CIM_Controller.Status
- CIM_Controller.Availability
- CIM_Controller.ConfigManagerErrorCode
- CIM_Controller.ConfigManagerUserConfig
- CIM_Controller.CreationClassName
- CIM_Controller.DeviceID
- CIM_Controller.PowerManagementCapabilities
- CIM_Controller.ErrorCleared
- CIM_Controller.ErrorDescription
- CIM_Controller.LastErrorCode
- CIM_Controller.PNPDeviceID
- CIM_Controller.PowerManagementSupported
- CIM_Controller.StatusInfo
- CIM_Controller.SystemCreationClassName
- CIM_Controller.SystemName
- CIM_Controller.MaxNumberControlled
- CIM_Controller.ProtocolSupported
- CIM_Controller.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b23ef846c118c8d0698660175e4be700ea892055
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225620"
---
# <a name="cim_controller-class-cimwin32-wmi-providers"></a><span data-ttu-id="4d522-104">Classe CIM_Controller (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="4d522-104">CIM_Controller class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="4d522-105">La classe del **\_ controller CIM** è una classe padre per il raggruppamento di dispositivi correlati al controllo.</span><span class="sxs-lookup"><span data-stu-id="4d522-105">The **CIM\_Controller** class is a parent class for grouping miscellaneous control-related devices.</span></span> <span data-ttu-id="4d522-106">Esempi di controller sono controller SCSI, controller USB e controller seriali.</span><span class="sxs-lookup"><span data-stu-id="4d522-106">Examples of controllers are SCSI controllers, USB controllers, and serial controllers.</span></span>

<span data-ttu-id="4d522-107">La classe del **\_ controller CIM** è un'astrazione per i dispositivi con un singolo stack di protocolli, che esiste principalmente per la comunicazione e il controllo o la reimpostazione dei dispositivi downstream ([**CIM \_ ControlledBy**](cim-controlledby.md)).</span><span class="sxs-lookup"><span data-stu-id="4d522-107">The **CIM\_Controller** class is an abstraction for devices with a single protocol stack, which exist primarily for communication to, and control or reset of, downstream ([**CIM\_ControlledBy**](cim-controlledby.md)) devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d522-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4d522-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4d522-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4d522-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4d522-110">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4d522-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4d522-111">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="4d522-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d522-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d522-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C531-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Controller : CIM_LogicalDevice
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
  uint32   MaxNumberControlled;
  uint16   ProtocolSupported;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="4d522-113">Members</span><span class="sxs-lookup"><span data-stu-id="4d522-113">Members</span></span>

<span data-ttu-id="4d522-114">La classe del **\_ controller CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4d522-114">The **CIM\_Controller** class has these types of members:</span></span>

-   [<span data-ttu-id="4d522-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="4d522-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="4d522-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4d522-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4d522-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="4d522-117">Methods</span></span>

<span data-ttu-id="4d522-118">La classe del **\_ controller CIM** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4d522-118">The **CIM\_Controller** class has these methods.</span></span>



| <span data-ttu-id="4d522-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="4d522-119">Method</span></span>                                                                | <span data-ttu-id="4d522-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d522-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d522-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="4d522-121">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                 | <span data-ttu-id="4d522-122">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="4d522-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="4d522-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="4d522-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="4d522-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4d522-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-controller.md) | <span data-ttu-id="4d522-125">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="4d522-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="4d522-126">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="4d522-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4d522-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4d522-127">Properties</span></span>

<span data-ttu-id="4d522-128">La classe del **\_ controller CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4d522-128">The **CIM\_Controller** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d522-129">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="4d522-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-130">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d522-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-132">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="4d522-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="4d522-133">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d522-133">Availability and status of the device.</span></span>

<span data-ttu-id="4d522-134">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4d522-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="4d522-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4d522-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="4d522-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="4d522-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="4d522-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="4d522-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="4d522-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="4d522-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="4d522-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4d522-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="4d522-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="4d522-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="4d522-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="4d522-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="4d522-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="4d522-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="4d522-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4d522-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="4d522-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="4d522-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="4d522-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="4d522-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="4d522-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="4d522-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="4d522-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-148">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="4d522-148">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="4d522-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="4d522-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-150">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="4d522-150">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="4d522-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="4d522-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-152">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="4d522-152">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="4d522-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="4d522-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="4d522-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="4d522-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-155">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="4d522-155">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="4d522-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="4d522-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-157">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="4d522-157">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="4d522-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="4d522-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-159">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="4d522-159">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="4d522-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="4d522-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-161">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="4d522-161">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="4d522-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="4d522-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-163">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="4d522-163">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d522-164">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="4d522-164">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4d522-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-167">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4d522-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4d522-168">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4d522-168">A short textual description of the object.</span></span>

<span data-ttu-id="4d522-169">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d522-170">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4d522-170">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-171">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d522-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-173">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4d522-173">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4d522-174">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4d522-174">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="4d522-175">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-175">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="4d522-176">**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="4d522-176">**This device is working properly.**</span></span> <span data-ttu-id="4d522-177"> (0)</span><span class="sxs-lookup"><span data-stu-id="4d522-177">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="4d522-178">**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="4d522-178">**This device is not configured correctly.**</span></span> <span data-ttu-id="4d522-179">(1)</span><span class="sxs-lookup"><span data-stu-id="4d522-179">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4d522-180">**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d522-180">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="4d522-181">(2)</span><span class="sxs-lookup"><span data-stu-id="4d522-181">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="4d522-182">**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="4d522-182">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="4d522-183">(3)</span><span class="sxs-lookup"><span data-stu-id="4d522-183">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4d522-184">**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="4d522-184">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="4d522-185">(4)</span><span class="sxs-lookup"><span data-stu-id="4d522-185">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="4d522-186">**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="4d522-186">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="4d522-187">(5)</span><span class="sxs-lookup"><span data-stu-id="4d522-187">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="4d522-188">**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="4d522-188">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="4d522-189"> (6)</span><span class="sxs-lookup"><span data-stu-id="4d522-189">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="4d522-190">**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="4d522-190">**Cannot filter.**</span></span> <span data-ttu-id="4d522-191">(7)</span><span class="sxs-lookup"><span data-stu-id="4d522-191">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="4d522-192">**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="4d522-192">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="4d522-193">(8)</span><span class="sxs-lookup"><span data-stu-id="4d522-193">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="4d522-194">**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="4d522-194">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="4d522-195">(9)</span><span class="sxs-lookup"><span data-stu-id="4d522-195">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="4d522-196">**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d522-196">**This device cannot start.**</span></span> <span data-ttu-id="4d522-197">(10)</span><span class="sxs-lookup"><span data-stu-id="4d522-197">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="4d522-198">**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d522-198">**This device failed.**</span></span> <span data-ttu-id="4d522-199">(11)</span><span class="sxs-lookup"><span data-stu-id="4d522-199">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="4d522-200">**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="4d522-200">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="4d522-201">12</span><span class="sxs-lookup"><span data-stu-id="4d522-201">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="4d522-202">**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d522-202">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="4d522-203">(13)</span><span class="sxs-lookup"><span data-stu-id="4d522-203">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="4d522-204">**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="4d522-204">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="4d522-205">(14)</span><span class="sxs-lookup"><span data-stu-id="4d522-205">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="4d522-206">**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="4d522-206">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="4d522-207">(15)</span><span class="sxs-lookup"><span data-stu-id="4d522-207">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="4d522-208">**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d522-208">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="4d522-209">(16)</span><span class="sxs-lookup"><span data-stu-id="4d522-209">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="4d522-210">**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="4d522-210">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="4d522-211">(17)</span><span class="sxs-lookup"><span data-stu-id="4d522-211">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4d522-212">**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d522-212">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="4d522-213">(18)</span><span class="sxs-lookup"><span data-stu-id="4d522-213">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="4d522-214">**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="4d522-214">**Failure using the VxD loader.**</span></span> <span data-ttu-id="4d522-215">(19)</span><span class="sxs-lookup"><span data-stu-id="4d522-215">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4d522-216">**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="4d522-216">**Your registry might be corrupted.**</span></span> <span data-ttu-id="4d522-217">(20)</span><span class="sxs-lookup"><span data-stu-id="4d522-217">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="4d522-218">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d522-218">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="4d522-219">(21)</span><span class="sxs-lookup"><span data-stu-id="4d522-219">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="4d522-220">**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="4d522-220">**This device is disabled.**</span></span> <span data-ttu-id="4d522-221">(22)</span><span class="sxs-lookup"><span data-stu-id="4d522-221">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="4d522-222">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="4d522-222">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="4d522-223">(23)</span><span class="sxs-lookup"><span data-stu-id="4d522-223">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="4d522-224">**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="4d522-224">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="4d522-225">(24)</span><span class="sxs-lookup"><span data-stu-id="4d522-225">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4d522-226">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d522-226">**Windows is still setting up this device.**</span></span> <span data-ttu-id="4d522-227">(25)</span><span class="sxs-lookup"><span data-stu-id="4d522-227">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4d522-228">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d522-228">**Windows is still setting up this device.**</span></span> <span data-ttu-id="4d522-229">(26)</span><span class="sxs-lookup"><span data-stu-id="4d522-229">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="4d522-230">**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="4d522-230">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="4d522-231">(27)</span><span class="sxs-lookup"><span data-stu-id="4d522-231">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="4d522-232">**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="4d522-232">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="4d522-233">(28)</span><span class="sxs-lookup"><span data-stu-id="4d522-233">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="4d522-234">**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="4d522-234">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="4d522-235">(29)</span><span class="sxs-lookup"><span data-stu-id="4d522-235">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="4d522-236">**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d522-236">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="4d522-237">(30)</span><span class="sxs-lookup"><span data-stu-id="4d522-237">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4d522-238">**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d522-238">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="4d522-239">31</span><span class="sxs-lookup"><span data-stu-id="4d522-239">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4d522-240">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="4d522-240">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-241">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4d522-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-243">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4d522-243">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4d522-244">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="4d522-244">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="4d522-245">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-245">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d522-246">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4d522-246">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-247">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4d522-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-249">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4d522-249">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4d522-250">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="4d522-250">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4d522-251">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="4d522-251">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4d522-252">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-252">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d522-253">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="4d522-253">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-254">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4d522-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-255">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-256">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="4d522-256">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4d522-257">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4d522-257">A textual description of the object.</span></span>

<span data-ttu-id="4d522-258">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-258">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d522-259">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4d522-259">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-260">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4d522-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-262">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4d522-262">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4d522-263">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="4d522-263">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="4d522-264">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-264">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d522-265">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="4d522-265">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-266">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4d522-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-267">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d522-268">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="4d522-268">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="4d522-269">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-269">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d522-270">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4d522-270">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-271">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4d522-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d522-273">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="4d522-273">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="4d522-274">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-274">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d522-275">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4d522-275">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-276">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4d522-276">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-277">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-278">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="4d522-278">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4d522-279">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="4d522-279">Indicates when the object was installed.</span></span> <span data-ttu-id="4d522-280">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="4d522-280">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4d522-281">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-281">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d522-282">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4d522-282">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-283">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d522-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d522-285">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="4d522-285">Last error code reported by the logical device.</span></span>

<span data-ttu-id="4d522-286">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d522-287">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="4d522-287">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-288">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d522-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-290">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="4d522-290">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="4d522-291">Numero massimo di entità indirizzabili direttamente supportate da questo controller.</span><span class="sxs-lookup"><span data-stu-id="4d522-291">Maximum number of directly addressable entities supported by this controller.</span></span> <span data-ttu-id="4d522-292">Se il numero è sconosciuto o illimitato, è necessario utilizzare il valore 0.</span><span class="sxs-lookup"><span data-stu-id="4d522-292">A value of 0 should be used if the number is unknown or unlimited.</span></span>

</dd> <dt>

<span data-ttu-id="4d522-293">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4d522-293">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-294">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4d522-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-296">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="4d522-296">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4d522-297">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="4d522-297">Label by which the object is known.</span></span> <span data-ttu-id="4d522-298">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="4d522-298">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4d522-299">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d522-300">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="4d522-300">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-301">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4d522-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-303">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4d522-303">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4d522-304">Indica l'identificatore del dispositivo Plug and Play Win32 del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="4d522-304">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="4d522-305">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="4d522-305">Example: "\*PNP030b"</span></span>

<span data-ttu-id="4d522-306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d522-307">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4d522-307">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-308">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d522-308">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4d522-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d522-310">Indica le funzionalità specifiche relative al risparmio di energia del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="4d522-310">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="4d522-311">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4d522-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="4d522-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-313">Le capacità relative al risparmio di energia sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="4d522-313">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="4d522-314"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="4d522-314"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-315">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d522-315">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4d522-316"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="4d522-316"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-317">Le capacità correlate all'alimentazione sono state disabilitate.</span><span class="sxs-lookup"><span data-stu-id="4d522-317">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4d522-318"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="4d522-318"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-319">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="4d522-319">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="4d522-320"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="4d522-320"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-321">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="4d522-321">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="4d522-322"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="4d522-322"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-323">Il metodo **SetPowerState** è supportato.</span><span class="sxs-lookup"><span data-stu-id="4d522-323">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="4d522-324">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="4d522-324">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="4d522-325">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="4d522-325">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="4d522-326"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="4d522-326"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-327">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").</span><span class="sxs-lookup"><span data-stu-id="4d522-327">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="4d522-328"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="4d522-328"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4d522-329">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e il parametro *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="4d522-329">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d522-330">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4d522-330">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-331">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4d522-331">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d522-333">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="4d522-333">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="4d522-334">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="4d522-334">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="4d522-335">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="4d522-335">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="4d522-336">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="4d522-336">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="4d522-337">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d522-338">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="4d522-338">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-339">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d522-339">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-341">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,2 "," MIF. \|Dischi DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="4d522-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="4d522-342">Protocollo usato dal controller per accedere ai dispositivi "controllati".</span><span class="sxs-lookup"><span data-stu-id="4d522-342">The protocol used by the controller to access 'controlled' devices.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4d522-343">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="4d522-343">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4d522-344">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="4d522-344">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="4d522-345">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="4d522-345">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="4d522-346">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="4d522-346">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="4d522-347">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="4d522-347">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="4d522-348">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="4d522-348">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="4d522-349">**Dischetto flessibile** (7)</span><span class="sxs-lookup"><span data-stu-id="4d522-349">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="4d522-350">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="4d522-350">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="4d522-351">**Interfaccia parallela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="4d522-351">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="4d522-352">**Protocollo di Fibre Channel SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="4d522-352">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="4d522-353">**Protocollo bus seriale SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="4d522-353">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="4d522-354">**Protocollo bus seriale SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="4d522-354">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="4d522-355">**Architettura di archiviazione seriale SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="4d522-355">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="4d522-356">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="4d522-356">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="4d522-357">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="4d522-357">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="4d522-358">**Bus seriale universale** (16)</span><span class="sxs-lookup"><span data-stu-id="4d522-358">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="4d522-359">**Protocollo parallelo** (17)</span><span class="sxs-lookup"><span data-stu-id="4d522-359">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="4d522-360">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="4d522-360">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="4d522-361">**Diagnostica** (19)</span><span class="sxs-lookup"><span data-stu-id="4d522-361">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="4d522-362">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="4d522-362">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="4d522-363">**Potenza** (21)</span><span class="sxs-lookup"><span data-stu-id="4d522-363">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="4d522-364">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="4d522-364">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="4d522-365">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="4d522-365">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="4d522-366">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="4d522-366">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="4d522-367">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="4d522-367">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="4d522-368">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="4d522-368">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="4d522-369">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="4d522-369">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="4d522-370">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="4d522-370">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="4d522-371">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="4d522-371">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="4d522-372">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="4d522-372">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="4d522-373">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="4d522-373">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="4d522-374">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="4d522-374">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="4d522-375">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="4d522-375">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="4d522-376">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="4d522-376">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="4d522-377">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="4d522-377">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="4d522-378">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="4d522-378">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="4d522-379">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="4d522-379">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="4d522-380">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="4d522-380">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="4d522-381">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="4d522-381">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="4d522-382">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="4d522-382">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="4d522-383">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="4d522-383">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="4d522-384">**ATA/IDE avanzato** (42)</span><span class="sxs-lookup"><span data-stu-id="4d522-384">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="4d522-385">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="4d522-385">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="4d522-386">**TWIRP (infrarossi bidirezionali)** (44)</span><span class="sxs-lookup"><span data-stu-id="4d522-386">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="4d522-387">**FIR (infrarossi veloci)** (45)</span><span class="sxs-lookup"><span data-stu-id="4d522-387">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="4d522-388">**Sir (Serial Infrared)** (46)</span><span class="sxs-lookup"><span data-stu-id="4d522-388">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="4d522-389">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="4d522-389">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4d522-390">**Status**</span><span class="sxs-lookup"><span data-stu-id="4d522-390">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-391">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4d522-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-392">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-393">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="4d522-393">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4d522-394">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4d522-394">String that indicates the current status of the object.</span></span> <span data-ttu-id="4d522-395">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="4d522-395">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="4d522-396">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="4d522-396">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="4d522-397">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="4d522-397">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="4d522-398">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="4d522-398">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4d522-399">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="4d522-399">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4d522-400">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="4d522-400">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4d522-401">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4d522-402">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="4d522-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4d522-403">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="4d522-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4d522-404">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="4d522-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4d522-405">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="4d522-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4d522-406">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="4d522-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4d522-407">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="4d522-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4d522-408">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="4d522-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4d522-409">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="4d522-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4d522-410">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="4d522-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4d522-411">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="4d522-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4d522-412">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="4d522-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4d522-413">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="4d522-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4d522-414">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="4d522-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4d522-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4d522-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-416">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d522-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-417">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-418">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="4d522-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="4d522-419">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="4d522-419">State of the logical device.</span></span> <span data-ttu-id="4d522-420">Se questa proprietà non è applicabile al dispositivo logico, è necessario utilizzare il valore 5 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="4d522-420">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="4d522-421">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4d522-422">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="4d522-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4d522-423">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="4d522-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4d522-424">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="4d522-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4d522-425">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="4d522-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4d522-426">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="4d522-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4d522-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4d522-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-428">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4d522-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-429">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-430">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4d522-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4d522-431">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="4d522-431">The scoping system's creation class name.</span></span>

<span data-ttu-id="4d522-432">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d522-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4d522-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-434">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4d522-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-435">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d522-436">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4d522-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4d522-437">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="4d522-437">The scoping system's name.</span></span>

<span data-ttu-id="4d522-438">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d522-439">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="4d522-439">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d522-440">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4d522-440">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4d522-441">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d522-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d522-442">Data e ora dell'ultima reimpostazione del controller (spento o reinizializzato).</span><span class="sxs-lookup"><span data-stu-id="4d522-442">Date and time the controller was last reset (powered down or reinitialized).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d522-443">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d522-443">Remarks</span></span>

<span data-ttu-id="4d522-444">La classe del **\_ controller CIM** è derivata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-444">The **CIM\_Controller** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="4d522-445">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="4d522-445">WMI does not implement this class.</span></span> <span data-ttu-id="4d522-446">Per le classi derivate dal **\_ controller CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4d522-446">For classes derived from **CIM\_Controller**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4d522-447">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="4d522-447">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4d522-448">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="4d522-448">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d522-449">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d522-449">Requirements</span></span>



| <span data-ttu-id="4d522-450">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d522-450">Requirement</span></span> | <span data-ttu-id="4d522-451">Valore</span><span class="sxs-lookup"><span data-stu-id="4d522-451">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d522-452">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d522-452">Minimum supported client</span></span><br/> | <span data-ttu-id="4d522-453">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d522-453">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4d522-454">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d522-454">Minimum supported server</span></span><br/> | <span data-ttu-id="4d522-455">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d522-455">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4d522-456">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4d522-456">Namespace</span></span><br/>                | <span data-ttu-id="4d522-457">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4d522-457">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4d522-458">MOF</span><span class="sxs-lookup"><span data-stu-id="4d522-458">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d522-459"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d522-459"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d522-460">DLL</span><span class="sxs-lookup"><span data-stu-id="4d522-460">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d522-461"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d522-461"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d522-462">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d522-462">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d522-463">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4d522-463">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

