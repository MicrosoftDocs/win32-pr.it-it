---
description: La \_ classe WMI della tastiera Win32 rappresenta una tastiera installata in un computer che esegue Windows.
ms.assetid: f42a8e4f-3db9-4f9a-88ca-336ec883e85b
ms.tgt_platform: multiple
title: Classe Win32_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Keyboard
- Win32_Keyboard.Reset
- Win32_Keyboard.SetPowerState
- Win32_Keyboard.Availability
- Win32_Keyboard.Caption
- Win32_Keyboard.ConfigManagerErrorCode
- Win32_Keyboard.ConfigManagerUserConfig
- Win32_Keyboard.CreationClassName
- Win32_Keyboard.Description
- Win32_Keyboard.DeviceID
- Win32_Keyboard.ErrorCleared
- Win32_Keyboard.ErrorDescription
- Win32_Keyboard.InstallDate
- Win32_Keyboard.IsLocked
- Win32_Keyboard.LastErrorCode
- Win32_Keyboard.Layout
- Win32_Keyboard.Name
- Win32_Keyboard.NumberOfFunctionKeys
- Win32_Keyboard.Password
- Win32_Keyboard.PNPDeviceID
- Win32_Keyboard.PowerManagementCapabilities
- Win32_Keyboard.PowerManagementSupported
- Win32_Keyboard.Status
- Win32_Keyboard.StatusInfo
- Win32_Keyboard.SystemCreationClassName
- Win32_Keyboard.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5d011b6757ffa3b9378421f29cde3cb77cc04789
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305170"
---
# <a name="win32_keyboard-class"></a><span data-ttu-id="bb2db-103">\_Classe della tastiera Win32</span><span class="sxs-lookup"><span data-stu-id="bb2db-103">Win32\_Keyboard class</span></span>

<span data-ttu-id="bb2db-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) della **\_ tastiera Win32** rappresenta una tastiera installata in un computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="bb2db-104">The **Win32\_Keyboard** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a keyboard installed on a computer system running Windows.</span></span>

<span data-ttu-id="bb2db-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="bb2db-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bb2db-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="bb2db-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb2db-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb2db-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Keyboard : CIM_Keyboard
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
  string   Layout;
  string   Name;
  uint16   NumberOfFunctionKeys;
  uint16   Password;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="bb2db-108">Members</span><span class="sxs-lookup"><span data-stu-id="bb2db-108">Members</span></span>

<span data-ttu-id="bb2db-109">La classe della **\_ tastiera Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bb2db-109">The **Win32\_Keyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="bb2db-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="bb2db-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="bb2db-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bb2db-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bb2db-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="bb2db-112">Methods</span></span>

<span data-ttu-id="bb2db-113">La classe della **\_ tastiera Win32** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bb2db-113">The **Win32\_Keyboard** class has these methods.</span></span>



| <span data-ttu-id="bb2db-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="bb2db-114">Method</span></span>            | <span data-ttu-id="bb2db-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb2db-115">Description</span></span>                                                                                                                                                                                            |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb2db-116">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="bb2db-116">**Reset**</span></span>         | <span data-ttu-id="bb2db-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="bb2db-117">Not implemented.</span></span> <span data-ttu-id="bb2db-118">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) nella [**\_ tastiera CIM**](cim-keyboard.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="bb2db-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Keyboard**](cim-keyboard.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="bb2db-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="bb2db-119">**SetPowerState**</span></span> | <span data-ttu-id="bb2db-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="bb2db-120">Not implemented.</span></span> <span data-ttu-id="bb2db-121">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) nella [**\_ tastiera CIM**](cim-keyboard.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="bb2db-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Keyboard**](cim-keyboard.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bb2db-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bb2db-122">Properties</span></span>

<span data-ttu-id="bb2db-123">La classe della **\_ tastiera Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb2db-123">The **Win32\_Keyboard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb2db-124">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="bb2db-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb2db-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-127">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="bb2db-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-128">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb2db-128">Availability and status of the device.</span></span>

<span data-ttu-id="bb2db-129">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bb2db-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="bb2db-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bb2db-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="bb2db-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="bb2db-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="bb2db-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-133">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="bb2db-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="bb2db-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="bb2db-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="bb2db-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="bb2db-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="bb2db-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="bb2db-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="bb2db-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="bb2db-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="bb2db-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="bb2db-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="bb2db-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="bb2db-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bb2db-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="bb2db-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="bb2db-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="bb2db-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="bb2db-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="bb2db-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="bb2db-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="bb2db-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-144">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="bb2db-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="bb2db-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="bb2db-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-146">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="bb2db-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="bb2db-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="bb2db-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-148">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="bb2db-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="bb2db-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="bb2db-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="bb2db-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="bb2db-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-151">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="bb2db-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="bb2db-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="bb2db-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-153">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="bb2db-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="bb2db-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="bb2db-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-155">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="bb2db-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="bb2db-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="bb2db-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-157">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="bb2db-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="bb2db-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="bb2db-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-159">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="bb2db-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bb2db-160">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="bb2db-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb2db-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-163">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="bb2db-163">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-164">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="bb2db-164">Short description of the object a one-line string.</span></span>

<span data-ttu-id="bb2db-165">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bb2db-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-167">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb2db-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-169">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bb2db-169">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-170">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bb2db-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="bb2db-171">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="bb2db-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="bb2db-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="bb2db-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-174">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="bb2db-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="bb2db-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="bb2db-176">(1)</span><span class="sxs-lookup"><span data-stu-id="bb2db-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-177">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="bb2db-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bb2db-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="bb2db-179">(2)</span><span class="sxs-lookup"><span data-stu-id="bb2db-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="bb2db-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="bb2db-181">(3)</span><span class="sxs-lookup"><span data-stu-id="bb2db-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-182">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="bb2db-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="bb2db-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="bb2db-184">(4)</span><span class="sxs-lookup"><span data-stu-id="bb2db-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-185">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="bb2db-185">Device is not working properly.</span></span> <span data-ttu-id="bb2db-186">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="bb2db-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="bb2db-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="bb2db-188">(5)</span><span class="sxs-lookup"><span data-stu-id="bb2db-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-189">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="bb2db-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="bb2db-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="bb2db-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="bb2db-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-192">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="bb2db-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="bb2db-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="bb2db-194">(7)</span><span class="sxs-lookup"><span data-stu-id="bb2db-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="bb2db-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="bb2db-196">(8)</span><span class="sxs-lookup"><span data-stu-id="bb2db-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-197">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="bb2db-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="bb2db-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="bb2db-199">(9)</span><span class="sxs-lookup"><span data-stu-id="bb2db-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-200">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="bb2db-200">Device is not working properly.</span></span> <span data-ttu-id="bb2db-201">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb2db-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="bb2db-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="bb2db-203">(10)</span><span class="sxs-lookup"><span data-stu-id="bb2db-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-204">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb2db-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="bb2db-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="bb2db-206">(11)</span><span class="sxs-lookup"><span data-stu-id="bb2db-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-207">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb2db-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="bb2db-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="bb2db-209">12</span><span class="sxs-lookup"><span data-stu-id="bb2db-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-210">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="bb2db-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="bb2db-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="bb2db-212">(13)</span><span class="sxs-lookup"><span data-stu-id="bb2db-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-213">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb2db-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="bb2db-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="bb2db-215">(14)</span><span class="sxs-lookup"><span data-stu-id="bb2db-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-216">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="bb2db-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="bb2db-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="bb2db-218">(15)</span><span class="sxs-lookup"><span data-stu-id="bb2db-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-219">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="bb2db-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="bb2db-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="bb2db-221">(16)</span><span class="sxs-lookup"><span data-stu-id="bb2db-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-222">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb2db-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="bb2db-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="bb2db-224">(17)</span><span class="sxs-lookup"><span data-stu-id="bb2db-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-225">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="bb2db-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bb2db-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="bb2db-227">(18)</span><span class="sxs-lookup"><span data-stu-id="bb2db-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-228">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb2db-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="bb2db-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="bb2db-230">(19)</span><span class="sxs-lookup"><span data-stu-id="bb2db-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="bb2db-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="bb2db-232">(20)</span><span class="sxs-lookup"><span data-stu-id="bb2db-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-233">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="bb2db-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="bb2db-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="bb2db-235">(21)</span><span class="sxs-lookup"><span data-stu-id="bb2db-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-236">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="bb2db-236">System failure.</span></span> <span data-ttu-id="bb2db-237">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="bb2db-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="bb2db-238">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb2db-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="bb2db-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="bb2db-240">(22)</span><span class="sxs-lookup"><span data-stu-id="bb2db-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-241">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bb2db-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="bb2db-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="bb2db-243">(23)</span><span class="sxs-lookup"><span data-stu-id="bb2db-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-244">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="bb2db-244">System failure.</span></span> <span data-ttu-id="bb2db-245">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="bb2db-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="bb2db-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="bb2db-247">(24)</span><span class="sxs-lookup"><span data-stu-id="bb2db-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-248">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="bb2db-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="bb2db-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="bb2db-250">(25)</span><span class="sxs-lookup"><span data-stu-id="bb2db-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-251">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb2db-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="bb2db-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="bb2db-253">(26)</span><span class="sxs-lookup"><span data-stu-id="bb2db-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-254">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb2db-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="bb2db-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="bb2db-256">(27)</span><span class="sxs-lookup"><span data-stu-id="bb2db-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-257">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="bb2db-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="bb2db-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="bb2db-259">(28)</span><span class="sxs-lookup"><span data-stu-id="bb2db-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-260">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="bb2db-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="bb2db-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="bb2db-262">(29)</span><span class="sxs-lookup"><span data-stu-id="bb2db-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-263">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bb2db-263">Device is disabled.</span></span> <span data-ttu-id="bb2db-264">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="bb2db-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="bb2db-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="bb2db-266">(30)</span><span class="sxs-lookup"><span data-stu-id="bb2db-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-267">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb2db-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bb2db-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb2db-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="bb2db-269">31</span><span class="sxs-lookup"><span data-stu-id="bb2db-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-270">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="bb2db-270">Device is not working properly.</span></span> <span data-ttu-id="bb2db-271">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="bb2db-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bb2db-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="bb2db-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-273">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bb2db-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-275">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bb2db-275">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-276">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="bb2db-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="bb2db-277">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-278">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bb2db-278">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-279">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb2db-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-281">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bb2db-281">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-282">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="bb2db-282">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="bb2db-283">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="bb2db-283">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="bb2db-284">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-285">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="bb2db-285">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb2db-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-288">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="bb2db-288">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-289">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bb2db-289">Description of the object.</span></span>

<span data-ttu-id="bb2db-290">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-291">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="bb2db-291">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-292">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb2db-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-294">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bb2db-294">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-295">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="bb2db-295">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="bb2db-296">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="bb2db-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-298">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bb2db-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-300">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="bb2db-300">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="bb2db-301">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="bb2db-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-303">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb2db-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-305">Altre informazioni sull'errore registrato in **LastErrorCode** e sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="bb2db-305">More information about the error recorded in **LastErrorCode**, and corrective actions that may be taken.</span></span>

<span data-ttu-id="bb2db-306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-307">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bb2db-307">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-308">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bb2db-308">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-310">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="bb2db-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-311">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bb2db-311">Date and time the object was installed.</span></span> <span data-ttu-id="bb2db-312">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="bb2db-312">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="bb2db-313">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-314">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="bb2db-314">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-315">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bb2db-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-317">Se **true**, il dispositivo è bloccato impedendo l'input o l'output dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bb2db-317">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="bb2db-318">Questa proprietà viene ereditata da [**CIM \_ UserDevice**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-318">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-319">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bb2db-319">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-320">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb2db-320">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-322">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="bb2db-322">Last error code reported by the logical device.</span></span>

<span data-ttu-id="bb2db-323">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-324">**Layout**</span><span class="sxs-lookup"><span data-stu-id="bb2db-324">**Layout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-325">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb2db-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-327">Stringa in formato libero che indica il layout della tastiera.</span><span class="sxs-lookup"><span data-stu-id="bb2db-327">Free-form string indicating the layout of the keyboard.</span></span>

<span data-ttu-id="bb2db-328">Questa proprietà viene ereditata [**dalla \_ tastiera CIM**](cim-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-328">This property is inherited from [**CIM\_Keyboard**](cim-keyboard.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-329">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bb2db-329">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-330">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb2db-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-332">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="bb2db-332">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-333">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="bb2db-333">Label by which the object is known.</span></span> <span data-ttu-id="bb2db-334">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="bb2db-334">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="bb2db-335">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-335">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-336">**NumberOfFunctionKeys**</span><span class="sxs-lookup"><span data-stu-id="bb2db-336">**NumberOfFunctionKeys**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-337">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb2db-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-339">Numero di tasti funzione sulla tastiera.</span><span class="sxs-lookup"><span data-stu-id="bb2db-339">Number of function keys on the keyboard.</span></span>

<span data-ttu-id="bb2db-340">Questa proprietà viene ereditata [**dalla \_ tastiera CIM**](cim-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-340">This property is inherited from [**CIM\_Keyboard**](cim-keyboard.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-341">**Password**</span><span class="sxs-lookup"><span data-stu-id="bb2db-341">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-342">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb2db-342">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-344">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sicurezza hardware del sistema DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="bb2db-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-345">Stato della password a livello hardware abilitato sulla tastiera (valore = 4), che impedisce l'input locale.</span><span class="sxs-lookup"><span data-stu-id="bb2db-345">Status of hardware-level password enabled at the keyboard (value=4), preventing local input.</span></span>

<span data-ttu-id="bb2db-346">Questa proprietà viene ereditata [**dalla \_ tastiera CIM**](cim-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-346">This property is inherited from [**CIM\_Keyboard**](cim-keyboard.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bb2db-347">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="bb2db-347">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bb2db-348">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="bb2db-348">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bb2db-349">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="bb2db-349">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bb2db-350">**Abilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="bb2db-350">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="bb2db-351">**Non implementato** (5)</span><span class="sxs-lookup"><span data-stu-id="bb2db-351">**Not Implemented** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bb2db-352">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="bb2db-352">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-353">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb2db-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-355">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bb2db-355">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-356">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="bb2db-356">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="bb2db-357">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-357">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="bb2db-358">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="bb2db-358">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-359">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bb2db-359">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-360">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb2db-360">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-362">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="bb2db-362">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="bb2db-363">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="bb2db-363">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bb2db-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bb2db-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="bb2db-365"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="bb2db-365"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bb2db-366"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="bb2db-366"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bb2db-367"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="bb2db-367"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-368">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="bb2db-368">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="bb2db-369"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="bb2db-369"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-370">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="bb2db-370">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="bb2db-371"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="bb2db-371"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-372">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="bb2db-372">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="bb2db-373">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="bb2db-373">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="bb2db-374">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="bb2db-374">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="bb2db-375"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="bb2db-375"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-376">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="bb2db-376">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="bb2db-377"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="bb2db-377"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="bb2db-378">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="bb2db-378">Timed Power-On Supported</span></span>

<span data-ttu-id="bb2db-379">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="bb2db-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bb2db-380">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="bb2db-380">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-381">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bb2db-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-383">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="bb2db-383">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="bb2db-384">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="bb2db-384">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="bb2db-385">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-386">**Status**</span><span class="sxs-lookup"><span data-stu-id="bb2db-386">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-387">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb2db-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-389">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="bb2db-389">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-390">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bb2db-390">Current status of the object.</span></span> <span data-ttu-id="bb2db-391">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="bb2db-391">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="bb2db-392">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="bb2db-392">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="bb2db-393">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="bb2db-393">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bb2db-394">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="bb2db-394">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bb2db-395">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="bb2db-395">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bb2db-396">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-396">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bb2db-397">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb2db-397">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="bb2db-398">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="bb2db-398">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bb2db-399">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="bb2db-399">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bb2db-400">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="bb2db-400">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bb2db-401">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="bb2db-401">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="bb2db-402">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="bb2db-402">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="bb2db-403">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="bb2db-403">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="bb2db-404">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="bb2db-404">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="bb2db-405">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="bb2db-405">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="bb2db-406">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="bb2db-406">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="bb2db-407">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="bb2db-407">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="bb2db-408">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="bb2db-408">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="bb2db-409">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="bb2db-409">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bb2db-410">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="bb2db-410">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-411">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb2db-411">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-412">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-413">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="bb2db-413">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-414">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="bb2db-414">State of the logical device.</span></span> <span data-ttu-id="bb2db-415">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="bb2db-415">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="bb2db-416">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-416">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bb2db-417">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="bb2db-417">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bb2db-418">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="bb2db-418">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bb2db-419">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="bb2db-419">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bb2db-420">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="bb2db-420">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="bb2db-421">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="bb2db-421">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bb2db-422">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bb2db-422">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-423">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb2db-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-424">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-425">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bb2db-425">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-426">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="bb2db-426">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="bb2db-427">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-428">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="bb2db-428">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb2db-429">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb2db-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb2db-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-431">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bb2db-431">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bb2db-432">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="bb2db-432">Name of the scoping system.</span></span>

<span data-ttu-id="bb2db-433">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-433">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb2db-434">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb2db-434">Remarks</span></span>

<span data-ttu-id="bb2db-435">La classe della **\_ tastiera Win32** è derivata [**dalla \_ tastiera CIM**](cim-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="bb2db-435">The **Win32\_Keyboard** class is derived from [**CIM\_Keyboard**](cim-keyboard.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bb2db-436">Esempio</span><span class="sxs-lookup"><span data-stu-id="bb2db-436">Examples</span></span>

<span data-ttu-id="bb2db-437">Il codice di PowerShell seguente consente di trovare una tastiera e un mouse senza fili.</span><span class="sxs-lookup"><span data-stu-id="bb2db-437">The following PowerShell code finds a wireless keyboard and mouse.</span></span>


```PowerShell
class = "win32_pointingdevice","win32_keyboard"

$class | % {gwmi $_ | ? description -match 'hid'} | ft description, PNPDeviceID -A -Wr
```



<span data-ttu-id="bb2db-438">Nell'esempio VBScript seguente sono elencate le proprietà della tastiera.</span><span class="sxs-lookup"><span data-stu-id="bb2db-438">The following VBScript sample lists the keyboard properties.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_Keyboard") 
For Each objItem in colItems 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Is Locked: " & objItem.IsLocked 
    Wscript.Echo "Layout: " & objItem.Layout 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Number of Function Keys: " & objItem.NumberOfFunctionKeys 
    Wscript.Echo "Password: " & objItem.Password 
    Wscript.Echo "PNP Device ID: " & objItem.PNPDeviceID 
Next
```



## <a name="requirements"></a><span data-ttu-id="bb2db-439">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb2db-439">Requirements</span></span>



| <span data-ttu-id="bb2db-440">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb2db-440">Requirement</span></span> | <span data-ttu-id="bb2db-441">Valore</span><span class="sxs-lookup"><span data-stu-id="bb2db-441">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb2db-442">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb2db-442">Minimum supported client</span></span><br/> | <span data-ttu-id="bb2db-443">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb2db-443">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bb2db-444">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb2db-444">Minimum supported server</span></span><br/> | <span data-ttu-id="bb2db-445">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb2db-445">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bb2db-446">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bb2db-446">Namespace</span></span><br/>                | <span data-ttu-id="bb2db-447">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="bb2db-447">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bb2db-448">MOF</span><span class="sxs-lookup"><span data-stu-id="bb2db-448">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb2db-449"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb2db-449"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb2db-450">DLL</span><span class="sxs-lookup"><span data-stu-id="bb2db-450">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb2db-451"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb2db-451"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb2db-452">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb2db-452">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb2db-453">**\_Tastiera CIM**</span><span class="sxs-lookup"><span data-stu-id="bb2db-453">**CIM\_Keyboard**</span></span>](cim-keyboard.md)
</dt> <dt>

[<span data-ttu-id="bb2db-454">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="bb2db-454">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

