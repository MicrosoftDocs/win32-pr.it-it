---
description: La \_ classe WMI MotherboardDevice Win32 rappresenta un dispositivo che contiene i componenti centrali del sistema di computer Windows.
ms.assetid: 2aed5fff-e994-4ce1-8a2e-aadb01adf28d
ms.tgt_platform: multiple
title: Classe Win32_MotherboardDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MotherboardDevice
- Win32_MotherboardDevice.Reset
- Win32_MotherboardDevice.SetPowerState
- Win32_MotherboardDevice.Availability
- Win32_MotherboardDevice.Caption
- Win32_MotherboardDevice.ConfigManagerErrorCode
- Win32_MotherboardDevice.ConfigManagerUserConfig
- Win32_MotherboardDevice.CreationClassName
- Win32_MotherboardDevice.Description
- Win32_MotherboardDevice.DeviceID
- Win32_MotherboardDevice.ErrorCleared
- Win32_MotherboardDevice.ErrorDescription
- Win32_MotherboardDevice.InstallDate
- Win32_MotherboardDevice.LastErrorCode
- Win32_MotherboardDevice.Name
- Win32_MotherboardDevice.PNPDeviceID
- Win32_MotherboardDevice.PowerManagementCapabilities
- Win32_MotherboardDevice.PowerManagementSupported
- Win32_MotherboardDevice.PrimaryBusType
- Win32_MotherboardDevice.RevisionNumber
- Win32_MotherboardDevice.SecondaryBusType
- Win32_MotherboardDevice.Status
- Win32_MotherboardDevice.StatusInfo
- Win32_MotherboardDevice.SystemCreationClassName
- Win32_MotherboardDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6df116d1e4bc4e87d7201deb33f57bc8e91320e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748922"
---
# <a name="win32_motherboarddevice-class"></a><span data-ttu-id="9f8e0-103">Win32 \_ MotherboardDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-103">Win32\_MotherboardDevice class</span></span>

<span data-ttu-id="9f8e0-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MotherboardDevice Win32** rappresenta un dispositivo che contiene i componenti centrali del sistema di computer Windows.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-104">The **Win32\_MotherboardDevice** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a device that contains the central components of the Windows computer system.</span></span>

<span data-ttu-id="9f8e0-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9f8e0-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f8e0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f8e0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_MotherboardDevice : CIM_LogicalDevice
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
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   PrimaryBusType;
  string   RevisionNumber;
  string   SecondaryBusType;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="9f8e0-108">Members</span><span class="sxs-lookup"><span data-stu-id="9f8e0-108">Members</span></span>

<span data-ttu-id="9f8e0-109">La classe **Win32 \_ MotherboardDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9f8e0-109">The **Win32\_MotherboardDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="9f8e0-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="9f8e0-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9f8e0-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f8e0-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9f8e0-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="9f8e0-112">Methods</span></span>

<span data-ttu-id="9f8e0-113">La classe **Win32 \_ MotherboardDevice** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-113">The **Win32\_MotherboardDevice** class has these methods.</span></span>



| <span data-ttu-id="9f8e0-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="9f8e0-114">Method</span></span>            | <span data-ttu-id="9f8e0-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f8e0-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f8e0-116">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-116">**Reset**</span></span>         | <span data-ttu-id="9f8e0-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-117">Not implemented.</span></span> <span data-ttu-id="9f8e0-118">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="9f8e0-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-119">**SetPowerState**</span></span> | <span data-ttu-id="9f8e0-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-120">Not implemented.</span></span> <span data-ttu-id="9f8e0-121">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9f8e0-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f8e0-122">Properties</span></span>

<span data-ttu-id="9f8e0-123">La classe **Win32 \_ MotherboardDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-123">The **Win32\_MotherboardDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f8e0-124">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-127">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-128">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-128">Availability and status of the device.</span></span>

<span data-ttu-id="9f8e0-129">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9f8e0-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f8e0-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9f8e0-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-133">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="9f8e0-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9f8e0-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9f8e0-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9f8e0-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9f8e0-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="9f8e0-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9f8e0-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="9f8e0-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9f8e0-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9f8e0-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9f8e0-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9f8e0-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9f8e0-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-144">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9f8e0-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-146">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9f8e0-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-148">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9f8e0-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9f8e0-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-151">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9f8e0-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-153">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9f8e0-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-155">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9f8e0-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-157">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9f8e0-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-159">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9f8e0-160">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-163">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-163">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-164">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-164">Short description of the object a one-line string.</span></span>

<span data-ttu-id="9f8e0-165">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-167">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-169">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-169">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-170">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="9f8e0-171">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9f8e0-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="9f8e0-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-174">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9f8e0-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="9f8e0-176">(1)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-177">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9f8e0-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9f8e0-179">(2)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9f8e0-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9f8e0-181">(3)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-182">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9f8e0-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9f8e0-184">(4)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-185">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-185">Device is not working properly.</span></span> <span data-ttu-id="9f8e0-186">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9f8e0-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9f8e0-188">(5)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-189">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9f8e0-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9f8e0-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-192">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9f8e0-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="9f8e0-194">(7)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9f8e0-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9f8e0-196">(8)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-197">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9f8e0-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9f8e0-199">(9)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-200">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-200">Device is not working properly.</span></span> <span data-ttu-id="9f8e0-201">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9f8e0-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="9f8e0-203">(10)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-204">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9f8e0-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="9f8e0-206">(11)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-207">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9f8e0-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9f8e0-209">12</span><span class="sxs-lookup"><span data-stu-id="9f8e0-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-210">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9f8e0-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9f8e0-212">(13)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-213">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9f8e0-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9f8e0-215">(14)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-216">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9f8e0-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9f8e0-218">(15)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-219">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9f8e0-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9f8e0-221">(16)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-222">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9f8e0-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9f8e0-224">(17)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-225">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9f8e0-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9f8e0-227">(18)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-228">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9f8e0-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="9f8e0-230">(19)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9f8e0-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="9f8e0-232">(20)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-233">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9f8e0-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9f8e0-235">(21)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-236">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-236">System failure.</span></span> <span data-ttu-id="9f8e0-237">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="9f8e0-238">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9f8e0-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="9f8e0-240">(22)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-241">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9f8e0-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9f8e0-243">(23)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-244">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-244">System failure.</span></span> <span data-ttu-id="9f8e0-245">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9f8e0-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9f8e0-247">(24)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-248">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9f8e0-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9f8e0-250">(25)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-251">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9f8e0-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9f8e0-253">(26)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-254">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9f8e0-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9f8e0-256">(27)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-257">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9f8e0-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9f8e0-259">(28)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-260">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9f8e0-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9f8e0-262">(29)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-263">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-263">Device is disabled.</span></span> <span data-ttu-id="9f8e0-264">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9f8e0-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9f8e0-266">(30)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-267">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9f8e0-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9f8e0-269">31</span><span class="sxs-lookup"><span data-stu-id="9f8e0-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-270">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-270">Device is not working properly.</span></span> <span data-ttu-id="9f8e0-271">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9f8e0-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-273">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-275">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-275">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-276">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9f8e0-277">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-278">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-278">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-279">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-281">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-281">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-282">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-282">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="9f8e0-283">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-283">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="9f8e0-284">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-285">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-285">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-288">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-288">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-289">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-289">Description of the object.</span></span>

<span data-ttu-id="9f8e0-290">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-291">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-291">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-292">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-294">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-294">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-295">Identificatore univoco di questa scheda madre.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-295">Unique identifier of this motherboard.</span></span>

<span data-ttu-id="9f8e0-296">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-298">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-300">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-300">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="9f8e0-301">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-303">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-305">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-305">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="9f8e0-306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-307">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-307">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-308">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-308">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-310">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-311">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-311">Date and time the object was installed.</span></span> <span data-ttu-id="9f8e0-312">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-312">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9f8e0-313">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-314">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-314">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-315">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-317">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-317">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9f8e0-318">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-319">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-320">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-322">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-322">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-323">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-323">Label by which the object is known.</span></span> <span data-ttu-id="9f8e0-324">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-324">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="9f8e0-325">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-325">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-326">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-326">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-327">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-329">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-329">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-330">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-330">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="9f8e0-331">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9f8e0-332">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="9f8e0-332">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-333">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-333">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-334">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-334">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-336">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-336">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="9f8e0-337">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-337">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f8e0-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9f8e0-339"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-339"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9f8e0-340"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-340"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9f8e0-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-342">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-342">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9f8e0-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-344">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-344">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9f8e0-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-346">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-346">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="9f8e0-347">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-347">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="9f8e0-348">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-348">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9f8e0-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-350">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-350">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9f8e0-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9f8e0-352">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="9f8e0-352">Timed Power-On Supported</span></span>

<span data-ttu-id="9f8e0-353">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-353">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9f8e0-354">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-354">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-355">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-357">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-357">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="9f8e0-358">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-358">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="9f8e0-359">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-360">**PrimaryBusType**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-360">**PrimaryBusType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-361">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-363">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ hardware \\ \\ Description \\ \\ System \\ \\ MultifunctionAdapter \| Identifier")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-363">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DESCRIPTION\\\\System\\\\MultifunctionAdapter\|Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-364">Tipo di bus primario della scheda madre.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-364">Primary bus type of the motherboard.</span></span>

<span data-ttu-id="9f8e0-365">Esempio: "PCI"</span><span class="sxs-lookup"><span data-stu-id="9f8e0-365">Example: "PCI"</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-366">**RevisionNumber**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-366">**RevisionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-367">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-369">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ hardware \\ \\ Description \\ \\ System")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-369">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DESCRIPTION\\\\System")</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-370">Numero di revisione della scheda madre.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-370">Revision number of the motherboard.</span></span>

<span data-ttu-id="9f8e0-371">Esempio: "00"</span><span class="sxs-lookup"><span data-stu-id="9f8e0-371">Example: "00"</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-372">**SecondaryBusType**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-372">**SecondaryBusType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-373">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-375">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ hardware \\ \\ Description \\ \\ System \\ \\ MultifunctionAdapter \| Identifier")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DESCRIPTION\\\\System\\\\MultifunctionAdapter\|Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-376">Tipo di bus secondario della scheda madre.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-376">Secondary bus type of the motherboard.</span></span>

<span data-ttu-id="9f8e0-377">Esempio: "ISA"</span><span class="sxs-lookup"><span data-stu-id="9f8e0-377">Example: "ISA"</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-378">**Status**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-379">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-381">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-381">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-382">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-382">Current status of the object.</span></span> <span data-ttu-id="9f8e0-383">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-383">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="9f8e0-384">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-384">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="9f8e0-385">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="9f8e0-385">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9f8e0-386">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-386">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9f8e0-387">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-387">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9f8e0-388">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9f8e0-389">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="9f8e0-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9f8e0-390">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9f8e0-391">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9f8e0-392">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="9f8e0-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f8e0-393">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9f8e0-394">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9f8e0-395">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9f8e0-396">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9f8e0-397">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9f8e0-398">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9f8e0-399">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9f8e0-400">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9f8e0-401">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9f8e0-402">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-402">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-403">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-405">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9f8e0-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-406">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-406">State of the logical device.</span></span> <span data-ttu-id="9f8e0-407">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-407">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="9f8e0-408">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9f8e0-409">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-409">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f8e0-410">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-410">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9f8e0-411">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-411">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9f8e0-412">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-412">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9f8e0-413">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-413">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9f8e0-414">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-414">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-415">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-417">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-418">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-418">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="9f8e0-419">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f8e0-420">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-420">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8e0-421">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-422">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f8e0-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8e0-423">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f8e0-423">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f8e0-424">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-424">Name of the scoping system.</span></span>

<span data-ttu-id="9f8e0-425">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-425">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f8e0-426">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f8e0-426">Remarks</span></span>

<span data-ttu-id="9f8e0-427">La classe **Win32 \_ MotherboardDevice** è derivata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f8e0-427">The **Win32\_MotherboardDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9f8e0-428">Esempio</span><span class="sxs-lookup"><span data-stu-id="9f8e0-428">Examples</span></span>

<span data-ttu-id="9f8e0-429">Gli esempi di codice [JavaScript](https://Gallery.TechNet.Microsoft.Com/05bbadf8-1356-43a6-82fc-fcab40233fe5) e [PowerShell](https://Gallery.TechNet.Microsoft.Com/cb520044-836e-425c-8c12-a9586d1c0e6e) seguenti recuperano le informazioni sulla scheda madre.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-429">The following [JavaScript](https://Gallery.TechNet.Microsoft.Com/05bbadf8-1356-43a6-82fc-fcab40233fe5) and [PowerShell](https://Gallery.TechNet.Microsoft.Com/cb520044-836e-425c-8c12-a9586d1c0e6e) code samples retrieve motherboard information.</span></span>

<span data-ttu-id="9f8e0-430">Nell'esempio di codice VBScript seguente vengono recuperate le informazioni sulla scheda madre.</span><span class="sxs-lookup"><span data-stu-id="9f8e0-430">The following VBScript code sample retrieves motherboard information.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_MotherboardDevice") 
 
For Each objItem in colItems 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Primary Bus Type: " & objItem.PrimaryBusType 
    Wscript.Echo "Secondary Bus Type: " & objItem.SecondaryBusType 
    Wscript.Echo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="9f8e0-431">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f8e0-431">Requirements</span></span>



| <span data-ttu-id="9f8e0-432">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f8e0-432">Requirement</span></span> | <span data-ttu-id="9f8e0-433">Valore</span><span class="sxs-lookup"><span data-stu-id="9f8e0-433">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f8e0-434">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f8e0-434">Minimum supported client</span></span><br/> | <span data-ttu-id="9f8e0-435">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f8e0-435">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f8e0-436">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f8e0-436">Minimum supported server</span></span><br/> | <span data-ttu-id="9f8e0-437">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f8e0-437">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f8e0-438">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9f8e0-438">Namespace</span></span><br/>                | <span data-ttu-id="9f8e0-439">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9f8e0-439">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9f8e0-440">MOF</span><span class="sxs-lookup"><span data-stu-id="9f8e0-440">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f8e0-441"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f8e0-441"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f8e0-442">DLL</span><span class="sxs-lookup"><span data-stu-id="9f8e0-442">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f8e0-443"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f8e0-443"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f8e0-444">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f8e0-444">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f8e0-445">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="9f8e0-445">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="9f8e0-446">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="9f8e0-446">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

