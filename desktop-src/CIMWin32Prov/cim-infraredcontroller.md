---
description: La \_ classe CIM InfraredController rappresenta le funzionalità e la gestione di un controller a infrarossi.
ms.assetid: c3643c1c-a3c0-4600-b432-4f4be925aeb5
ms.tgt_platform: multiple
title: Classe CIM_InfraredController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InfraredController
- CIM_InfraredController.Availability
- CIM_InfraredController.Caption
- CIM_InfraredController.ConfigManagerErrorCode
- CIM_InfraredController.ConfigManagerUserConfig
- CIM_InfraredController.CreationClassName
- CIM_InfraredController.Description
- CIM_InfraredController.DeviceID
- CIM_InfraredController.ErrorCleared
- CIM_InfraredController.ErrorDescription
- CIM_InfraredController.InstallDate
- CIM_InfraredController.LastErrorCode
- CIM_InfraredController.MaxNumberControlled
- CIM_InfraredController.Name
- CIM_InfraredController.PNPDeviceID
- CIM_InfraredController.PowerManagementCapabilities
- CIM_InfraredController.PowerManagementSupported
- CIM_InfraredController.ProtocolSupported
- CIM_InfraredController.Status
- CIM_InfraredController.StatusInfo
- CIM_InfraredController.SystemCreationClassName
- CIM_InfraredController.SystemName
- CIM_InfraredController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27d61c82d3874e0a6d1864b04795dd51203c89eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126963"
---
# <a name="cim_infraredcontroller-class"></a><span data-ttu-id="aef80-103">CIM \_ InfraredController (classe)</span><span class="sxs-lookup"><span data-stu-id="aef80-103">CIM\_InfraredController class</span></span>

<span data-ttu-id="aef80-104">La classe **CIM \_ InfraredController** rappresenta le funzionalità e la gestione di un controller a infrarossi.</span><span class="sxs-lookup"><span data-stu-id="aef80-104">The **CIM\_InfraredController** class represents the capabilities and management of an infrared controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aef80-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="aef80-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aef80-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="aef80-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aef80-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="aef80-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="aef80-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="aef80-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aef80-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aef80-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{EDCE42F9-0991-11d3-910A-00105AA630BE}"), AMENDMENT]
class CIM_InfraredController : CIM_Controller
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

## <a name="members"></a><span data-ttu-id="aef80-110">Members</span><span class="sxs-lookup"><span data-stu-id="aef80-110">Members</span></span>

<span data-ttu-id="aef80-111">La classe **CIM \_ InfraredController** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="aef80-111">The **CIM\_InfraredController** class has these types of members:</span></span>

-   [<span data-ttu-id="aef80-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="aef80-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="aef80-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aef80-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="aef80-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="aef80-114">Methods</span></span>

<span data-ttu-id="aef80-115">La classe **CIM \_ InfraredController** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="aef80-115">The **CIM\_InfraredController** class has these methods.</span></span>



| <span data-ttu-id="aef80-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="aef80-116">Method</span></span>                                                                        | <span data-ttu-id="aef80-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aef80-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aef80-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="aef80-118">**Reset**</span></span>](reset-method-in-class-cim-infraredcontroller.md)                 | <span data-ttu-id="aef80-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="aef80-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="aef80-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aef80-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="aef80-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="aef80-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-infraredcontroller.md) | <span data-ttu-id="aef80-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="aef80-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="aef80-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aef80-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="aef80-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aef80-124">Properties</span></span>

<span data-ttu-id="aef80-125">La classe **CIM \_ InfraredController** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="aef80-125">The **CIM\_InfraredController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aef80-126">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="aef80-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aef80-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-129">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="aef80-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="aef80-130">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aef80-130">Availability and status of the device.</span></span>

<span data-ttu-id="aef80-131">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aef80-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="aef80-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aef80-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="aef80-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="aef80-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="aef80-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="aef80-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="aef80-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="aef80-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="aef80-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="aef80-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="aef80-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="aef80-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="aef80-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="aef80-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="aef80-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="aef80-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="aef80-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aef80-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="aef80-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="aef80-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="aef80-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="aef80-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="aef80-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="aef80-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="aef80-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-145">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="aef80-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="aef80-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="aef80-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-147">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="aef80-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="aef80-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="aef80-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-149">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="aef80-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="aef80-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="aef80-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="aef80-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="aef80-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-152">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="aef80-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="aef80-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="aef80-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-154">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="aef80-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="aef80-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="aef80-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-156">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="aef80-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="aef80-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="aef80-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-158">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="aef80-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="aef80-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="aef80-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-160">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="aef80-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aef80-161">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="aef80-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aef80-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-164">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="aef80-164">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="aef80-165">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aef80-165">Short textual description of the object.</span></span>

<span data-ttu-id="aef80-166">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef80-167">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="aef80-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-168">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aef80-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-170">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aef80-170">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aef80-171">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="aef80-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="aef80-172">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="aef80-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="aef80-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="aef80-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="aef80-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-175">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="aef80-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="aef80-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="aef80-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="aef80-177">(1)</span><span class="sxs-lookup"><span data-stu-id="aef80-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-178">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="aef80-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aef80-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aef80-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="aef80-180">(2)</span><span class="sxs-lookup"><span data-stu-id="aef80-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="aef80-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="aef80-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="aef80-182">(3)</span><span class="sxs-lookup"><span data-stu-id="aef80-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-183">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="aef80-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="aef80-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="aef80-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="aef80-185">(4)</span><span class="sxs-lookup"><span data-stu-id="aef80-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-186">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="aef80-186">Device is not working properly.</span></span> <span data-ttu-id="aef80-187">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="aef80-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="aef80-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="aef80-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="aef80-189">(5)</span><span class="sxs-lookup"><span data-stu-id="aef80-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-190">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="aef80-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="aef80-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="aef80-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="aef80-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="aef80-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-193">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="aef80-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="aef80-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="aef80-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="aef80-195">(7)</span><span class="sxs-lookup"><span data-stu-id="aef80-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="aef80-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="aef80-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="aef80-197">(8)</span><span class="sxs-lookup"><span data-stu-id="aef80-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-198">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="aef80-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="aef80-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="aef80-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="aef80-200">(9)</span><span class="sxs-lookup"><span data-stu-id="aef80-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-201">Il dispositivo non funziona correttamente; il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aef80-201">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="aef80-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aef80-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="aef80-203">(10)</span><span class="sxs-lookup"><span data-stu-id="aef80-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-204">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aef80-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="aef80-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aef80-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="aef80-206">(11)</span><span class="sxs-lookup"><span data-stu-id="aef80-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-207">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aef80-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="aef80-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="aef80-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="aef80-209">12</span><span class="sxs-lookup"><span data-stu-id="aef80-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-210">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="aef80-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="aef80-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aef80-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="aef80-212">(13)</span><span class="sxs-lookup"><span data-stu-id="aef80-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-213">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aef80-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="aef80-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="aef80-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="aef80-215">(14)</span><span class="sxs-lookup"><span data-stu-id="aef80-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-216">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="aef80-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="aef80-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="aef80-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="aef80-218">(15)</span><span class="sxs-lookup"><span data-stu-id="aef80-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-219">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="aef80-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="aef80-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aef80-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="aef80-221">(16)</span><span class="sxs-lookup"><span data-stu-id="aef80-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-222">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aef80-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="aef80-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="aef80-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="aef80-224">(17)</span><span class="sxs-lookup"><span data-stu-id="aef80-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-225">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="aef80-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aef80-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aef80-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="aef80-227">(18)</span><span class="sxs-lookup"><span data-stu-id="aef80-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-228">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aef80-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="aef80-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="aef80-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="aef80-230">(19)</span><span class="sxs-lookup"><span data-stu-id="aef80-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="aef80-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="aef80-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="aef80-232">(20)</span><span class="sxs-lookup"><span data-stu-id="aef80-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-233">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="aef80-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="aef80-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aef80-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="aef80-235">(21)</span><span class="sxs-lookup"><span data-stu-id="aef80-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-236">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="aef80-236">System failure.</span></span> <span data-ttu-id="aef80-237">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="aef80-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="aef80-238">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aef80-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="aef80-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="aef80-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="aef80-240">(22)</span><span class="sxs-lookup"><span data-stu-id="aef80-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-241">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="aef80-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="aef80-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="aef80-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="aef80-243">(23)</span><span class="sxs-lookup"><span data-stu-id="aef80-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-244">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="aef80-244">System failure.</span></span> <span data-ttu-id="aef80-245">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="aef80-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="aef80-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="aef80-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="aef80-247">(24)</span><span class="sxs-lookup"><span data-stu-id="aef80-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-248">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="aef80-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="aef80-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aef80-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="aef80-250">(25)</span><span class="sxs-lookup"><span data-stu-id="aef80-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-251">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aef80-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="aef80-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aef80-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="aef80-253">(26)</span><span class="sxs-lookup"><span data-stu-id="aef80-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-254">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aef80-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="aef80-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="aef80-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="aef80-256">(27)</span><span class="sxs-lookup"><span data-stu-id="aef80-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-257">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="aef80-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="aef80-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="aef80-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="aef80-259">(28)</span><span class="sxs-lookup"><span data-stu-id="aef80-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-260">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="aef80-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="aef80-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="aef80-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="aef80-262">(29)</span><span class="sxs-lookup"><span data-stu-id="aef80-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-263">Il dispositivo è disabilitato; il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="aef80-263">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="aef80-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aef80-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="aef80-265">(30)</span><span class="sxs-lookup"><span data-stu-id="aef80-265">(30)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-266">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aef80-266">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aef80-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aef80-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="aef80-268">31</span><span class="sxs-lookup"><span data-stu-id="aef80-268">(31)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-269">Il dispositivo non funziona correttamente; Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="aef80-269">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aef80-270">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="aef80-270">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-271">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aef80-271">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-273">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aef80-273">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aef80-274">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="aef80-274">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="aef80-275">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-275">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef80-276">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aef80-276">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-277">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aef80-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-279">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aef80-279">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aef80-280">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="aef80-280">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="aef80-281">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="aef80-281">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="aef80-282">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef80-283">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="aef80-283">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-284">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aef80-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-286">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="aef80-286">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="aef80-287">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aef80-287">Textual description of the object.</span></span>

<span data-ttu-id="aef80-288">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef80-289">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="aef80-289">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-290">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aef80-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-292">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aef80-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aef80-293">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="aef80-293">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="aef80-294">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef80-295">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="aef80-295">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-296">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aef80-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aef80-298">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="aef80-298">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="aef80-299">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef80-300">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="aef80-300">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-301">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aef80-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aef80-303">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="aef80-303">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="aef80-304">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef80-305">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aef80-305">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-306">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aef80-306">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-308">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="aef80-308">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="aef80-309">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aef80-309">Date and time the object was installed.</span></span> <span data-ttu-id="aef80-310">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="aef80-310">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="aef80-311">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef80-312">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="aef80-312">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-313">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aef80-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aef80-315">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="aef80-315">Last error code reported by the logical device.</span></span>

<span data-ttu-id="aef80-316">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef80-317">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="aef80-317">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-318">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aef80-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-320">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="aef80-320">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="aef80-321">Numero massimo di entità indirizzabili direttamente supportate dal controller.</span><span class="sxs-lookup"><span data-stu-id="aef80-321">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="aef80-322">Se il numero è sconosciuto o illimitato, è necessario utilizzare il valore 0.</span><span class="sxs-lookup"><span data-stu-id="aef80-322">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="aef80-323">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-323">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef80-324">**Nome**</span><span class="sxs-lookup"><span data-stu-id="aef80-324">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-325">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aef80-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-327">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="aef80-327">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="aef80-328">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="aef80-328">Label by which the object is known.</span></span> <span data-ttu-id="aef80-329">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="aef80-329">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="aef80-330">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef80-331">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="aef80-331">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-332">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aef80-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-334">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aef80-334">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aef80-335">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="aef80-335">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="aef80-336">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="aef80-337">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="aef80-337">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="aef80-338">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="aef80-338">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-339">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aef80-339">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="aef80-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aef80-341">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="aef80-341">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="aef80-342">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="aef80-342">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aef80-343"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="aef80-343"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="aef80-344"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="aef80-344"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aef80-345"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="aef80-345"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="aef80-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="aef80-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-347">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="aef80-347">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="aef80-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="aef80-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-349">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="aef80-349">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="aef80-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="aef80-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-351">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="aef80-351">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="aef80-352">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="aef80-352">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="aef80-353">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="aef80-353">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="aef80-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="aef80-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-355">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="aef80-355">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="aef80-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="aef80-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="aef80-357">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="aef80-357">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aef80-358">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="aef80-358">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-359">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aef80-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-360">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aef80-361">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="aef80-361">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="aef80-362">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="aef80-362">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="aef80-363">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="aef80-363">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="aef80-364">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="aef80-364">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="aef80-365">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef80-366">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="aef80-366">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-367">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aef80-367">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-369">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta bus DMTF \| 001,2 "," MIF. \|Dischi DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="aef80-369">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="aef80-370">Protocollo usato dal controller per accedere ai dispositivi "controllati".</span><span class="sxs-lookup"><span data-stu-id="aef80-370">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="aef80-371">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-371">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="aef80-372">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="aef80-372">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aef80-373">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="aef80-373">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aef80-374">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="aef80-374">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="aef80-375">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="aef80-375">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="aef80-376">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="aef80-376">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="aef80-377">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="aef80-377">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="aef80-378">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="aef80-378">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="aef80-379">**Dischetto flessibile** (7)</span><span class="sxs-lookup"><span data-stu-id="aef80-379">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="aef80-380">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="aef80-380">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="aef80-381">**Interfaccia parallela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="aef80-381">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="aef80-382">**Protocollo di Fibre Channel SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="aef80-382">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="aef80-383">**Protocollo bus seriale SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="aef80-383">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="aef80-384">**Protocollo bus seriale SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="aef80-384">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="aef80-385">**Architettura di archiviazione seriale SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="aef80-385">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="aef80-386">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="aef80-386">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="aef80-387">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="aef80-387">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="aef80-388">**Bus seriale universale** (16)</span><span class="sxs-lookup"><span data-stu-id="aef80-388">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="aef80-389">**Protocollo parallelo** (17)</span><span class="sxs-lookup"><span data-stu-id="aef80-389">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="aef80-390">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="aef80-390">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="aef80-391">**Diagnostica** (19)</span><span class="sxs-lookup"><span data-stu-id="aef80-391">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="aef80-392">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="aef80-392">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="aef80-393">**Potenza** (21)</span><span class="sxs-lookup"><span data-stu-id="aef80-393">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="aef80-394">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="aef80-394">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="aef80-395">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="aef80-395">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="aef80-396">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="aef80-396">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="aef80-397">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="aef80-397">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="aef80-398">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="aef80-398">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="aef80-399">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="aef80-399">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="aef80-400">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="aef80-400">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="aef80-401">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="aef80-401">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="aef80-402">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="aef80-402">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="aef80-403">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="aef80-403">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="aef80-404">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="aef80-404">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="aef80-405">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="aef80-405">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="aef80-406">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="aef80-406">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="aef80-407">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="aef80-407">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="aef80-408">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="aef80-408">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="aef80-409">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="aef80-409">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="aef80-410">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="aef80-410">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="aef80-411">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="aef80-411">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="aef80-412">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="aef80-412">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="aef80-413">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="aef80-413">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="aef80-414">**ATA/IDE avanzato** (42)</span><span class="sxs-lookup"><span data-stu-id="aef80-414">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="aef80-415">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="aef80-415">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="aef80-416">**TWIRP (infrarossi bidirezionali)** (44)</span><span class="sxs-lookup"><span data-stu-id="aef80-416">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="aef80-417">**FIR (infrarossi veloci)** (45)</span><span class="sxs-lookup"><span data-stu-id="aef80-417">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="aef80-418">**Sir (Serial Infrared)** (46)</span><span class="sxs-lookup"><span data-stu-id="aef80-418">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="aef80-419">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="aef80-419">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aef80-420">**Status**</span><span class="sxs-lookup"><span data-stu-id="aef80-420">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-421">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aef80-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-422">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-423">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="aef80-423">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="aef80-424">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aef80-424">Current status of the object.</span></span> <span data-ttu-id="aef80-425">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-425">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="aef80-426">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="aef80-426">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="aef80-427">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="aef80-427">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="aef80-428">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="aef80-428">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aef80-429">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="aef80-429">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aef80-430">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="aef80-430">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="aef80-431">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="aef80-431">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="aef80-432">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="aef80-432">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="aef80-433">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="aef80-433">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="aef80-434">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="aef80-434">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="aef80-435">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="aef80-435">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="aef80-436">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="aef80-436">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="aef80-437">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="aef80-437">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="aef80-438">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="aef80-438">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aef80-439">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="aef80-439">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-440">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aef80-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-441">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-442">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="aef80-442">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="aef80-443">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="aef80-443">State of the logical device.</span></span> <span data-ttu-id="aef80-444">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="aef80-444">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="aef80-445">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-445">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aef80-446">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="aef80-446">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aef80-447">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="aef80-447">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="aef80-448">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="aef80-448">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aef80-449">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="aef80-449">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="aef80-450">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="aef80-450">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aef80-451">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aef80-451">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-452">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aef80-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-453">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-454">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aef80-454">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aef80-455">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="aef80-455">Scoping system's creation class name.</span></span>

<span data-ttu-id="aef80-456">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-456">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef80-457">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="aef80-457">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-458">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aef80-458">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-459">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef80-460">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aef80-460">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aef80-461">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="aef80-461">Scoping system's name.</span></span>

<span data-ttu-id="aef80-462">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-462">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef80-463">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="aef80-463">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef80-464">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aef80-464">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aef80-465">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aef80-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aef80-466">Data e ora dell'ultima reimpostazione del controller, che può indicare che il controller è stato spento o reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="aef80-466">Date and time the controller was last reset, which could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="aef80-467">Questa proprietà viene ereditata [**dal \_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-467">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aef80-468">Commenti</span><span class="sxs-lookup"><span data-stu-id="aef80-468">Remarks</span></span>

<span data-ttu-id="aef80-469">La classe **CIM \_ InfraredController** è derivata dal [**\_ controller CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-469">The **CIM\_InfraredController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="aef80-470">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="aef80-470">WMI does not implement this class.</span></span> <span data-ttu-id="aef80-471">Per le classi derivate da **CIM \_ InfraredController**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="aef80-471">For classes derived from **CIM\_InfraredController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="aef80-472">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="aef80-472">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aef80-473">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="aef80-473">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aef80-474">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aef80-474">Requirements</span></span>



| <span data-ttu-id="aef80-475">Requisito</span><span class="sxs-lookup"><span data-stu-id="aef80-475">Requirement</span></span> | <span data-ttu-id="aef80-476">Valore</span><span class="sxs-lookup"><span data-stu-id="aef80-476">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aef80-477">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aef80-477">Minimum supported client</span></span><br/> | <span data-ttu-id="aef80-478">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aef80-478">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aef80-479">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aef80-479">Minimum supported server</span></span><br/> | <span data-ttu-id="aef80-480">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aef80-480">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aef80-481">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aef80-481">Namespace</span></span><br/>                | <span data-ttu-id="aef80-482">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="aef80-482">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aef80-483">MOF</span><span class="sxs-lookup"><span data-stu-id="aef80-483">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aef80-484"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aef80-484"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aef80-485">DLL</span><span class="sxs-lookup"><span data-stu-id="aef80-485">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aef80-486"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aef80-486"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aef80-487">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aef80-487">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef80-488">**\_Controller CIM**</span><span class="sxs-lookup"><span data-stu-id="aef80-488">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

