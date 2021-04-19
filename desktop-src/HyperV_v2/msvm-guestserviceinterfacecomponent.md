---
description: Rappresenta lo stato del componente dell'interfaccia del servizio Guest, che fornisce un meccanismo per interagire con la macchina virtuale dalle interfacce di gestione nel sistema host.
ms.assetid: 9A158B42-052B-42B3-8539-00927056306D
title: Classe Msvm_GuestServiceInterfaceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent
- Msvm_GuestServiceInterfaceComponent.Availability
- Msvm_GuestServiceInterfaceComponent.Caption
- Msvm_GuestServiceInterfaceComponent.ConfigManagerErrorCode
- Msvm_GuestServiceInterfaceComponent.ConfigManagerUserConfig
- Msvm_GuestServiceInterfaceComponent.CreationClassName
- Msvm_GuestServiceInterfaceComponent.Description
- Msvm_GuestServiceInterfaceComponent.DeviceID
- Msvm_GuestServiceInterfaceComponent.ErrorCleared
- Msvm_GuestServiceInterfaceComponent.ErrorDescription
- Msvm_GuestServiceInterfaceComponent.InstallDate
- Msvm_GuestServiceInterfaceComponent.LastErrorCode
- Msvm_GuestServiceInterfaceComponent.Name
- Msvm_GuestServiceInterfaceComponent.PNPDeviceID
- Msvm_GuestServiceInterfaceComponent.PowerManagementCapabilities
- Msvm_GuestServiceInterfaceComponent.PowerManagementSupported
- Msvm_GuestServiceInterfaceComponent.Status
- Msvm_GuestServiceInterfaceComponent.StatusInfo
- Msvm_GuestServiceInterfaceComponent.SystemCreationClassName
- Msvm_GuestServiceInterfaceComponent.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4c55417edeee6d9a9fb15c474ba4ee9ca2dd93f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307907"
---
# <a name="msvm_guestserviceinterfacecomponent-class"></a><span data-ttu-id="944bb-103">\_Classe MSVM GuestServiceInterfaceComponent</span><span class="sxs-lookup"><span data-stu-id="944bb-103">Msvm\_GuestServiceInterfaceComponent class</span></span>

<span data-ttu-id="944bb-104">Rappresenta lo stato del componente dell'interfaccia del servizio Guest, che fornisce un meccanismo per interagire con la macchina virtuale dalle interfacce di gestione nel sistema host.</span><span class="sxs-lookup"><span data-stu-id="944bb-104">Represents the state of the guest service interface component, which provides a mechanism to interact with the virtual machine from the management interfaces on the host system.</span></span> <span data-ttu-id="944bb-105">Questa classe deriva dalla classe [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) .</span><span class="sxs-lookup"><span data-stu-id="944bb-105">This class derives from the [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) class.</span></span>

<span data-ttu-id="944bb-106">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="944bb-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="944bb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="944bb-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponent : CIM_LogicalDevice
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
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="944bb-108">Members</span><span class="sxs-lookup"><span data-stu-id="944bb-108">Members</span></span>

<span data-ttu-id="944bb-109">La **classe \_ GuestServiceInterfaceComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="944bb-109">The **Msvm\_GuestServiceInterfaceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="944bb-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="944bb-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="944bb-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="944bb-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="944bb-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="944bb-112">Methods</span></span>

<span data-ttu-id="944bb-113">La **classe \_ GuestServiceInterfaceComponent di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="944bb-113">The **Msvm\_GuestServiceInterfaceComponent** class has these methods.</span></span>



| <span data-ttu-id="944bb-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="944bb-114">Method</span></span>                                                                               | <span data-ttu-id="944bb-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="944bb-115">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="944bb-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="944bb-116">**RequestStateChange**</span></span>](requeststatechange-msvm-guestserviceinterfacecomponent.md) | <span data-ttu-id="944bb-117">Richiede che lo stato del componente dell'interfaccia del servizio Guest venga modificato nel valore specificato.</span><span class="sxs-lookup"><span data-stu-id="944bb-117">Requests that the state of the guest service interface component be changed to the specified value.</span></span><br/>                           |
| [<span data-ttu-id="944bb-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="944bb-118">**Reset**</span></span>](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | <span data-ttu-id="944bb-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="944bb-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="944bb-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="944bb-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="944bb-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="944bb-121">**SetPowerState**</span></span>](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | <span data-ttu-id="944bb-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="944bb-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="944bb-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="944bb-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="944bb-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="944bb-124">Properties</span></span>

<span data-ttu-id="944bb-125">La **classe \_ GuestServiceInterfaceComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="944bb-125">The **Msvm\_GuestServiceInterfaceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="944bb-126">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="944bb-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="944bb-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-129">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="944bb-129">Availability and status of the device.</span></span>



| <span data-ttu-id="944bb-130">Valore</span><span class="sxs-lookup"><span data-stu-id="944bb-130">Value</span></span>                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="944bb-131">Significato</span><span class="sxs-lookup"><span data-stu-id="944bb-131">Meaning</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="944bb-132"><dt>**Other**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-132"><dt>**Other**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="944bb-133"><dt>**Sconosciuto**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-133"><dt>**Unknown**</dt> <dt>2 (0x2)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> <span data-ttu-id="944bb-134"><dt>**Running/complete Power**</dt> <dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-134"><dt>**Running/Full Power**</dt> <dt>3 (0x3)</dt></span></span> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <span data-ttu-id="944bb-135"><dt>**Avviso**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-135"><dt>**Warning**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="944bb-136"><dt>**Nel test**</dt> <dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-136"><dt>**In Test**</dt> <dt>5 (0x5)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="944bb-137"><dt>**Non applicabile**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-137"><dt>**Not Applicable**</dt> <dt>6 (0x6)</dt></span></span> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <span data-ttu-id="944bb-138"><dt>**Spegnere**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-138"><dt>**Power Off**</dt> <dt>7 (0x7)</dt></span></span> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <span data-ttu-id="944bb-139"><dt>**Off line**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-139"><dt>**Off Line**</dt> <dt>8 (0x8)</dt></span></span> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <span data-ttu-id="944bb-140"><dt>**Off Duty**</dt> <dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-140"><dt>**Off Duty**</dt> <dt>9 (0x9)</dt></span></span> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="944bb-141"><dt>**Danneggiato**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-141"><dt>**Degraded**</dt> <dt>10 (0xA)</dt></span></span> </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <span data-ttu-id="944bb-142"><dt>**Non installato**</dt> <dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-142"><dt>**Not Installed**</dt> <dt>11 (0xB)</dt></span></span> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <span data-ttu-id="944bb-143"><dt>**Errore di installazione**</dt> <dt>12 (0xC)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-143"><dt>**Install Error**</dt> <dt>12 (0xC)</dt></span></span> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> <span data-ttu-id="944bb-144"><dt>**Risparmio energia-sconosciuto**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-144"><dt>**Power Save - Unknown**</dt> <dt>13 (0xD)</dt></span></span> </dl>                             | <span data-ttu-id="944bb-145">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="944bb-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span><br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> <span data-ttu-id="944bb-146"><dt>**Risparmio energia-modalità a basso consumo**</dt> <dt>14 (0xe)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-146"><dt>**Power Save - Low Power Mode**</dt> <dt>14 (0xE)</dt></span></span> </dl> | <span data-ttu-id="944bb-147">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="944bb-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span><br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> <span data-ttu-id="944bb-148"><dt>**Risparmio energia-standby**</dt> <dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-148"><dt>**Power Save - Standby**</dt> <dt>15 (0xF)</dt></span></span> </dl>                             | <span data-ttu-id="944bb-149">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="944bb-149">The device is not functioning but could be brought to full power quickly.</span></span><br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <span data-ttu-id="944bb-150"><dt>**Ciclo di alimentazione**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-150"><dt>**Power Cycle**</dt> <dt>16 (0x10)</dt></span></span> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> <span data-ttu-id="944bb-151"><dt>**Risparmio energia-avviso**</dt> <dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-151"><dt>**Power Save - Warning**</dt> <dt>17 (0x11)</dt></span></span> </dl>                            | <span data-ttu-id="944bb-152">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="944bb-152">The device is in a warning state, though also in a power save mode.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="944bb-153">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="944bb-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="944bb-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-156">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="944bb-156">Short textual description of the object.</span></span> <span data-ttu-id="944bb-157">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="944bb-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="944bb-158">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="944bb-158">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-159">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="944bb-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-161">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="944bb-161">Win32 Configuration Manager error code.</span></span>



| <span data-ttu-id="944bb-162">Valore</span><span class="sxs-lookup"><span data-stu-id="944bb-162">Value</span></span>                                                                                | <span data-ttu-id="944bb-163">Significato</span><span class="sxs-lookup"><span data-stu-id="944bb-163">Meaning</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="944bb-164"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-164"><dt>0 (0x0)</dt></span></span> </dl>   | <span data-ttu-id="944bb-165">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="944bb-165">Device is working properly.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="944bb-166"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-166"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="944bb-167">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="944bb-167">Device is not configured correctly.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="944bb-168"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-168"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="944bb-169">Windows non è in grado di caricare il driver per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="944bb-169">Windows cannot load the driver for this device.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="944bb-170"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-170"><dt>3 (0x3)</dt></span></span> </dl>   | <span data-ttu-id="944bb-171">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="944bb-171">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span><br/>                             |
| <dl> <span data-ttu-id="944bb-172"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-172"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="944bb-173">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="944bb-173">Device is not working properly.</span></span> <span data-ttu-id="944bb-174">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="944bb-174">One of its drivers or the registry might be corrupted.</span></span><br/>                                        |
| <dl> <span data-ttu-id="944bb-175"><dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-175"><dt>5 (0x5)</dt></span></span> </dl>   | <span data-ttu-id="944bb-176">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="944bb-176">Driver for the device requires a resource that Windows cannot manage.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="944bb-177"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-177"><dt>6 (0x6)</dt></span></span> </dl>   | <span data-ttu-id="944bb-178">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="944bb-178">Boot configuration for the device conflicts with other devices.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="944bb-179"><dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-179"><dt>7 (0x7)</dt></span></span> </dl>   | <span data-ttu-id="944bb-180">Impossibile filtrare.</span><span class="sxs-lookup"><span data-stu-id="944bb-180">Cannot filter.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="944bb-181"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-181"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="944bb-182">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="944bb-182">Driver loader for the device is missing.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="944bb-183"><dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-183"><dt>9 (0x9)</dt></span></span> </dl>   | <span data-ttu-id="944bb-184">Il dispositivo non funziona correttamente; il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="944bb-184">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span><br/>               |
| <dl> <span data-ttu-id="944bb-185"><dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-185"><dt>10 (0xA)</dt></span></span> </dl>  | <span data-ttu-id="944bb-186">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="944bb-186">Device cannot start.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="944bb-187"><dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-187"><dt>11 (0xB)</dt></span></span> </dl>  | <span data-ttu-id="944bb-188">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="944bb-188">Device failed.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="944bb-189"><dt>12 (0xC)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-189"><dt>12 (0xC)</dt></span></span> </dl>  | <span data-ttu-id="944bb-190">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="944bb-190">Device cannot find enough free resources to use.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="944bb-191"><dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-191"><dt>13 (0xD)</dt></span></span> </dl>  | <span data-ttu-id="944bb-192">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="944bb-192">Windows cannot verify the device's resources.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="944bb-193"><dt>14 (0xE)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-193"><dt>14 (0xE)</dt></span></span> </dl>  | <span data-ttu-id="944bb-194">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="944bb-194">Device cannot work properly until the computer is restarted.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="944bb-195"><dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-195"><dt>15 (0xF)</dt></span></span> </dl>  | <span data-ttu-id="944bb-196">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="944bb-196">Device is not working properly due to a possible re-enumeration problem.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="944bb-197"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-197"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="944bb-198">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="944bb-198">Windows cannot identify all of the resources that the device uses.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="944bb-199"><dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-199"><dt>17 (0x11)</dt></span></span> </dl> | <span data-ttu-id="944bb-200">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="944bb-200">Device is requesting an unknown resource type.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="944bb-201"><dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-201"><dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="944bb-202">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="944bb-202">Device drivers must be reinstalled.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="944bb-203"><dt>19 (0x13)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-203"><dt>19 (0x13)</dt></span></span> </dl> | <span data-ttu-id="944bb-204">Errore durante l'utilizzo del caricatore VxD.</span><span class="sxs-lookup"><span data-stu-id="944bb-204">Failure using the VxD loader.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="944bb-205"><dt>20 (0x14)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-205"><dt>20 (0x14)</dt></span></span> </dl> | <span data-ttu-id="944bb-206">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="944bb-206">Registry might be corrupted.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="944bb-207"><dt>21 (0x15)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-207"><dt>21 (0x15)</dt></span></span> </dl> | <span data-ttu-id="944bb-208">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="944bb-208">System failure.</span></span> <span data-ttu-id="944bb-209">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="944bb-209">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="944bb-210">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="944bb-210">Windows is removing the device.</span></span><br/> |
| <dl> <span data-ttu-id="944bb-211"><dt>22 (0x16)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-211"><dt>22 (0x16)</dt></span></span> </dl> | <span data-ttu-id="944bb-212">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="944bb-212">Device is disabled.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="944bb-213"><dt>23 (0x17)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-213"><dt>23 (0x17)</dt></span></span> </dl> | <span data-ttu-id="944bb-214">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="944bb-214">System failure.</span></span> <span data-ttu-id="944bb-215">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="944bb-215">If changing the device driver is ineffective, see the hardware documentation.</span></span><br/>                                 |
| <dl> <span data-ttu-id="944bb-216"><dt>24 (0x18)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-216"><dt>24 (0x18)</dt></span></span> </dl> | <span data-ttu-id="944bb-217">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="944bb-217">Device is not present, not working properly, or does not have all of its drivers installed.</span></span><br/>                                   |
| <dl> <span data-ttu-id="944bb-218"><dt>25 (0x19)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-218"><dt>25 (0x19)</dt></span></span> </dl> | <span data-ttu-id="944bb-219">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="944bb-219">Windows is still setting up the device.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="944bb-220"><dt>26 (0x1A)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-220"><dt>26 (0x1A)</dt></span></span> </dl> | <span data-ttu-id="944bb-221">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="944bb-221">Windows is still setting up the device.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="944bb-222"><dt>27 (0x1B)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-222"><dt>27 (0x1B)</dt></span></span> </dl> | <span data-ttu-id="944bb-223">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="944bb-223">Device does not have valid log configuration.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="944bb-224"><dt>28 (0x1C)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-224"><dt>28 (0x1C)</dt></span></span> </dl> | <span data-ttu-id="944bb-225">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="944bb-225">Device drivers are not installed.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="944bb-226"><dt>29 (0x1D)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-226"><dt>29 (0x1D)</dt></span></span> </dl> | <span data-ttu-id="944bb-227">Il dispositivo è disabilitato; il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="944bb-227">Device is disabled; the device firmware did not provide the required resources.</span></span><br/>                                               |
| <dl> <span data-ttu-id="944bb-228"><dt>30 (0x1E)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-228"><dt>30 (0x1E)</dt></span></span> </dl> | <span data-ttu-id="944bb-229">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="944bb-229">Device is using an IRQ resource that another device is using.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="944bb-230"><dt>31 (0x1F)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-230"><dt>31 (0x1F)</dt></span></span> </dl> | <span data-ttu-id="944bb-231">Il dispositivo non funziona correttamente; Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="944bb-231">Device is not working properly; Windows cannot load the required device drivers.</span></span><br/>                                              |



 

</dd> <dt>

<span data-ttu-id="944bb-232">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="944bb-232">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-233">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="944bb-233">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-235">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="944bb-235">If **TRUE**, the device is using a user-defined configuration.</span></span>

</dd> <dt>

<span data-ttu-id="944bb-236">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="944bb-236">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="944bb-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-239">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="944bb-239">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="944bb-240">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="944bb-240">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="944bb-241">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="944bb-241">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-242">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="944bb-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-244">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="944bb-244">Textual description of the object.</span></span> <span data-ttu-id="944bb-245">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="944bb-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="944bb-246">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="944bb-246">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-247">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="944bb-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-249">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="944bb-249">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="944bb-250">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="944bb-250">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-251">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="944bb-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-253">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="944bb-253">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

</dd> <dt>

<span data-ttu-id="944bb-254">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="944bb-254">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-255">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="944bb-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-257">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="944bb-257">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

</dd> <dt>

<span data-ttu-id="944bb-258">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="944bb-258">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-259">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="944bb-259">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-260">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-261">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="944bb-261">Date and time the object was installed.</span></span> <span data-ttu-id="944bb-262">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="944bb-262">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="944bb-263">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="944bb-263">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="944bb-264">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="944bb-264">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-265">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="944bb-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-266">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-267">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="944bb-267">Last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="944bb-268">**Nome**</span><span class="sxs-lookup"><span data-stu-id="944bb-268">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-269">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="944bb-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-271">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="944bb-271">Label by which the object is known.</span></span> <span data-ttu-id="944bb-272">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="944bb-272">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="944bb-273">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="944bb-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="944bb-274">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="944bb-274">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-275">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="944bb-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-277">Indica l'identificatore del dispositivo Plug and Play Win32 del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="944bb-277">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="944bb-278">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="944bb-278">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="944bb-279">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="944bb-279">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-280">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="944bb-280">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="944bb-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-282">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="944bb-282">Array of the specific power-related capabilities of a logical device.</span></span> <span data-ttu-id="944bb-283">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="944bb-283">This property is inherited from **CIM\_LogicalDevice**.</span></span>



| <span data-ttu-id="944bb-284">Valore</span><span class="sxs-lookup"><span data-stu-id="944bb-284">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="944bb-285">Significato</span><span class="sxs-lookup"><span data-stu-id="944bb-285">Meaning</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="944bb-286"><dt>**Sconosciuto**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-286"><dt>**Unknown**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <span data-ttu-id="944bb-287"><dt>**Non supportato**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-287"><dt>**Not Supported**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="944bb-288"><dt>**Disabilitato**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-288"><dt>**Disabled**</dt> <dt>2 (0x2)</dt></span></span> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="944bb-289"><dt>**Abilitato**</dt> <dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-289"><dt>**Enabled**</dt> <dt>3 (0x3)</dt></span></span> </dl>                                                                                                                                     | <span data-ttu-id="944bb-290">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="944bb-290">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span><br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> <span data-ttu-id="944bb-291"><dt>**Modalità di risparmio energia immesse automaticamente**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-291"><dt>**Power Saving Modes Entered Automatically**</dt> <dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="944bb-292">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="944bb-292">The device can change its power state based on usage or other criteria.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <span data-ttu-id="944bb-293"><dt>**Stato di alimentazione impostabile**</dt> <dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-293"><dt>**Power State Settable**</dt> <dt>5 (0x5)</dt></span></span> </dl>                                                                                 | <span data-ttu-id="944bb-294">Il metodo [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) è supportato.</span><span class="sxs-lookup"><span data-stu-id="944bb-294">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method is supported.</span></span> <span data-ttu-id="944bb-295">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="944bb-295">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="944bb-296">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="944bb-296">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span><br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <span data-ttu-id="944bb-297"><dt>**Power Cycling supportato**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-297"><dt>**Power Cycling Supported**</dt> <dt>6 (0x6)</dt></span></span> </dl>                                                                     | <span data-ttu-id="944bb-298">Il metodo [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").</span><span class="sxs-lookup"><span data-stu-id="944bb-298">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span><br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> <span data-ttu-id="944bb-299"><dt>**Accensione temporizzata su supportata**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-299"><dt>**Timed Power On Supported**</dt> <dt>7 (0x7)</dt></span></span> </dl>                                                                 | <span data-ttu-id="944bb-300">Il metodo [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="944bb-300">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and *Time* set to a specific date and time, or interval, for power-on.</span></span><br/>                                                                                       |



 

</dd> <dt>

<span data-ttu-id="944bb-301">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="944bb-301">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-302">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="944bb-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-304">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="944bb-304">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="944bb-305">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="944bb-305">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="944bb-306">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="944bb-306">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="944bb-307">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="944bb-307">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="944bb-308">**Status**</span><span class="sxs-lookup"><span data-stu-id="944bb-308">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-309">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="944bb-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-311">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="944bb-311">Current status of the object.</span></span> <span data-ttu-id="944bb-312">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="944bb-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="944bb-313">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="944bb-313">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="944bb-314">**OK**</span><span class="sxs-lookup"><span data-stu-id="944bb-314">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="944bb-315">**Errore**</span><span class="sxs-lookup"><span data-stu-id="944bb-315">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="944bb-316">**Degradato**</span><span class="sxs-lookup"><span data-stu-id="944bb-316">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="944bb-317">**Sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="944bb-317">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="944bb-318">**"Errore di predazione"**</span><span class="sxs-lookup"><span data-stu-id="944bb-318">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="944bb-319">**Avvio**</span><span class="sxs-lookup"><span data-stu-id="944bb-319">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="944bb-320">**Arresto**</span><span class="sxs-lookup"><span data-stu-id="944bb-320">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="944bb-321">**Servizio**</span><span class="sxs-lookup"><span data-stu-id="944bb-321">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="944bb-322">**Sottolineato**</span><span class="sxs-lookup"><span data-stu-id="944bb-322">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="944bb-323">**"Non ripristino"**</span><span class="sxs-lookup"><span data-stu-id="944bb-323">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="944bb-324">**"Nessun contatto"**</span><span class="sxs-lookup"><span data-stu-id="944bb-324">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="944bb-325">**"Lost comm"**</span><span class="sxs-lookup"><span data-stu-id="944bb-325">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="944bb-326">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="944bb-326">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-327">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="944bb-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-329">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="944bb-329">State of the logical device.</span></span> <span data-ttu-id="944bb-330">Se questa proprietà non è applicabile al dispositivo logico, è necessario utilizzare il valore 5 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="944bb-330">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span> <span data-ttu-id="944bb-331">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="944bb-331">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

<dl> <dt>

<span data-ttu-id="944bb-332"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="944bb-332"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1 (0x1))</span></span>
</dt> <dt>

<span data-ttu-id="944bb-333"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="944bb-333"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2 (0x2))</span></span>
</dt> <dt>

<span data-ttu-id="944bb-334"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="944bb-334"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3 (0x3))</span></span>
</dt> <dt>

<span data-ttu-id="944bb-335"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="944bb-335"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (4 (0x4))</span></span>
</dt> <dt>

<span data-ttu-id="944bb-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (5 (0x5))</span><span class="sxs-lookup"><span data-stu-id="944bb-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5 (0x5))</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="944bb-337">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="944bb-337">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-338">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="944bb-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-340">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="944bb-340">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="944bb-341">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="944bb-341">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944bb-342">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="944bb-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="944bb-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="944bb-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="944bb-344">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="944bb-344">Scoping system's name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="944bb-345">Requisiti</span><span class="sxs-lookup"><span data-stu-id="944bb-345">Requirements</span></span>



| <span data-ttu-id="944bb-346">Requisito</span><span class="sxs-lookup"><span data-stu-id="944bb-346">Requirement</span></span> | <span data-ttu-id="944bb-347">Valore</span><span class="sxs-lookup"><span data-stu-id="944bb-347">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="944bb-348">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="944bb-348">Minimum supported client</span></span><br/> | <span data-ttu-id="944bb-349">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="944bb-349">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="944bb-350">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="944bb-350">Minimum supported server</span></span><br/> | <span data-ttu-id="944bb-351">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="944bb-351">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="944bb-352">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="944bb-352">Namespace</span></span><br/>                | <span data-ttu-id="944bb-353">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="944bb-353">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="944bb-354">MOF</span><span class="sxs-lookup"><span data-stu-id="944bb-354">MOF</span></span><br/>                      | <dl> <span data-ttu-id="944bb-355"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-355"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="944bb-356">DLL</span><span class="sxs-lookup"><span data-stu-id="944bb-356">DLL</span></span><br/>                      | <dl> <span data-ttu-id="944bb-357"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="944bb-357"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="944bb-358">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="944bb-358">See also</span></span>

<dl> <dt>

[<span data-ttu-id="944bb-359">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="944bb-359">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="944bb-360">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="944bb-360">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

