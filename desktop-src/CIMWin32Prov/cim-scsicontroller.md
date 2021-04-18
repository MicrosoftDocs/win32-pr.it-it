---
description: La \_ classe CIM controller SCSI rappresenta le funzionalità e la gestione del dispositivo logico del controller SCSI.
ms.assetid: a9b3dee4-1e42-4ac3-8c67-1da46f8acb43
ms.tgt_platform: multiple
title: Classe CIM_SCSIController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIController
- CIM_SCSIController.Availability
- CIM_SCSIController.Caption
- CIM_SCSIController.ConfigManagerErrorCode
- CIM_SCSIController.ConfigManagerUserConfig
- CIM_SCSIController.ControllerTimeouts
- CIM_SCSIController.CreationClassName
- CIM_SCSIController.Description
- CIM_SCSIController.DeviceID
- CIM_SCSIController.ErrorCleared
- CIM_SCSIController.ErrorDescription
- CIM_SCSIController.InstallDate
- CIM_SCSIController.LastErrorCode
- CIM_SCSIController.MaxDataWidth
- CIM_SCSIController.MaxNumberControlled
- CIM_SCSIController.MaxTransferRate
- CIM_SCSIController.Name
- CIM_SCSIController.PNPDeviceID
- CIM_SCSIController.PowerManagementCapabilities
- CIM_SCSIController.PowerManagementSupported
- CIM_SCSIController.ProtectionManagement
- CIM_SCSIController.ProtocolSupported
- CIM_SCSIController.Status
- CIM_SCSIController.StatusInfo
- CIM_SCSIController.SystemCreationClassName
- CIM_SCSIController.SystemName
- CIM_SCSIController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0523f436081a8b09f562d19d1d337fc1b7574b62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304492"
---
# <a name="cim_scsicontroller-class"></a><span data-ttu-id="9c209-103">CIM \_ controller SCSI (classe)</span><span class="sxs-lookup"><span data-stu-id="9c209-103">CIM\_SCSIController class</span></span>

<span data-ttu-id="9c209-104">La classe **CIM \_ controller SCSI** rappresenta le funzionalità e la gestione del dispositivo logico del controller SCSI.</span><span class="sxs-lookup"><span data-stu-id="9c209-104">The **CIM\_SCSIController** class represents the capabilities and management of the SCSI controller logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9c209-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="9c209-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9c209-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9c209-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9c209-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9c209-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9c209-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="9c209-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c209-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c209-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C553-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SCSIController : CIM_Controller
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  uint32   ControllerTimeouts;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxDataWidth;
  uint32   MaxNumberControlled;
  uint64   MaxTransferRate;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtectionManagement;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="9c209-110">Members</span><span class="sxs-lookup"><span data-stu-id="9c209-110">Members</span></span>

<span data-ttu-id="9c209-111">La classe **CIM \_ controller SCSI** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9c209-111">The **CIM\_SCSIController** class has these types of members:</span></span>

-   [<span data-ttu-id="9c209-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="9c209-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9c209-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9c209-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9c209-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="9c209-114">Methods</span></span>

<span data-ttu-id="9c209-115">La classe **CIM \_ controller SCSI** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9c209-115">The **CIM\_SCSIController** class has these methods.</span></span>



| <span data-ttu-id="9c209-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="9c209-116">Method</span></span>                                                                    | <span data-ttu-id="9c209-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c209-117">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c209-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="9c209-118">**Reset**</span></span>](reset-method-in-class-cim-scsicontroller.md)                 | <span data-ttu-id="9c209-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9c209-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="9c209-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="9c209-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="9c209-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9c209-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-scsicontroller.md) | <span data-ttu-id="9c209-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="9c209-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="9c209-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="9c209-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9c209-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9c209-124">Properties</span></span>

<span data-ttu-id="9c209-125">La classe **CIM \_ controller SCSI** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9c209-125">The **CIM\_SCSIController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c209-126">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="9c209-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c209-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-129">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="9c209-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9c209-130">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c209-130">Availability and status of the device.</span></span>

<span data-ttu-id="9c209-131">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9c209-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9c209-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c209-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="9c209-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9c209-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="9c209-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-135">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="9c209-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9c209-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="9c209-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9c209-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="9c209-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9c209-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="9c209-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9c209-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="9c209-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9c209-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="9c209-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9c209-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="9c209-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9c209-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="9c209-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9c209-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="9c209-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9c209-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="9c209-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9c209-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="9c209-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-146">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="9c209-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9c209-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="9c209-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-148">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="9c209-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9c209-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="9c209-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-150">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="9c209-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9c209-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="9c209-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9c209-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="9c209-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-153">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="9c209-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9c209-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="9c209-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-155">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="9c209-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9c209-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="9c209-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-157">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="9c209-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9c209-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="9c209-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-159">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="9c209-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9c209-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="9c209-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-161">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="9c209-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c209-162">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="9c209-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c209-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-165">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9c209-165">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9c209-166">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9c209-166">Short textual description of the object.</span></span>

<span data-ttu-id="9c209-167">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c209-168">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9c209-168">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-169">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c209-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-171">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9c209-171">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9c209-172">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9c209-172">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="9c209-173">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-173">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9c209-174"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="9c209-174"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="9c209-175"> (0)</span><span class="sxs-lookup"><span data-stu-id="9c209-175">(0)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-176">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9c209-176">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9c209-177"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="9c209-177"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="9c209-178">(1)</span><span class="sxs-lookup"><span data-stu-id="9c209-178">(1)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-179">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="9c209-179">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9c209-180"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c209-180"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9c209-181">(2)</span><span class="sxs-lookup"><span data-stu-id="9c209-181">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9c209-182"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="9c209-182"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9c209-183">(3)</span><span class="sxs-lookup"><span data-stu-id="9c209-183">(3)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-184">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="9c209-184">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9c209-185"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="9c209-185"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9c209-186">(4)</span><span class="sxs-lookup"><span data-stu-id="9c209-186">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-187">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9c209-187">Device is not working properly.</span></span> <span data-ttu-id="9c209-188">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="9c209-188">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9c209-189"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="9c209-189"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9c209-190">(5)</span><span class="sxs-lookup"><span data-stu-id="9c209-190">(5)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-191">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="9c209-191">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9c209-192"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="9c209-192"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9c209-193"> (6)</span><span class="sxs-lookup"><span data-stu-id="9c209-193">(6)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-194">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="9c209-194">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9c209-195"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="9c209-195"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="9c209-196">(7)</span><span class="sxs-lookup"><span data-stu-id="9c209-196">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9c209-197"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="9c209-197"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9c209-198">(8)</span><span class="sxs-lookup"><span data-stu-id="9c209-198">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-199">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="9c209-199">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9c209-200"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="9c209-200"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9c209-201">(9)</span><span class="sxs-lookup"><span data-stu-id="9c209-201">(9)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-202">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9c209-202">Device is not working properly.</span></span> <span data-ttu-id="9c209-203">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c209-203">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9c209-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c209-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="9c209-205">(10)</span><span class="sxs-lookup"><span data-stu-id="9c209-205">(10)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-206">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c209-206">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9c209-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c209-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="9c209-208">(11)</span><span class="sxs-lookup"><span data-stu-id="9c209-208">(11)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-209">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c209-209">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9c209-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="9c209-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9c209-211">12</span><span class="sxs-lookup"><span data-stu-id="9c209-211">(12)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-212">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="9c209-212">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9c209-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c209-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9c209-214">(13)</span><span class="sxs-lookup"><span data-stu-id="9c209-214">(13)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-215">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c209-215">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9c209-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="9c209-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9c209-217">(14)</span><span class="sxs-lookup"><span data-stu-id="9c209-217">(14)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-218">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="9c209-218">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9c209-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="9c209-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9c209-220">(15)</span><span class="sxs-lookup"><span data-stu-id="9c209-220">(15)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-221">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="9c209-221">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9c209-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c209-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9c209-223">(16)</span><span class="sxs-lookup"><span data-stu-id="9c209-223">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-224">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c209-224">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9c209-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="9c209-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9c209-226">(17)</span><span class="sxs-lookup"><span data-stu-id="9c209-226">(17)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-227">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="9c209-227">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9c209-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c209-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9c209-229">(18)</span><span class="sxs-lookup"><span data-stu-id="9c209-229">(18)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-230">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c209-230">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9c209-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="9c209-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="9c209-232">(19)</span><span class="sxs-lookup"><span data-stu-id="9c209-232">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9c209-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="9c209-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="9c209-234">(20)</span><span class="sxs-lookup"><span data-stu-id="9c209-234">(20)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-235">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="9c209-235">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9c209-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c209-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9c209-237">(21)</span><span class="sxs-lookup"><span data-stu-id="9c209-237">(21)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-238">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="9c209-238">System failure.</span></span> <span data-ttu-id="9c209-239">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="9c209-239">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="9c209-240">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c209-240">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9c209-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="9c209-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="9c209-242">(22)</span><span class="sxs-lookup"><span data-stu-id="9c209-242">(22)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-243">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="9c209-243">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9c209-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="9c209-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9c209-245">(23)</span><span class="sxs-lookup"><span data-stu-id="9c209-245">(23)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-246">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="9c209-246">System failure.</span></span> <span data-ttu-id="9c209-247">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="9c209-247">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9c209-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="9c209-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9c209-249">(24)</span><span class="sxs-lookup"><span data-stu-id="9c209-249">(24)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-250">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="9c209-250">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9c209-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c209-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9c209-252">(25)</span><span class="sxs-lookup"><span data-stu-id="9c209-252">(25)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-253">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c209-253">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9c209-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c209-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9c209-255">(26)</span><span class="sxs-lookup"><span data-stu-id="9c209-255">(26)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-256">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c209-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9c209-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="9c209-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9c209-258">(27)</span><span class="sxs-lookup"><span data-stu-id="9c209-258">(27)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-259">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="9c209-259">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9c209-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="9c209-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9c209-261">(28)</span><span class="sxs-lookup"><span data-stu-id="9c209-261">(28)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-262">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="9c209-262">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9c209-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="9c209-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9c209-264">(29)</span><span class="sxs-lookup"><span data-stu-id="9c209-264">(29)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-265">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="9c209-265">Device is disabled.</span></span> <span data-ttu-id="9c209-266">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="9c209-266">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9c209-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c209-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9c209-268">(30)</span><span class="sxs-lookup"><span data-stu-id="9c209-268">(30)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-269">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c209-269">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9c209-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9c209-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9c209-271">31</span><span class="sxs-lookup"><span data-stu-id="9c209-271">(31)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-272">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9c209-272">Device is not working properly.</span></span> <span data-ttu-id="9c209-273">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="9c209-273">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c209-274">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="9c209-274">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-275">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9c209-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-277">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9c209-277">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9c209-278">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9c209-278">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9c209-279">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-279">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c209-280">**ControllerTimeouts**</span><span class="sxs-lookup"><span data-stu-id="9c209-280">**ControllerTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-281">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c209-281">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c209-283">Numero di timeout del controller SCSI che si sono verificati dopo l'ultima reimpostazione.</span><span class="sxs-lookup"><span data-stu-id="9c209-283">Number of SCSI controller time-outs that have occurred since the last reset.</span></span>

</dd> <dt>

<span data-ttu-id="9c209-284">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9c209-284">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-285">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c209-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-287">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9c209-287">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9c209-288">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="9c209-288">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9c209-289">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="9c209-289">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9c209-290">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c209-291">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9c209-291">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-292">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c209-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-294">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9c209-294">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9c209-295">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9c209-295">Textual description of the object.</span></span>

<span data-ttu-id="9c209-296">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-296">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c209-297">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9c209-297">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-298">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c209-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-300">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9c209-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9c209-301">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9c209-301">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="9c209-302">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c209-303">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9c209-303">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-304">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9c209-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c209-306">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="9c209-306">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="9c209-307">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c209-308">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9c209-308">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-309">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c209-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c209-311">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="9c209-311">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="9c209-312">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-312">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c209-313">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9c209-313">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-314">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9c209-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-316">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="9c209-316">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9c209-317">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9c209-317">Date and time the object was installed.</span></span> <span data-ttu-id="9c209-318">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="9c209-318">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9c209-319">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c209-320">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9c209-320">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-321">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c209-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c209-323">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9c209-323">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9c209-324">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c209-325">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="9c209-325">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-326">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c209-326">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-328">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="9c209-328">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="9c209-329">Larghezza massima dei dati, in bit, supportata dal controller SCSI.</span><span class="sxs-lookup"><span data-stu-id="9c209-329">Maximum data width, in bits, supported by the SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="9c209-330">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="9c209-330">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-331">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c209-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-333">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="9c209-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="9c209-334">Numero massimo di entità indirizzabili direttamente supportate dal controller.</span><span class="sxs-lookup"><span data-stu-id="9c209-334">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="9c209-335">Se il numero è sconosciuto o illimitato, è necessario utilizzare il valore 0.</span><span class="sxs-lookup"><span data-stu-id="9c209-335">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="9c209-336">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-336">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c209-337">**MaxTransferRate**</span><span class="sxs-lookup"><span data-stu-id="9c209-337">**MaxTransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-338">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c209-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-340">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="9c209-340">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="9c209-341">Velocità massima di trasferimento, in bit al secondo, supportata dal controller SCSI.</span><span class="sxs-lookup"><span data-stu-id="9c209-341">Maximum transfer rate, in bits-per-second, supported by the SCSI controller.</span></span>

<span data-ttu-id="9c209-342">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9c209-342">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9c209-343">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9c209-343">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-344">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c209-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-346">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9c209-346">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9c209-347">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="9c209-347">Label by which the object is known.</span></span> <span data-ttu-id="9c209-348">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="9c209-348">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9c209-349">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-349">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c209-350">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9c209-350">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-351">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c209-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-353">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9c209-353">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9c209-354">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9c209-354">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="9c209-355">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9c209-356">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="9c209-356">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="9c209-357">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9c209-357">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-358">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c209-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9c209-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c209-360">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9c209-360">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="9c209-361">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="9c209-361">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c209-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="9c209-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9c209-363"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="9c209-363"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9c209-364"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="9c209-364"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9c209-365"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="9c209-365"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-366">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="9c209-366">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9c209-367"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="9c209-367"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-368">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="9c209-368">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9c209-369"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="9c209-369"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-370">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="9c209-370">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="9c209-371">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="9c209-371">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="9c209-372">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="9c209-372">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9c209-373"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="9c209-373"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-374">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="9c209-374">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9c209-375"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="9c209-375"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-376">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="9c209-376">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c209-377">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9c209-377">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-378">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9c209-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-379">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c209-380">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="9c209-380">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="9c209-381">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9c209-381">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="9c209-382">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="9c209-382">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="9c209-383">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9c209-383">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="9c209-384">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c209-385">**ProtectionManagement**</span><span class="sxs-lookup"><span data-stu-id="9c209-385">**ProtectionManagement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-386">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c209-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-388">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Controller di archiviazione DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="9c209-388">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Controller\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="9c209-389">Indica se il controller SCSI fornisce la ridondanza o la protezione dagli errori del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c209-389">Indicates whether the SCSI controller provides redundancy or protection against device failures.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9c209-390"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9c209-390"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c209-391"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="9c209-391"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span>

<span data-ttu-id="9c209-392"><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span>Non **protetto** (3)</span><span class="sxs-lookup"><span data-stu-id="9c209-392"><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span>**Unprotected** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span>

<span data-ttu-id="9c209-393"><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span>**Protetto** (4)</span><span class="sxs-lookup"><span data-stu-id="9c209-393"><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span>**Protected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC__SCSI-3_Controller_Command_"></span><span id="protected_through_scc__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="9c209-394"><span id="Protected_through_SCC__SCSI-3_Controller_Command_"></span><span id="protected_through_scc__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC__SCSI-3_CONTROLLER_COMMAND_"></span>**Protetto tramite SCC (comando controller SCSI-3)** (5)</span><span class="sxs-lookup"><span data-stu-id="9c209-394"><span id="Protected_through_SCC__SCSI-3_Controller_Command_"></span><span id="protected_through_scc__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC__SCSI-3_CONTROLLER_COMMAND_"></span>**Protected through SCC (SCSI-3 Controller Command)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-395">Protetto da SCC (comando controller SCSI-3)</span><span class="sxs-lookup"><span data-stu-id="9c209-395">Protected by SCC (SCSI-3 controller command)</span></span>

</dd> <dt>

<span id="Protected_through_SCC-2__SCSI-3_Controller_Command_"></span><span id="protected_through_scc-2__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC-2__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="9c209-396"><span id="Protected_through_SCC-2__SCSI-3_Controller_Command_"></span><span id="protected_through_scc-2__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC-2__SCSI-3_CONTROLLER_COMMAND_"></span>**Protetto tramite SCC-2 (comando controller SCSI-3)** (6)</span><span class="sxs-lookup"><span data-stu-id="9c209-396"><span id="Protected_through_SCC-2__SCSI-3_Controller_Command_"></span><span id="protected_through_scc-2__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC-2__SCSI-3_CONTROLLER_COMMAND_"></span>**Protected through SCC-2 (SCSI-3 Controller Command)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9c209-397">Protetto da SCC-2 (comando controller SCSI-3)</span><span class="sxs-lookup"><span data-stu-id="9c209-397">Protected by SCC-2 (SCSI-3 controller command)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c209-398">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="9c209-398">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-399">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c209-399">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-401">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,2 "," MIF. \|Dischi DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9c209-401">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9c209-402">Protocollo usato dal controller per accedere ai dispositivi "controllati".</span><span class="sxs-lookup"><span data-stu-id="9c209-402">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="9c209-403">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-403">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="9c209-404">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="9c209-404">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9c209-405">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9c209-405">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c209-406">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="9c209-406">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="9c209-407">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="9c209-407">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="9c209-408">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="9c209-408">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="9c209-409">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="9c209-409">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="9c209-410">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="9c209-410">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="9c209-411">**Dischetto flessibile** (7)</span><span class="sxs-lookup"><span data-stu-id="9c209-411">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="9c209-412">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="9c209-412">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="9c209-413">**Interfaccia parallela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="9c209-413">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="9c209-414">**Protocollo di Fibre Channel SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="9c209-414">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="9c209-415">**Protocollo bus seriale SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="9c209-415">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="9c209-416">**Protocollo bus seriale SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="9c209-416">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="9c209-417">**Architettura di archiviazione seriale SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="9c209-417">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="9c209-418">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="9c209-418">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="9c209-419">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="9c209-419">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="9c209-420">**Bus seriale universale** (16)</span><span class="sxs-lookup"><span data-stu-id="9c209-420">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="9c209-421">**Protocollo parallelo** (17)</span><span class="sxs-lookup"><span data-stu-id="9c209-421">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="9c209-422">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="9c209-422">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="9c209-423">**Diagnostica** (19)</span><span class="sxs-lookup"><span data-stu-id="9c209-423">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="9c209-424">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="9c209-424">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="9c209-425">**Potenza** (21)</span><span class="sxs-lookup"><span data-stu-id="9c209-425">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="9c209-426">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="9c209-426">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="9c209-427">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="9c209-427">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="9c209-428">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="9c209-428">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="9c209-429">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="9c209-429">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="9c209-430">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="9c209-430">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="9c209-431">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="9c209-431">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="9c209-432">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="9c209-432">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="9c209-433">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="9c209-433">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="9c209-434">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="9c209-434">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="9c209-435">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="9c209-435">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="9c209-436">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="9c209-436">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="9c209-437">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="9c209-437">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="9c209-438">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="9c209-438">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="9c209-439">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="9c209-439">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="9c209-440">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="9c209-440">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="9c209-441">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="9c209-441">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="9c209-442">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="9c209-442">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="9c209-443">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="9c209-443">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="9c209-444">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="9c209-444">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="9c209-445">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="9c209-445">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="9c209-446">**ATA/IDE avanzato** (42)</span><span class="sxs-lookup"><span data-stu-id="9c209-446">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="9c209-447">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="9c209-447">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="9c209-448">**TWIRP (infrarossi bidirezionali)** (44)</span><span class="sxs-lookup"><span data-stu-id="9c209-448">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="9c209-449">**FIR (infrarossi veloci)** (45)</span><span class="sxs-lookup"><span data-stu-id="9c209-449">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="9c209-450">**Sir (Serial Infrared)** (46)</span><span class="sxs-lookup"><span data-stu-id="9c209-450">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="9c209-451">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="9c209-451">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9c209-452">**Status**</span><span class="sxs-lookup"><span data-stu-id="9c209-452">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-453">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c209-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-454">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-455">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="9c209-455">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9c209-456">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9c209-456">Current status of the object.</span></span> <span data-ttu-id="9c209-457">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-457">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9c209-458">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="9c209-458">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9c209-459">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9c209-459">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9c209-460">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="9c209-460">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9c209-461">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="9c209-461">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c209-462">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="9c209-462">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9c209-463">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="9c209-463">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9c209-464">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="9c209-464">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9c209-465">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="9c209-465">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9c209-466">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="9c209-466">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9c209-467">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="9c209-467">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9c209-468">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="9c209-468">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9c209-469">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="9c209-469">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9c209-470">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="9c209-470">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9c209-471">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9c209-471">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-472">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c209-472">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-473">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-474">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9c209-474">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9c209-475">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9c209-475">State of the logical device.</span></span> <span data-ttu-id="9c209-476">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="9c209-476">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="9c209-477">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9c209-478">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9c209-478">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c209-479">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="9c209-479">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9c209-480">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="9c209-480">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9c209-481">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="9c209-481">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9c209-482">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="9c209-482">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9c209-483">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9c209-483">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-484">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c209-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-485">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-485">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-486">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9c209-486">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9c209-487">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="9c209-487">Scoping system's creation class name.</span></span>

<span data-ttu-id="9c209-488">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-488">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c209-489">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9c209-489">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-490">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9c209-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-491">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c209-492">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9c209-492">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9c209-493">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="9c209-493">Scoping system's name.</span></span>

<span data-ttu-id="9c209-494">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-494">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c209-495">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="9c209-495">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c209-496">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9c209-496">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9c209-497">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c209-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c209-498">Data e ora dell'ultima reimpostazione del controller, ovvero il controller è stato spento o reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="9c209-498">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="9c209-499">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-499">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c209-500">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c209-500">Remarks</span></span>

<span data-ttu-id="9c209-501">La classe **CIM \_ controller SCSI** è derivata dal [**\_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-501">The **CIM\_SCSIController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="9c209-502">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="9c209-502">WMI does not implement this class.</span></span> <span data-ttu-id="9c209-503">Per le classi WMI derivate da **CIM \_ controller SCSI**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9c209-503">For WMI classes derived from **CIM\_SCSIController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9c209-504">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="9c209-504">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9c209-505">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="9c209-505">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c209-506">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c209-506">Requirements</span></span>



| <span data-ttu-id="9c209-507">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c209-507">Requirement</span></span> | <span data-ttu-id="9c209-508">Valore</span><span class="sxs-lookup"><span data-stu-id="9c209-508">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c209-509">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c209-509">Minimum supported client</span></span><br/> | <span data-ttu-id="9c209-510">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c209-510">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9c209-511">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c209-511">Minimum supported server</span></span><br/> | <span data-ttu-id="9c209-512">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c209-512">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9c209-513">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9c209-513">Namespace</span></span><br/>                | <span data-ttu-id="9c209-514">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9c209-514">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9c209-515">MOF</span><span class="sxs-lookup"><span data-stu-id="9c209-515">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c209-516"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c209-516"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c209-517">DLL</span><span class="sxs-lookup"><span data-stu-id="9c209-517">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c209-518"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c209-518"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c209-519">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c209-519">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c209-520">**\_Controller CIM**</span><span class="sxs-lookup"><span data-stu-id="9c209-520">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

