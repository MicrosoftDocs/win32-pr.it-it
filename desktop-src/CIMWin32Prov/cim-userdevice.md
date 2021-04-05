---
description: La \_ classe CIM UserDevice è una classe padre da cui discendono altre classi, ad esempio CIM \_ Keyboard o CIM \_ DesktopMonitor. I dispositivi utente sono dispositivi logici che consentono all'utente di un sistema informatico di immettere, visualizzare o ascoltare i dati.
ms.assetid: 311a065a-df9b-4c4b-bdc4-d3de89ce2f3d
ms.tgt_platform: multiple
title: Classe CIM_UserDevice (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UserDevice
- CIM_UserDevice.Availability
- CIM_UserDevice.Caption
- CIM_UserDevice.ConfigManagerErrorCode
- CIM_UserDevice.ConfigManagerUserConfig
- CIM_UserDevice.CreationClassName
- CIM_UserDevice.Description
- CIM_UserDevice.DeviceID
- CIM_UserDevice.ErrorCleared
- CIM_UserDevice.ErrorDescription
- CIM_UserDevice.InstallDate
- CIM_UserDevice.IsLocked
- CIM_UserDevice.LastErrorCode
- CIM_UserDevice.Name
- CIM_UserDevice.PNPDeviceID
- CIM_UserDevice.PowerManagementCapabilities
- CIM_UserDevice.PowerManagementSupported
- CIM_UserDevice.Status
- CIM_UserDevice.StatusInfo
- CIM_UserDevice.SystemCreationClassName
- CIM_UserDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b8a91082679c38d7741f9a8d7b43c7f9705333f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125817"
---
# <a name="cim_userdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="12837-104">Classe CIM_UserDevice (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="12837-104">CIM_UserDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="12837-105">La classe **CIM \_ UserDevice** è una classe padre da cui discendono altre classi, ad esempio [**CIM \_ Keyboard**](cim-keyboard.md) o [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="12837-105">The **CIM\_UserDevice** class is a parent class from which other classes, such as [**CIM\_Keyboard**](cim-keyboard.md) or [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), descend.</span></span> <span data-ttu-id="12837-106">I dispositivi utente sono dispositivi logici che consentono all'utente di un sistema informatico di immettere, visualizzare o ascoltare i dati.</span><span class="sxs-lookup"><span data-stu-id="12837-106">User devices are logical devices that allow a computer system's user to input, view, or hear data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12837-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="12837-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="12837-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="12837-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="12837-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="12837-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="12837-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="12837-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="12837-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12837-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C533-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UserDevice : CIM_LogicalDevice
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
  boolean  IsLocked;
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

## <a name="members"></a><span data-ttu-id="12837-112">Members</span><span class="sxs-lookup"><span data-stu-id="12837-112">Members</span></span>

<span data-ttu-id="12837-113">La classe **CIM \_ UserDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="12837-113">The **CIM\_UserDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="12837-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="12837-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="12837-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12837-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="12837-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="12837-116">Methods</span></span>

<span data-ttu-id="12837-117">La classe **CIM \_ UserDevice** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="12837-117">The **CIM\_UserDevice** class has these methods.</span></span>



| <span data-ttu-id="12837-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="12837-118">Method</span></span>                                                                | <span data-ttu-id="12837-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12837-119">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12837-120">**Reset**</span><span class="sxs-lookup"><span data-stu-id="12837-120">**Reset**</span></span>](reset-method-in-class-cim-userdevice.md)                 | <span data-ttu-id="12837-121">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="12837-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="12837-122">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="12837-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="12837-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="12837-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-userdevice.md) | <span data-ttu-id="12837-124">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="12837-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="12837-125">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="12837-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="12837-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12837-126">Properties</span></span>

<span data-ttu-id="12837-127">La classe **CIM \_ UserDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="12837-127">The **CIM\_UserDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12837-128">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="12837-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12837-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12837-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12837-131">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="12837-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="12837-132">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12837-132">Availability and status of the device.</span></span>

<span data-ttu-id="12837-133">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12837-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="12837-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="12837-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12837-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="12837-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="12837-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="12837-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="12837-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="12837-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="12837-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="12837-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="12837-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="12837-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="12837-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="12837-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="12837-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="12837-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="12837-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="12837-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="12837-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="12837-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="12837-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="12837-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="12837-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="12837-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="12837-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="12837-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="12837-147">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="12837-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="12837-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="12837-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="12837-149">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="12837-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="12837-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="12837-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="12837-151">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="12837-151">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="12837-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="12837-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="12837-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="12837-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="12837-154">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="12837-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="12837-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="12837-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="12837-156">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="12837-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="12837-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="12837-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="12837-158">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="12837-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="12837-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="12837-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="12837-160">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="12837-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="12837-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="12837-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="12837-162">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="12837-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="12837-163">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="12837-163">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12837-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12837-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12837-166">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="12837-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="12837-167">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="12837-167">Short textual description of the object.</span></span>

<span data-ttu-id="12837-168">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12837-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12837-169">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="12837-169">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-170">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12837-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12837-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12837-172">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="12837-172">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="12837-173">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="12837-173">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="12837-174">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12837-174">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="12837-175"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="12837-175"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="12837-176"> (0)</span><span class="sxs-lookup"><span data-stu-id="12837-176">(0)</span></span>


</dt> <dd>

<span data-ttu-id="12837-177">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="12837-177">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="12837-178"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="12837-178"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="12837-179">(1)</span><span class="sxs-lookup"><span data-stu-id="12837-179">(1)</span></span>


</dt> <dd>

<span data-ttu-id="12837-180">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="12837-180">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="12837-181"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12837-181"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="12837-182">(2)</span><span class="sxs-lookup"><span data-stu-id="12837-182">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="12837-183"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="12837-183"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="12837-184">(3)</span><span class="sxs-lookup"><span data-stu-id="12837-184">(3)</span></span>


</dt> <dd>

<span data-ttu-id="12837-185">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="12837-185">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="12837-186"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="12837-186"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="12837-187">(4)</span><span class="sxs-lookup"><span data-stu-id="12837-187">(4)</span></span>


</dt> <dd>

<span data-ttu-id="12837-188">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="12837-188">Device is not working properly.</span></span> <span data-ttu-id="12837-189">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="12837-189">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="12837-190"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="12837-190"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="12837-191">(5)</span><span class="sxs-lookup"><span data-stu-id="12837-191">(5)</span></span>


</dt> <dd>

<span data-ttu-id="12837-192">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="12837-192">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="12837-193"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="12837-193"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="12837-194"> (6)</span><span class="sxs-lookup"><span data-stu-id="12837-194">(6)</span></span>


</dt> <dd>

<span data-ttu-id="12837-195">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="12837-195">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="12837-196"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="12837-196"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="12837-197">(7)</span><span class="sxs-lookup"><span data-stu-id="12837-197">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="12837-198"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="12837-198"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="12837-199">(8)</span><span class="sxs-lookup"><span data-stu-id="12837-199">(8)</span></span>


</dt> <dd>

<span data-ttu-id="12837-200">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="12837-200">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="12837-201"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="12837-201"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="12837-202">(9)</span><span class="sxs-lookup"><span data-stu-id="12837-202">(9)</span></span>


</dt> <dd>

<span data-ttu-id="12837-203">Il dispositivo non funziona correttamente; il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12837-203">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="12837-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12837-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="12837-205">(10)</span><span class="sxs-lookup"><span data-stu-id="12837-205">(10)</span></span>


</dt> <dd>

<span data-ttu-id="12837-206">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12837-206">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="12837-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12837-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="12837-208">(11)</span><span class="sxs-lookup"><span data-stu-id="12837-208">(11)</span></span>


</dt> <dd>

<span data-ttu-id="12837-209">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12837-209">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="12837-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="12837-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="12837-211">12</span><span class="sxs-lookup"><span data-stu-id="12837-211">(12)</span></span>


</dt> <dd>

<span data-ttu-id="12837-212">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="12837-212">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="12837-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12837-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="12837-214">(13)</span><span class="sxs-lookup"><span data-stu-id="12837-214">(13)</span></span>


</dt> <dd>

<span data-ttu-id="12837-215">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12837-215">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="12837-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="12837-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="12837-217">(14)</span><span class="sxs-lookup"><span data-stu-id="12837-217">(14)</span></span>


</dt> <dd>

<span data-ttu-id="12837-218">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="12837-218">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="12837-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="12837-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="12837-220">(15)</span><span class="sxs-lookup"><span data-stu-id="12837-220">(15)</span></span>


</dt> <dd>

<span data-ttu-id="12837-221">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="12837-221">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="12837-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12837-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="12837-223">(16)</span><span class="sxs-lookup"><span data-stu-id="12837-223">(16)</span></span>


</dt> <dd>

<span data-ttu-id="12837-224">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12837-224">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="12837-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="12837-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="12837-226">(17)</span><span class="sxs-lookup"><span data-stu-id="12837-226">(17)</span></span>


</dt> <dd>

<span data-ttu-id="12837-227">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="12837-227">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="12837-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12837-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="12837-229">(18)</span><span class="sxs-lookup"><span data-stu-id="12837-229">(18)</span></span>


</dt> <dd>

<span data-ttu-id="12837-230">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12837-230">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="12837-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="12837-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="12837-232">(19)</span><span class="sxs-lookup"><span data-stu-id="12837-232">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="12837-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="12837-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="12837-234">(20)</span><span class="sxs-lookup"><span data-stu-id="12837-234">(20)</span></span>


</dt> <dd>

<span data-ttu-id="12837-235">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="12837-235">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="12837-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12837-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="12837-237">(21)</span><span class="sxs-lookup"><span data-stu-id="12837-237">(21)</span></span>


</dt> <dd>

<span data-ttu-id="12837-238">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="12837-238">System failure.</span></span> <span data-ttu-id="12837-239">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="12837-239">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="12837-240">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12837-240">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="12837-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="12837-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="12837-242">(22)</span><span class="sxs-lookup"><span data-stu-id="12837-242">(22)</span></span>


</dt> <dd>

<span data-ttu-id="12837-243">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="12837-243">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="12837-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="12837-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="12837-245">(23)</span><span class="sxs-lookup"><span data-stu-id="12837-245">(23)</span></span>


</dt> <dd>

<span data-ttu-id="12837-246">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="12837-246">System failure.</span></span> <span data-ttu-id="12837-247">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="12837-247">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="12837-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="12837-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="12837-249">(24)</span><span class="sxs-lookup"><span data-stu-id="12837-249">(24)</span></span>


</dt> <dd>

<span data-ttu-id="12837-250">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="12837-250">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="12837-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12837-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="12837-252">(25)</span><span class="sxs-lookup"><span data-stu-id="12837-252">(25)</span></span>


</dt> <dd>

<span data-ttu-id="12837-253">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12837-253">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="12837-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12837-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="12837-255">(26)</span><span class="sxs-lookup"><span data-stu-id="12837-255">(26)</span></span>


</dt> <dd>

<span data-ttu-id="12837-256">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12837-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="12837-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="12837-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="12837-258">(27)</span><span class="sxs-lookup"><span data-stu-id="12837-258">(27)</span></span>


</dt> <dd>

<span data-ttu-id="12837-259">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="12837-259">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="12837-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="12837-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="12837-261">(28)</span><span class="sxs-lookup"><span data-stu-id="12837-261">(28)</span></span>


</dt> <dd>

<span data-ttu-id="12837-262">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="12837-262">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="12837-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="12837-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="12837-264">(29)</span><span class="sxs-lookup"><span data-stu-id="12837-264">(29)</span></span>


</dt> <dd>

<span data-ttu-id="12837-265">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="12837-265">Device is disabled.</span></span> <span data-ttu-id="12837-266">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="12837-266">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="12837-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12837-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="12837-268">(30)</span><span class="sxs-lookup"><span data-stu-id="12837-268">(30)</span></span>


</dt> <dd>

<span data-ttu-id="12837-269">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12837-269">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="12837-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12837-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="12837-271">31</span><span class="sxs-lookup"><span data-stu-id="12837-271">(31)</span></span>


</dt> <dd>

<span data-ttu-id="12837-272">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="12837-272">Device is not working properly.</span></span> <span data-ttu-id="12837-273">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="12837-273">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="12837-274">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="12837-274">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-275">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="12837-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12837-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12837-277">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="12837-277">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="12837-278">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="12837-278">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="12837-279">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12837-279">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12837-280">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="12837-280">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-281">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12837-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12837-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12837-283">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12837-283">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12837-284">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="12837-284">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="12837-285">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="12837-285">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="12837-286">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12837-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12837-287">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="12837-287">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12837-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12837-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12837-290">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="12837-290">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="12837-291">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="12837-291">Textual description of the object.</span></span>

<span data-ttu-id="12837-292">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12837-292">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12837-293">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="12837-293">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-294">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12837-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12837-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12837-296">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12837-296">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12837-297">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="12837-297">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="12837-298">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12837-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12837-299">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="12837-299">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-300">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="12837-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12837-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12837-302">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="12837-302">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="12837-303">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12837-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12837-304">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="12837-304">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-305">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12837-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12837-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12837-307">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="12837-307">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="12837-308">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12837-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12837-309">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="12837-309">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-310">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="12837-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="12837-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12837-312">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="12837-312">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="12837-313">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="12837-313">Date and time the object was installed.</span></span> <span data-ttu-id="12837-314">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="12837-314">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="12837-315">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12837-315">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12837-316">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="12837-316">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-317">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="12837-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12837-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12837-319">Se **true**, il dispositivo è bloccato impedendo l'input o l'output dell'utente.</span><span class="sxs-lookup"><span data-stu-id="12837-319">If **TRUE**, the device is locked, preventing user input or output.</span></span>

</dd> <dt>

<span data-ttu-id="12837-320">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="12837-320">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-321">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12837-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12837-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12837-323">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="12837-323">Last error code reported by the logical device.</span></span>

<span data-ttu-id="12837-324">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12837-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12837-325">**Nome**</span><span class="sxs-lookup"><span data-stu-id="12837-325">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-326">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12837-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12837-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12837-328">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="12837-328">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="12837-329">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="12837-329">Label by which the object is known.</span></span> <span data-ttu-id="12837-330">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="12837-330">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="12837-331">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12837-331">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12837-332">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="12837-332">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-333">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12837-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12837-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12837-335">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="12837-335">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="12837-336">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="12837-336">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="12837-337">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12837-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="12837-338">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="12837-338">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="12837-339">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="12837-339">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-340">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12837-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="12837-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12837-342">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="12837-342">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="12837-343">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="12837-343">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12837-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="12837-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="12837-345"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="12837-345"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="12837-346"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="12837-346"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="12837-347"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="12837-347"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="12837-348">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="12837-348">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="12837-349"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="12837-349"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="12837-350">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="12837-350">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="12837-351"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="12837-351"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="12837-352">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="12837-352">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="12837-353">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="12837-353">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="12837-354">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="12837-354">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="12837-355"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="12837-355"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="12837-356">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="12837-356">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="12837-357"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="12837-357"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="12837-358">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="12837-358">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="12837-359">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="12837-359">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-360">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="12837-360">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12837-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12837-362">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="12837-362">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="12837-363">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="12837-363">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="12837-364">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="12837-364">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="12837-365">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="12837-365">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="12837-366">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12837-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12837-367">**Status**</span><span class="sxs-lookup"><span data-stu-id="12837-367">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-368">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12837-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12837-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12837-370">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="12837-370">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="12837-371">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="12837-371">Current status of the object.</span></span> <span data-ttu-id="12837-372">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12837-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="12837-373">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="12837-373">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="12837-374">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="12837-374">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="12837-375">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="12837-375">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="12837-376">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="12837-376">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12837-377">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="12837-377">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="12837-378">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="12837-378">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="12837-379">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="12837-379">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="12837-380">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="12837-380">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="12837-381">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="12837-381">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="12837-382">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="12837-382">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="12837-383">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="12837-383">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="12837-384">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="12837-384">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="12837-385">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="12837-385">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12837-386">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="12837-386">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-387">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12837-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12837-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12837-389">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="12837-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="12837-390">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="12837-390">State of the logical device.</span></span> <span data-ttu-id="12837-391">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="12837-391">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="12837-392">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12837-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="12837-393">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="12837-393">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12837-394">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="12837-394">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="12837-395">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="12837-395">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="12837-396">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="12837-396">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="12837-397">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="12837-397">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12837-398">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="12837-398">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-399">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12837-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12837-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12837-401">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12837-401">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12837-402">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="12837-402">Scoping system's creation class name.</span></span>

<span data-ttu-id="12837-403">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12837-403">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12837-404">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="12837-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12837-405">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12837-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12837-406">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12837-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12837-407">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12837-407">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12837-408">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="12837-408">Scoping system's name.</span></span>

<span data-ttu-id="12837-409">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12837-409">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12837-410">Commenti</span><span class="sxs-lookup"><span data-stu-id="12837-410">Remarks</span></span>

<span data-ttu-id="12837-411">La classe **CIM \_ UserDevice** è derivata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12837-411">The **CIM\_UserDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="12837-412">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="12837-412">WMI does not implement this class.</span></span> <span data-ttu-id="12837-413">Per le classi WMI derivate da **CIM \_ UserDevice**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="12837-413">For WMI classes derived from **CIM\_UserDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="12837-414">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="12837-414">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="12837-415">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="12837-415">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="12837-416">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12837-416">Requirements</span></span>



| <span data-ttu-id="12837-417">Requisito</span><span class="sxs-lookup"><span data-stu-id="12837-417">Requirement</span></span> | <span data-ttu-id="12837-418">Valore</span><span class="sxs-lookup"><span data-stu-id="12837-418">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12837-419">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12837-419">Minimum supported client</span></span><br/> | <span data-ttu-id="12837-420">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12837-420">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12837-421">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12837-421">Minimum supported server</span></span><br/> | <span data-ttu-id="12837-422">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12837-422">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12837-423">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="12837-423">Namespace</span></span><br/>                | <span data-ttu-id="12837-424">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="12837-424">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="12837-425">MOF</span><span class="sxs-lookup"><span data-stu-id="12837-425">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12837-426"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12837-426"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="12837-427">DLL</span><span class="sxs-lookup"><span data-stu-id="12837-427">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12837-428"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12837-428"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12837-429">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12837-429">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12837-430">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="12837-430">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

