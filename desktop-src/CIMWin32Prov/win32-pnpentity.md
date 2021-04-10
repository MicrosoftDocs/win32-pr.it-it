---
description: Epresents le proprietà di un dispositivo Plug and Play.
ms.assetid: 621f4410-8d8f-4afa-b0f0-beed263f3a13
ms.tgt_platform: multiple
title: Classe Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity
- Win32_PnPEntity.Reset
- Win32_PnPEntity.SetPowerState
- Win32_PnPEntity.Availability
- Win32_PnPEntity.Caption
- Win32_PnPEntity.ClassGuid
- Win32_PnPEntity.CompatibleID
- Win32_PnPEntity.ConfigManagerErrorCode
- Win32_PnPEntity.ConfigManagerUserConfig
- Win32_PnPEntity.CreationClassName
- Win32_PnPEntity.Description
- Win32_PnPEntity.DeviceID
- Win32_PnPEntity.ErrorCleared
- Win32_PnPEntity.ErrorDescription
- Win32_PnPEntity.HardwareID
- Win32_PnPEntity.InstallDate
- Win32_PnPEntity.LastErrorCode
- Win32_PnPEntity.Manufacturer
- Win32_PnPEntity.Name
- Win32_PnPEntity.PNPClass
- Win32_PnPEntity.PNPDeviceID
- Win32_PnPEntity.PowerManagementCapabilities
- Win32_PnPEntity.PowerManagementSupported
- Win32_PnPEntity.Present
- Win32_PnPEntity.Service
- Win32_PnPEntity.Status
- Win32_PnPEntity.StatusInfo
- Win32_PnPEntity.SystemCreationClassName
- Win32_PnPEntity.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62eaa59944c9b71a1b8b3520969122ab23350bba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126099"
---
# <a name="win32_pnpentity-class"></a><span data-ttu-id="952e3-103">Win32 \_ PnPEntity (classe)</span><span class="sxs-lookup"><span data-stu-id="952e3-103">Win32\_PnPEntity class</span></span>

<span data-ttu-id="952e3-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PnPEntity Win32** rappresenta le proprietà di un dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="952e3-104">The **Win32\_PnPEntity** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a Plug and Play device.</span></span> <span data-ttu-id="952e3-105">Plug and Play entità vengono visualizzate come voci nell'Gestione dispositivi disponibile nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="952e3-105">Plug and Play entities are shown as entries in the Device Manager located in Control Panel.</span></span>

<span data-ttu-id="952e3-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="952e3-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="952e3-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="952e3-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="952e3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="952e3-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FE28FD98-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPEntity : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  string   ClassGuid;
  string   CompatibleID[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   HardwareID[];
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  string   Name;
  string   PNPClass;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  boolean  Present;
  string   Service;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="952e3-109">Members</span><span class="sxs-lookup"><span data-stu-id="952e3-109">Members</span></span>

<span data-ttu-id="952e3-110">La classe **Win32 \_ PnPEntity** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="952e3-110">The **Win32\_PnPEntity** class has these types of members:</span></span>

-   [<span data-ttu-id="952e3-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="952e3-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="952e3-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="952e3-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="952e3-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="952e3-113">Methods</span></span>

<span data-ttu-id="952e3-114">La classe **Win32 \_ PnPEntity** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="952e3-114">The **Win32\_PnPEntity** class has these methods.</span></span>



| <span data-ttu-id="952e3-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="952e3-115">Method</span></span>                                                             | <span data-ttu-id="952e3-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="952e3-116">Description</span></span>                                                                                                                                                                                    |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="952e3-117">**Disabilita**</span><span class="sxs-lookup"><span data-stu-id="952e3-117">**Disable**</span></span>](disable-win32-pnpentity.md)                         | <span data-ttu-id="952e3-118">Disabilita questo dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="952e3-118">Disables this Plug and Play device.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="952e3-119">**Abilitare**</span><span class="sxs-lookup"><span data-stu-id="952e3-119">**Enable**</span></span>](enable-win32-pnpentity.md)                           | <span data-ttu-id="952e3-120">Abilita questa Plug and Play dispositivo.</span><span class="sxs-lookup"><span data-stu-id="952e3-120">Enables this Plug and Play device.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="952e3-121">**GetDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="952e3-121">**GetDeviceProperties**</span></span>](getdeviceproperties-win32-pnpentity.md) | <span data-ttu-id="952e3-122">Ottiene le proprietà specificate del dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="952e3-122">Gets the specified properties of this Plug and Play device.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="952e3-123">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="952e3-123">**Reset**</span></span>                                                          | <span data-ttu-id="952e3-124">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="952e3-124">Not implemented.</span></span> <span data-ttu-id="952e3-125">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-125">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="952e3-126">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="952e3-126">**SetPowerState**</span></span>                                                  | <span data-ttu-id="952e3-127">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="952e3-127">Not implemented.</span></span> <span data-ttu-id="952e3-128">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-128">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="952e3-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="952e3-129">Properties</span></span>

<span data-ttu-id="952e3-130">La classe **Win32 \_ PnPEntity** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="952e3-130">The **Win32\_PnPEntity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="952e3-131">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="952e3-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-132">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="952e3-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-134">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="952e3-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="952e3-135">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="952e3-135">Availability and status of the device.</span></span>

<span data-ttu-id="952e3-136">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="952e3-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="952e3-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="952e3-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="952e3-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="952e3-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="952e3-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-140">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="952e3-140">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="952e3-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="952e3-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="952e3-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="952e3-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="952e3-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="952e3-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="952e3-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="952e3-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="952e3-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="952e3-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="952e3-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="952e3-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="952e3-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="952e3-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="952e3-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="952e3-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="952e3-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="952e3-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="952e3-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="952e3-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-151">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="952e3-151">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="952e3-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="952e3-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-153">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="952e3-153">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="952e3-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="952e3-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-155">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="952e3-155">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="952e3-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="952e3-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="952e3-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="952e3-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-158">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="952e3-158">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="952e3-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="952e3-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-160">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="952e3-160">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="952e3-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="952e3-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-162">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="952e3-162">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="952e3-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="952e3-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-164">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="952e3-164">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="952e3-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="952e3-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-166">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="952e3-166">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="952e3-167">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="952e3-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="952e3-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-170">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="952e3-170">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="952e3-171">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="952e3-171">Short description of the object.</span></span>

<span data-ttu-id="952e3-172">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="952e3-173">**ClassGuid**</span><span class="sxs-lookup"><span data-stu-id="952e3-173">**ClassGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="952e3-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-176">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="952e3-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="952e3-177">Identificatore univoco globale (GUID) di questo dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="952e3-177">Globally unique identifier (GUID) of this Plug and Play device.</span></span>

</dd> <dt>

<span data-ttu-id="952e3-178">**CompatibleID**</span><span class="sxs-lookup"><span data-stu-id="952e3-178">**CompatibleID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-179">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="952e3-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="952e3-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="952e3-181">Una stringa di identificazione definita dal fornitore che viene utilizzata dal programma di installazione per associare un dispositivo a un file INF.</span><span class="sxs-lookup"><span data-stu-id="952e3-181">A vendor-defined identification string that Setup uses to match a device to an INF file.</span></span> <span data-ttu-id="952e3-182">A un dispositivo può essere associato un elenco di ID compatibili.</span><span class="sxs-lookup"><span data-stu-id="952e3-182">A device can have a list of compatible IDs associated with it.</span></span> <span data-ttu-id="952e3-183">Gli ID compatibili devono essere elencati in ordine di idoneità decrescente.</span><span class="sxs-lookup"><span data-stu-id="952e3-183">The compatible IDs should be listed in order of decreasing suitability.</span></span> <span data-ttu-id="952e3-184">Se il programma di installazione non è in grado di individuare un file INF corrispondente a uno degli ID hardware di un dispositivo, utilizza ID compatibili per individuare un file INF.</span><span class="sxs-lookup"><span data-stu-id="952e3-184">If Setup cannot locate an INF file that matches one of a device's hardware IDs, it uses compatible IDs to locate an INF file.</span></span> <span data-ttu-id="952e3-185">Un ID compatibile ha lo stesso formato di un **HardwareID**.</span><span class="sxs-lookup"><span data-stu-id="952e3-185">A compatible ID has the same format as a **HardwareID**.</span></span> <span data-ttu-id="952e3-186">Per ulteriori informazioni, vedere [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span><span class="sxs-lookup"><span data-stu-id="952e3-186">For more information, see [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span></span>

</dd> <dt>

<span data-ttu-id="952e3-187">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="952e3-187">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-188">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="952e3-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-190">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="952e3-190">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="952e3-191">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="952e3-191">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="952e3-192">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-192">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="952e3-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="952e3-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="952e3-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="952e3-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-195">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="952e3-195">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="952e3-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="952e3-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="952e3-197">(1)</span><span class="sxs-lookup"><span data-stu-id="952e3-197">(1)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-198">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="952e3-198">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="952e3-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="952e3-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="952e3-200">(2)</span><span class="sxs-lookup"><span data-stu-id="952e3-200">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="952e3-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="952e3-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="952e3-202">(3)</span><span class="sxs-lookup"><span data-stu-id="952e3-202">(3)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-203">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="952e3-203">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="952e3-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="952e3-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="952e3-205">(4)</span><span class="sxs-lookup"><span data-stu-id="952e3-205">(4)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-206">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="952e3-206">Device is not working properly.</span></span> <span data-ttu-id="952e3-207">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="952e3-207">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="952e3-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="952e3-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="952e3-209">(5)</span><span class="sxs-lookup"><span data-stu-id="952e3-209">(5)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-210">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="952e3-210">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="952e3-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="952e3-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="952e3-212"> (6)</span><span class="sxs-lookup"><span data-stu-id="952e3-212">(6)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-213">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="952e3-213">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="952e3-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="952e3-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="952e3-215">(7)</span><span class="sxs-lookup"><span data-stu-id="952e3-215">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="952e3-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="952e3-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="952e3-217">(8)</span><span class="sxs-lookup"><span data-stu-id="952e3-217">(8)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-218">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="952e3-218">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="952e3-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="952e3-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="952e3-220">(9)</span><span class="sxs-lookup"><span data-stu-id="952e3-220">(9)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-221">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="952e3-221">Device is not working properly.</span></span> <span data-ttu-id="952e3-222">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="952e3-222">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="952e3-223"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="952e3-223"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="952e3-224">(10)</span><span class="sxs-lookup"><span data-stu-id="952e3-224">(10)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-225">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="952e3-225">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="952e3-226"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="952e3-226"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="952e3-227">(11)</span><span class="sxs-lookup"><span data-stu-id="952e3-227">(11)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-228">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="952e3-228">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="952e3-229"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="952e3-229"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="952e3-230">12</span><span class="sxs-lookup"><span data-stu-id="952e3-230">(12)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-231">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="952e3-231">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="952e3-232"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="952e3-232"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="952e3-233">(13)</span><span class="sxs-lookup"><span data-stu-id="952e3-233">(13)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-234">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="952e3-234">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="952e3-235"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="952e3-235"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="952e3-236">(14)</span><span class="sxs-lookup"><span data-stu-id="952e3-236">(14)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-237">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="952e3-237">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="952e3-238"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="952e3-238"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="952e3-239">(15)</span><span class="sxs-lookup"><span data-stu-id="952e3-239">(15)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-240">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="952e3-240">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="952e3-241"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="952e3-241"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="952e3-242">(16)</span><span class="sxs-lookup"><span data-stu-id="952e3-242">(16)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-243">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="952e3-243">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="952e3-244"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="952e3-244"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="952e3-245">(17)</span><span class="sxs-lookup"><span data-stu-id="952e3-245">(17)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-246">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="952e3-246">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="952e3-247"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="952e3-247"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="952e3-248">(18)</span><span class="sxs-lookup"><span data-stu-id="952e3-248">(18)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-249">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="952e3-249">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="952e3-250"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="952e3-250"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="952e3-251">(19)</span><span class="sxs-lookup"><span data-stu-id="952e3-251">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="952e3-252"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="952e3-252"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="952e3-253">(20)</span><span class="sxs-lookup"><span data-stu-id="952e3-253">(20)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-254">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="952e3-254">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="952e3-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="952e3-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="952e3-256">(21)</span><span class="sxs-lookup"><span data-stu-id="952e3-256">(21)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-257">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="952e3-257">System failure.</span></span> <span data-ttu-id="952e3-258">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="952e3-258">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="952e3-259">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="952e3-259">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="952e3-260"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="952e3-260"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="952e3-261">(22)</span><span class="sxs-lookup"><span data-stu-id="952e3-261">(22)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-262">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="952e3-262">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="952e3-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="952e3-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="952e3-264">(23)</span><span class="sxs-lookup"><span data-stu-id="952e3-264">(23)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-265">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="952e3-265">System failure.</span></span> <span data-ttu-id="952e3-266">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="952e3-266">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="952e3-267"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="952e3-267"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="952e3-268">(24)</span><span class="sxs-lookup"><span data-stu-id="952e3-268">(24)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-269">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="952e3-269">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="952e3-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="952e3-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="952e3-271">(25)</span><span class="sxs-lookup"><span data-stu-id="952e3-271">(25)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-272">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="952e3-272">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="952e3-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="952e3-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="952e3-274">(26)</span><span class="sxs-lookup"><span data-stu-id="952e3-274">(26)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-275">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="952e3-275">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="952e3-276"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="952e3-276"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="952e3-277">(27)</span><span class="sxs-lookup"><span data-stu-id="952e3-277">(27)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-278">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="952e3-278">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="952e3-279"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="952e3-279"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="952e3-280">(28)</span><span class="sxs-lookup"><span data-stu-id="952e3-280">(28)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-281">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="952e3-281">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="952e3-282"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="952e3-282"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="952e3-283">(29)</span><span class="sxs-lookup"><span data-stu-id="952e3-283">(29)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-284">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="952e3-284">Device is disabled.</span></span> <span data-ttu-id="952e3-285">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="952e3-285">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="952e3-286"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="952e3-286"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="952e3-287">(30)</span><span class="sxs-lookup"><span data-stu-id="952e3-287">(30)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-288">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="952e3-288">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="952e3-289"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="952e3-289"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="952e3-290">31</span><span class="sxs-lookup"><span data-stu-id="952e3-290">(31)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-291">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="952e3-291">Device is not working properly.</span></span> <span data-ttu-id="952e3-292">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="952e3-292">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="952e3-293">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="952e3-293">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-294">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="952e3-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-296">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="952e3-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="952e3-297">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="952e3-297">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="952e3-298">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="952e3-299">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="952e3-299">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="952e3-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-302">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="952e3-302">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="952e3-303">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="952e3-303">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="952e3-304">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="952e3-304">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="952e3-305">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="952e3-306">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="952e3-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="952e3-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-309">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="952e3-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="952e3-310">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="952e3-310">Description of the object.</span></span>

<span data-ttu-id="952e3-311">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="952e3-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="952e3-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-313">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="952e3-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-315">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="952e3-315">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="952e3-316">Identificatore del dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="952e3-316">Identifier of the Plug and Play device.</span></span>

<span data-ttu-id="952e3-317">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="952e3-318">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="952e3-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-319">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="952e3-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="952e3-321">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="952e3-321">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="952e3-322">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="952e3-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="952e3-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="952e3-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="952e3-326">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="952e3-326">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="952e3-327">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="952e3-328">**HardwareID**</span><span class="sxs-lookup"><span data-stu-id="952e3-328">**HardwareID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-329">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="952e3-329">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="952e3-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="952e3-331">Una stringa di identificazione definita dal fornitore che viene utilizzata dal programma di installazione per associare un dispositivo a un file INF.</span><span class="sxs-lookup"><span data-stu-id="952e3-331">A vendor-defined identification string that Setup uses to match a device to an INF file.</span></span> <span data-ttu-id="952e3-332">In genere, a un dispositivo è associato un elenco di ID hardware.</span><span class="sxs-lookup"><span data-stu-id="952e3-332">Normally, a device has an associated list of hardware IDs.</span></span> <span data-ttu-id="952e3-333">Un'eccezione è rappresentata dal driver del bus 1394, che non utilizza gli ID hardware.</span><span class="sxs-lookup"><span data-stu-id="952e3-333">An exception is the 1394 bus driver, which does not use hardware IDs.</span></span> <span data-ttu-id="952e3-334">Il primo ID hardware nell'elenco deve essere l'ID del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="952e3-334">The first hardware ID in the list should be the device ID.</span></span> <span data-ttu-id="952e3-335">Gli ID rimanenti devono essere elencati in ordine di idoneità decrescente.</span><span class="sxs-lookup"><span data-stu-id="952e3-335">The remaining IDs should be listed in order of decreasing suitability.</span></span>

<span data-ttu-id="952e3-336">Gli ID hardware vengono visualizzati in uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="952e3-336">Hardware IDs appear in one the following formats:</span></span>

-   <span data-ttu-id="952e3-337">specifico enumeratore enumeratore- \\ Device-ID</span><span class="sxs-lookup"><span data-stu-id="952e3-337">enumerator\\enumerator-specific-device-ID</span></span>

    <span data-ttu-id="952e3-338">Questo è il formato più comune per i singoli dispositivi PnP.</span><span class="sxs-lookup"><span data-stu-id="952e3-338">This is the most common format for individual PnP devices.</span></span> <span data-ttu-id="952e3-339">Un esempio di enumeratore è il BIOS o ISAPNP.</span><span class="sxs-lookup"><span data-stu-id="952e3-339">An example of an enumerator is the BIOS or ISAPNP.</span></span>

-   <span data-ttu-id="952e3-340">\*ID specifico dell'enumeratore</span><span class="sxs-lookup"><span data-stu-id="952e3-340">\*enumerator-specific ID</span></span>

    <span data-ttu-id="952e3-341">Un asterisco ( \* ) indica l'utilizzo da parte di più enumeratori.</span><span class="sxs-lookup"><span data-stu-id="952e3-341">An asterisk (\*) indicates use by more than one enumerator.</span></span>

-   <span data-ttu-id="952e3-342">ID specifico del dispositivo</span><span class="sxs-lookup"><span data-stu-id="952e3-342">device-class-specific ID</span></span>

    <span data-ttu-id="952e3-343">Formato personalizzato.</span><span class="sxs-lookup"><span data-stu-id="952e3-343">A custom format.</span></span>

<span data-ttu-id="952e3-344">Esempi di ID hardware sono:</span><span class="sxs-lookup"><span data-stu-id="952e3-344">Examples of Hardware IDs are:</span></span>

<dl> <dd><span data-ttu-id="952e3-345">\\ \* PNPOF08 radice</span><span class="sxs-lookup"><span data-stu-id="952e3-345">root\\\*PNPOF08</span></span></dd> <dd><span data-ttu-id="952e3-346">PC \\ VEN \_ 1000&DEV \_ 001&SUBSYS \_ 00000000&rev \_ 02</span><span class="sxs-lookup"><span data-stu-id="952e3-346">PC\\VEN\_1000&DEV\_001&SUBSYS\_00000000&REV\_02</span></span></dd> </dl>

<span data-ttu-id="952e3-347">Per ulteriori informazioni, vedere [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span><span class="sxs-lookup"><span data-stu-id="952e3-347">For more information, see the [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span></span>

</dd> <dt>

<span data-ttu-id="952e3-348">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="952e3-348">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-349">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="952e3-349">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-351">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="952e3-351">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="952e3-352">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="952e3-352">Date and time the object was installed.</span></span> <span data-ttu-id="952e3-353">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="952e3-353">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="952e3-354">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-354">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="952e3-355">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="952e3-355">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-356">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="952e3-356">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="952e3-358">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="952e3-358">Last error code reported by the logical device.</span></span>

<span data-ttu-id="952e3-359">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="952e3-360">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="952e3-360">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-361">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="952e3-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-363">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="952e3-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="952e3-364">Nome del produttore del dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="952e3-364">Name of the manufacturer of the Plug and Play device.</span></span>

<span data-ttu-id="952e3-365">Esempio: "Acme"</span><span class="sxs-lookup"><span data-stu-id="952e3-365">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="952e3-366">**Nome**</span><span class="sxs-lookup"><span data-stu-id="952e3-366">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-367">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="952e3-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-369">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="952e3-369">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="952e3-370">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="952e3-370">Label by which the object is known.</span></span> <span data-ttu-id="952e3-371">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="952e3-371">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="952e3-372">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="952e3-373">**PNPClass**</span><span class="sxs-lookup"><span data-stu-id="952e3-373">**PNPClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-374">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="952e3-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-376">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="952e3-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

> [!WARNING]
> <span data-ttu-id="952e3-377">Questa proprietà, nonostante sia elencata nel file MOF, non esiste effettivamente nella classe.</span><span class="sxs-lookup"><span data-stu-id="952e3-377">This property, despite being listed in the MOF file, does not actually exist in the class.</span></span> <span data-ttu-id="952e3-378">La proprietà viene descritta solo per motivi di completezza e per chiarire il file MOF.</span><span class="sxs-lookup"><span data-stu-id="952e3-378">The property is described here only for the sake of completeness, and to clarify the MOF file itself.</span></span>

 

<span data-ttu-id="952e3-379">Nome del tipo di questo dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="952e3-379">The name of the type of this Plug and Play device.</span></span>

<span data-ttu-id="952e3-380">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è presente nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="952e3-380">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not in the MOF file.</span></span>

</dd> <dt>

<span data-ttu-id="952e3-381">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="952e3-381">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-382">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="952e3-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-384">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="952e3-384">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="952e3-385">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="952e3-385">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="952e3-386">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-386">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="952e3-387">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="952e3-387">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="952e3-388">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="952e3-388">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-389">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="952e3-389">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="952e3-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="952e3-391">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="952e3-391">Not implemented.</span></span>

<span data-ttu-id="952e3-392">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="952e3-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="952e3-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-394">Le capacità relative al risparmio di energia sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="952e3-394">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="952e3-395"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="952e3-395"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-396">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="952e3-396">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="952e3-397"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="952e3-397"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-398">Le capacità correlate all'alimentazione sono state disabilitate.</span><span class="sxs-lookup"><span data-stu-id="952e3-398">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="952e3-399"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="952e3-399"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-400">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="952e3-400">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="952e3-401"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="952e3-401"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-402">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="952e3-402">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="952e3-403"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="952e3-403"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-404">Il metodo **SetPowerState** è supportato.</span><span class="sxs-lookup"><span data-stu-id="952e3-404">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="952e3-405">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="952e3-405">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="952e3-406">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-406">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="952e3-407"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="952e3-407"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-408">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").</span><span class="sxs-lookup"><span data-stu-id="952e3-408">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="952e3-409"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="952e3-409"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="952e3-410">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e il parametro *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="952e3-410">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="952e3-411">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="952e3-411">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-412">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="952e3-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="952e3-414">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="952e3-414">Not implemented.</span></span>

<span data-ttu-id="952e3-415">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="952e3-416">**Presente**</span><span class="sxs-lookup"><span data-stu-id="952e3-416">**Present**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-417">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="952e3-417">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-418">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-419">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="952e3-419">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="952e3-420">Indica se il dispositivo Plug and Play è attualmente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="952e3-420">Whether this Plug and Play device is currently in the system.</span></span>

<span data-ttu-id="952e3-421">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="952e3-421">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="952e3-422">**Servizio**</span><span class="sxs-lookup"><span data-stu-id="952e3-422">**Service**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-423">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="952e3-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-424">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-425">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="952e3-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="952e3-426">Nome del servizio che supporta questo dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="952e3-426">Name of the service that supports this Plug and Play device.</span></span> <span data-ttu-id="952e3-427">Per ulteriori informazioni, vedere [**Win32 \_ SystemDriverPnPEntity**](win32-systemdriverpnpentity.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-427">For more information, see [**Win32\_SystemDriverPnPEntity**](win32-systemdriverpnpentity.md).</span></span>

<span data-ttu-id="952e3-428">Esempio: "ATAPI"</span><span class="sxs-lookup"><span data-stu-id="952e3-428">Example: "atapi"</span></span>

</dd> <dt>

<span data-ttu-id="952e3-429">**Status**</span><span class="sxs-lookup"><span data-stu-id="952e3-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-430">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="952e3-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-431">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-432">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="952e3-432">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="952e3-433">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="952e3-433">Current status of the object.</span></span> <span data-ttu-id="952e3-434">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="952e3-434">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="952e3-435">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="952e3-435">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="952e3-436">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="952e3-436">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="952e3-437">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="952e3-437">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="952e3-438">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="952e3-438">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="952e3-439">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="952e3-440">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="952e3-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="952e3-441">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="952e3-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="952e3-442">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="952e3-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="952e3-443">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="952e3-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="952e3-444">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="952e3-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="952e3-445">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="952e3-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="952e3-446">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="952e3-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="952e3-447">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="952e3-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="952e3-448">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="952e3-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="952e3-449">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="952e3-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="952e3-450">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="952e3-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="952e3-451">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="952e3-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="952e3-452">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="952e3-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="952e3-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="952e3-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-454">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="952e3-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-455">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-456">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="952e3-456">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="952e3-457">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="952e3-457">State of the logical device.</span></span> <span data-ttu-id="952e3-458">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="952e3-458">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="952e3-459">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="952e3-460">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="952e3-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="952e3-461">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="952e3-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="952e3-462">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="952e3-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="952e3-463">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="952e3-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="952e3-464">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="952e3-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="952e3-465">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="952e3-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-466">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="952e3-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-467">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-468">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="952e3-468">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="952e3-469">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="952e3-469">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="952e3-470">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="952e3-471">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="952e3-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="952e3-472">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="952e3-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="952e3-473">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="952e3-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="952e3-474">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="952e3-474">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="952e3-475">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="952e3-475">Name of the scoping system.</span></span>

<span data-ttu-id="952e3-476">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="952e3-477">Commenti</span><span class="sxs-lookup"><span data-stu-id="952e3-477">Remarks</span></span>

<span data-ttu-id="952e3-478">La classe **Win32 \_ PnPEntity** è derivata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="952e3-478">The **Win32\_PnPEntity** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="952e3-479">Esempio</span><span class="sxs-lookup"><span data-stu-id="952e3-479">Examples</span></span>

<span data-ttu-id="952e3-480">Nell'esempio [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell della raccolta TechNet viene usato **per \_ PnPEntity Win32** per recuperare un elenco di hardware non funzionante con WMI.</span><span class="sxs-lookup"><span data-stu-id="952e3-480">The [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell sample on TechNet Gallery uses to **Win32\_PnPEntity** to retrieve a list of non-working hardware using WMI.</span></span>

<span data-ttu-id="952e3-481">L'esempio di codice VBScript seguente consente di connettersi a un gruppo di computer remoti nello stesso dominio creando una matrice di nomi di computer remoti e visualizzando quindi i nomi dei dispositivi Plug and Play, ovvero le istanze di Win32 \_ PnPEntity, in ogni computer.</span><span class="sxs-lookup"><span data-stu-id="952e3-481">The following VBScript code example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of Win32\_PnPEntity—on each computer.</span></span>


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer& "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



## <a name="requirements"></a><span data-ttu-id="952e3-482">Requisiti</span><span class="sxs-lookup"><span data-stu-id="952e3-482">Requirements</span></span>



| <span data-ttu-id="952e3-483">Requisito</span><span class="sxs-lookup"><span data-stu-id="952e3-483">Requirement</span></span> | <span data-ttu-id="952e3-484">Valore</span><span class="sxs-lookup"><span data-stu-id="952e3-484">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="952e3-485">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="952e3-485">Minimum supported client</span></span><br/> | <span data-ttu-id="952e3-486">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="952e3-486">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="952e3-487">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="952e3-487">Minimum supported server</span></span><br/> | <span data-ttu-id="952e3-488">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="952e3-488">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="952e3-489">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="952e3-489">Namespace</span></span><br/>                | <span data-ttu-id="952e3-490">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="952e3-490">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="952e3-491">MOF</span><span class="sxs-lookup"><span data-stu-id="952e3-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="952e3-492"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="952e3-492"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="952e3-493">DLL</span><span class="sxs-lookup"><span data-stu-id="952e3-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="952e3-494"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="952e3-494"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="952e3-495">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="952e3-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="952e3-496">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="952e3-496">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="952e3-497">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="952e3-497">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="952e3-498">Connessione a WMI in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="952e3-498">Connecting to WMI on a Remote Computer</span></span>](../wmisdk/connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="952e3-499">Attività WMI: hardware del computer</span><span class="sxs-lookup"><span data-stu-id="952e3-499">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
