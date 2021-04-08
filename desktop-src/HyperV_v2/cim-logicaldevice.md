---
description: Astrazione o emulazione di un'entità hardware che può essere o meno basata su hardware fisico.
ms.assetid: e31c82ed-2da2-4a18-a55e-16931d74f243
title: Classe CIM_LogicalDevice (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice
- CIM_LogicalDevice.SystemCreationClassName
- CIM_LogicalDevice.SystemName
- CIM_LogicalDevice.CreationClassName
- CIM_LogicalDevice.DeviceID
- CIM_LogicalDevice.PowerManagementSupported
- CIM_LogicalDevice.PowerManagementCapabilities
- CIM_LogicalDevice.Availability
- CIM_LogicalDevice.StatusInfo
- CIM_LogicalDevice.LastErrorCode
- CIM_LogicalDevice.ErrorDescription
- CIM_LogicalDevice.ErrorCleared
- CIM_LogicalDevice.OtherIdentifyingInfo
- CIM_LogicalDevice.PowerOnHours
- CIM_LogicalDevice.TotalPowerOnHours
- CIM_LogicalDevice.IdentifyingDescriptions
- CIM_LogicalDevice.AdditionalAvailability
- CIM_LogicalDevice.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 471b10f8d3c8640cfcc4277d0151bdd46d59db86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749655"
---
# <a name="cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="ed71b-103">Classe CIM_LogicalDevice (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="ed71b-103">CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="ed71b-104">Astrazione o emulazione di un'entità hardware che può essere o meno basata su hardware fisico.</span><span class="sxs-lookup"><span data-stu-id="ed71b-104">An abstraction or emulation of a hardware entity that may or may not be based on physical hardware.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed71b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed71b-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_LogicalDevice : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  DeviceID;
  boolean PowerManagementSupported;
  uint16  PowerManagementCapabilities[];
  uint16  Availability;
  uint16  StatusInfo;
  uint32  LastErrorCode;
  string  ErrorDescription;
  boolean ErrorCleared;
  string  OtherIdentifyingInfo[];
  uint64  PowerOnHours;
  uint64  TotalPowerOnHours;
  string  IdentifyingDescriptions[];
  uint16  AdditionalAvailability[];
  uint64  MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="ed71b-106">Members</span><span class="sxs-lookup"><span data-stu-id="ed71b-106">Members</span></span>

<span data-ttu-id="ed71b-107">La classe **CIM \_ LogicalDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ed71b-107">The **CIM\_LogicalDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="ed71b-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="ed71b-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="ed71b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ed71b-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ed71b-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="ed71b-110">Methods</span></span>

<span data-ttu-id="ed71b-111">La classe **CIM \_ LogicalDevice** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ed71b-111">The **CIM\_LogicalDevice** class has these methods.</span></span>



| <span data-ttu-id="ed71b-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="ed71b-112">Method</span></span>                                                           | <span data-ttu-id="ed71b-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed71b-113">Description</span></span>                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed71b-114">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="ed71b-114">**EnableDevice**</span></span>](cim-logicaldevice-enabledevice.md)           | <span data-ttu-id="ed71b-115">Questo metodo è deprecato.</span><span class="sxs-lookup"><span data-stu-id="ed71b-115">This method is deprecated.</span></span> <span data-ttu-id="ed71b-116">Usare invece il metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="ed71b-116">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="ed71b-117">**Descrizione deprecata:** Abilita o Disabilita il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ed71b-117">**Deprecated description:** Enables or disables the logical device.</span></span><br/>                                                                     |
| [<span data-ttu-id="ed71b-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="ed71b-118">**OnlineDevice**</span></span>](cim-logicaldevice-onlinedevice.md)           | <span data-ttu-id="ed71b-119">Questo metodo è deprecato.</span><span class="sxs-lookup"><span data-stu-id="ed71b-119">This method is deprecated.</span></span> <span data-ttu-id="ed71b-120">Usare invece il metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="ed71b-120">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="ed71b-121">**Descrizione deprecata:** Porta online il dispositivo logico, in modo che possa accettare le richieste oppure offline in modo che non possa più accettare richieste.</span><span class="sxs-lookup"><span data-stu-id="ed71b-121">**Deprecated description:** Brings the logical device online so it can accept requests, or offline so it can no longer accept requests.</span></span><br/> |
| [<span data-ttu-id="ed71b-122">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="ed71b-122">**QuiesceDevice**</span></span>](cim-logicaldevice-quiescedevice.md)         | <span data-ttu-id="ed71b-123">Questo metodo è deprecato.</span><span class="sxs-lookup"><span data-stu-id="ed71b-123">This method is deprecated.</span></span> <span data-ttu-id="ed71b-124">Usare invece il metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="ed71b-124">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="ed71b-125">**Descrizione deprecata:** Sospende temporaneamente l'attività sul dispositivo logico o Abilita nuovamente l'attività.</span><span class="sxs-lookup"><span data-stu-id="ed71b-125">**Deprecated description:** Temporarily suspends activity on the logical device, or re-enables the activity.</span></span><br/>                            |
| [<span data-ttu-id="ed71b-126">**Reset**</span><span class="sxs-lookup"><span data-stu-id="ed71b-126">**Reset**</span></span>](cim-logicaldevice-reset.md)                         | <span data-ttu-id="ed71b-127">Reimposta il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ed71b-127">Resets the logical device.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="ed71b-128">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="ed71b-128">**RestoreProperties**</span></span>](cim-logicaldevice-restoreproperties.md) | <span data-ttu-id="ed71b-129">Ripristina una configurazione precedente e lo stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ed71b-129">Restores a previous configuration and state of the logical device.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="ed71b-130">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="ed71b-130">**SaveProperties**</span></span>](cim-logicaldevice-saveproperties.md)       | <span data-ttu-id="ed71b-131">Salva la configurazione e lo stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ed71b-131">Saves the configuration and state of the logical device.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="ed71b-132">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ed71b-132">**SetPowerState**</span></span>](cim-logicaldevice-setpowerstate.md)         | <span data-ttu-id="ed71b-133">Questo metodo è deprecato.</span><span class="sxs-lookup"><span data-stu-id="ed71b-133">This method is deprecated.</span></span> <span data-ttu-id="ed71b-134">Usare invece la proprietà **SetPowerState** della classe **CIM \_ PowerManagementService** .</span><span class="sxs-lookup"><span data-stu-id="ed71b-134">Instead, use the **SetPowerState** property of the **CIM\_PowerManagementService** class.</span></span><br/> <span data-ttu-id="ed71b-135">**Descrizione deprecata:** Imposta lo stato di alimentazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ed71b-135">**Deprecated description:** Sets the power state of the logical device.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="ed71b-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ed71b-136">Properties</span></span>

<span data-ttu-id="ed71b-137">La classe **CIM \_ LogicalDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ed71b-137">The **CIM\_LogicalDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed71b-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="ed71b-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-139">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ed71b-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-141">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**Disponibilità**")</span><span class="sxs-lookup"><span data-stu-id="ed71b-141">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**Availability**")</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-142">Matrice che contiene le informazioni sulla disponibilità relative al dispositivo logico, oltre a quelle della proprietà di **disponibilità** .</span><span class="sxs-lookup"><span data-stu-id="ed71b-142">An array that contains availability information about of the logical device, in addition to the that of the **Availability** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ed71b-143">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ed71b-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ed71b-144">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="ed71b-144">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="ed71b-145">**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="ed71b-145">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="ed71b-146">**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="ed71b-146">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="ed71b-147">**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="ed71b-147">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ed71b-148">**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="ed71b-148">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ed71b-149">**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="ed71b-149">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="ed71b-150">**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="ed71b-150">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="ed71b-151">**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="ed71b-151">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ed71b-152">**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="ed71b-152">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="ed71b-153">**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="ed71b-153">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="ed71b-154">**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="ed71b-154">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="ed71b-155">**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="ed71b-155">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ed71b-156">**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="ed71b-156">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ed71b-157">**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="ed71b-157">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ed71b-158">**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="ed71b-158">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="ed71b-159">**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="ed71b-159">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ed71b-160">In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="ed71b-160">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="ed71b-161">**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="ed71b-161">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="ed71b-162">**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="ed71b-162">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="ed71b-163">**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="ed71b-163">**Quiesced** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ed71b-164">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="ed71b-164">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-165">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ed71b-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-167">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 006,5 "," MIB. IETF \| host-Resources-MIB. hrDeviceStatus "," MIF. DMTF \| Host Device \| 001,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**AdditionalAvailability**")</span><span class="sxs-lookup"><span data-stu-id="ed71b-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|006.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus", "MIF.DMTF\|Host Device\|001.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**AdditionalAvailability**")</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-168">Contiene la disponibilità del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ed71b-168">Contains the availability of the logical device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ed71b-169">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ed71b-169">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ed71b-170">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="ed71b-170">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="ed71b-171">**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="ed71b-171">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="ed71b-172">**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="ed71b-172">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="ed71b-173">**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="ed71b-173">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ed71b-174">**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="ed71b-174">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ed71b-175">**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="ed71b-175">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="ed71b-176">**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="ed71b-176">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="ed71b-177">**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="ed71b-177">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ed71b-178">**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="ed71b-178">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="ed71b-179">**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="ed71b-179">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="ed71b-180">**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="ed71b-180">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="ed71b-181">**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="ed71b-181">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ed71b-182">**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="ed71b-182">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ed71b-183">**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="ed71b-183">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ed71b-184">**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="ed71b-184">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="ed71b-185">**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="ed71b-185">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ed71b-186">In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="ed71b-186">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="ed71b-187">**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="ed71b-187">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="ed71b-188">**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="ed71b-188">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="ed71b-189">**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="ed71b-189">**Quiesced** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ed71b-190">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ed71b-190">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ed71b-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-193">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ed71b-193">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-194">Nome della classe utilizzato per creare un'istanza del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ed71b-194">The class name used to create an instance of the logical device.</span></span> <span data-ttu-id="ed71b-195">**CreationClassName** è combinato con altre proprietà chiave di questa classe per identificare in modo univoco le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="ed71b-195">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="ed71b-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ed71b-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ed71b-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-199">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ed71b-199">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-200">Identificatore univoco del dispositivo logico, ad esempio l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="ed71b-200">A unique identifier of the logical device, such as the address.</span></span>

</dd> <dt>

<span data-ttu-id="ed71b-201">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="ed71b-201">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-202">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ed71b-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-204">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span><span class="sxs-lookup"><span data-stu-id="ed71b-204">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-205">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ed71b-205">This property is deprecated.</span></span> <span data-ttu-id="ed71b-206">Usare invece la proprietà **OperationalStatus** della classe **CIM \_ ManagedSystemElement** .</span><span class="sxs-lookup"><span data-stu-id="ed71b-206">Instead, use the **OperationalStatus** property from the **CIM\_ManagedSystemElement** class.</span></span>

<span data-ttu-id="ed71b-207">**Descrizione deprecata:** Indica se un errore segnalato dalla proprietà **LastErrorCode** è deselezionato.</span><span class="sxs-lookup"><span data-stu-id="ed71b-207">**Deprecated description:** Indicates whether an error reported by the **LastErrorCode** property is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="ed71b-208">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ed71b-208">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-209">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ed71b-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-211">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ DeviceErrorData. ErrorDescription")</span><span class="sxs-lookup"><span data-stu-id="ed71b-211">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_DeviceErrorData.ErrorDescription")</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-212">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ed71b-212">This property is deprecated.</span></span> <span data-ttu-id="ed71b-213">Usare invece la proprietà **ErrorDescription** della classe **CIM \_ DeviceErrorData** .</span><span class="sxs-lookup"><span data-stu-id="ed71b-213">Instead, use the **ErrorDescription** property from the **CIM\_DeviceErrorData** class.</span></span>

<span data-ttu-id="ed71b-214">**Descrizione deprecata:** Informazioni aggiuntive sull'errore segnalato dalla proprietà **LastErrorCode** .</span><span class="sxs-lookup"><span data-stu-id="ed71b-214">**Deprecated description:** Additional information about the error reported by the **LastErrorCode** property.</span></span>

</dd> <dt>

<span data-ttu-id="ed71b-215">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ed71b-215">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-216">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ed71b-216">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-218">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**OtherIdentifyingInfo**")</span><span class="sxs-lookup"><span data-stu-id="ed71b-218">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**OtherIdentifyingInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-219">Matrice di stringhe che descrivono gli elementi della matrice **OtherIdentifyingInfo** dello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="ed71b-219">An array of strings that describe the **OtherIdentifyingInfo** array items of the same index.</span></span>

</dd> <dt>

<span data-ttu-id="ed71b-220">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ed71b-220">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-221">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed71b-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-223">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ DeviceErrorData. LastErrorCode")</span><span class="sxs-lookup"><span data-stu-id="ed71b-223">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_DeviceErrorData.LastErrorCode")</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-224">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ed71b-224">This property is deprecated.</span></span> <span data-ttu-id="ed71b-225">Viene invece usata la proprietà **LastErrorCode** della classe **CIM \_ DeviceErrorData** .</span><span class="sxs-lookup"><span data-stu-id="ed71b-225">Instead, we use the **LastErrorCode** property from the **CIM\_DeviceErrorData** class.</span></span>

<span data-ttu-id="ed71b-226">**Descrizione deprecata:** Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ed71b-226">**Deprecated description:** The last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="ed71b-227">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="ed71b-227">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-228">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ed71b-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-230">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi")</span><span class="sxs-lookup"><span data-stu-id="ed71b-230">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-231">Questa proprietà è deprecata e non deve essere usata.</span><span class="sxs-lookup"><span data-stu-id="ed71b-231">This property is deprecated and should not be used.</span></span>

<span data-ttu-id="ed71b-232">**Descrizione deprecata:** Tempo massimo, in millisecondi, per cui un dispositivo può rimanere in uno stato temporaneamente disabilitato (le proprietà **Availability** e **AdditionalAvailability** sono impostate su "21" riposo).</span><span class="sxs-lookup"><span data-stu-id="ed71b-232">**Deprecated description:** The maximum time in milliseconds, that a device can remain in a temporarily disabled state (**Availability** and **AdditionalAvailability** properties set to "21"   quiescent ).</span></span> <span data-ttu-id="ed71b-233">Il valore "0" indica che il dispositivo logico può rimanere in uno stato temporaneamente disabilitato per un periodo illimitato.</span><span class="sxs-lookup"><span data-stu-id="ed71b-233">A value of "0" indicates that the logical device can remain in a temporarily disabled state indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="ed71b-234">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ed71b-234">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-235">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ed71b-235">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-237">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**IdentifyingDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="ed71b-237">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**IdentifyingDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-238">Informazioni che identificano il dispositivo logico, diverso da **DeviceID**.</span><span class="sxs-lookup"><span data-stu-id="ed71b-238">Information that identifies the logical device, other than **DeviceID**.</span></span>

</dd> <dt>

<span data-ttu-id="ed71b-239">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ed71b-239">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-240">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ed71b-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-242">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities. PowerCapabilities")</span><span class="sxs-lookup"><span data-stu-id="ed71b-242">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities.PowerCapabilities")</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-243">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ed71b-243">This property is deprecated.</span></span> <span data-ttu-id="ed71b-244">Usare invece la classe **CIM \_ PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="ed71b-244">Instead, use the **CIM\_PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="ed71b-245">**Descrizione deprecata:** Matrice che contiene le funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed71b-245">**Deprecated description:** An array that contains the power management capabilities of the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ed71b-246">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ed71b-246">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="ed71b-247">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="ed71b-247">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ed71b-248">**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="ed71b-248">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ed71b-249">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="ed71b-249">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="ed71b-250">**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="ed71b-250">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="ed71b-251">**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="ed71b-251">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="ed71b-252">**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="ed71b-252">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="ed71b-253">**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="ed71b-253">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ed71b-254">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="ed71b-254">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-255">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ed71b-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-257">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities")</span><span class="sxs-lookup"><span data-stu-id="ed71b-257">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities")</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-258">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ed71b-258">This property is deprecated.</span></span> <span data-ttu-id="ed71b-259">Usare invece la classe **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="ed71b-259">Instead, use the **PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="ed71b-260">**Descrizione deprecata: true** se il dispositivo logico può essere gestito dall'alimentazione; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="ed71b-260">**Deprecated description:  true** if the logical device can be power managed; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="ed71b-261">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ed71b-261">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-262">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ed71b-262">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-264">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("ore"), **contatore**</span><span class="sxs-lookup"><span data-stu-id="ed71b-264">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hours"), **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-265">Il numero di ore consecutive in cui il dispositivo logico è stato alimentato, dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="ed71b-265">The number of consecutive hours the logical device has been powered, since its last power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="ed71b-266">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ed71b-266">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-267">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ed71b-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-269">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Stato operativo DMTF \| 006,4 ")</span><span class="sxs-lookup"><span data-stu-id="ed71b-269">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|006.4")</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-270">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ed71b-270">This property is deprecated.</span></span> <span data-ttu-id="ed71b-271">Usare invece la classe **CIM \_ PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="ed71b-271">Instead, use the **CIM\_PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="ed71b-272">**Descrizione deprecata:** Indica se il dispositivo logico è abilitato o in uno stato correlato.</span><span class="sxs-lookup"><span data-stu-id="ed71b-272">**Deprecated description:** Indicates whether the logical device is enabled or in a related state.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ed71b-273">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ed71b-273">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ed71b-274">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="ed71b-274">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ed71b-275">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="ed71b-275">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ed71b-276">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="ed71b-276">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ed71b-277">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="ed71b-277">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ed71b-278">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ed71b-278">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-279">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ed71b-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-281">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="ed71b-281">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-282">Nome della classe utilizzato per creare un'istanza del sistema che contiene il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ed71b-282">The class name used to create an instance of the system that contains the logical device.</span></span> <span data-ttu-id="ed71b-283">**SystemCreationClassName** è combinato con altre proprietà chiave di questa classe per identificare in modo univoco le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="ed71b-283">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="ed71b-284">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ed71b-284">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-285">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ed71b-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-287">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="ed71b-287">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-288">Nome del sistema che contiene il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ed71b-288">The name of the system that contains the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="ed71b-289">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ed71b-289">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed71b-290">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ed71b-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed71b-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed71b-292">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("ore"), **contatore**</span><span class="sxs-lookup"><span data-stu-id="ed71b-292">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hours"), **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="ed71b-293">Il numero totale di ore in cui il dispositivo logico è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="ed71b-293">The total number of hours the logical device has been powered.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed71b-294">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed71b-294">Requirements</span></span>



| <span data-ttu-id="ed71b-295">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed71b-295">Requirement</span></span> | <span data-ttu-id="ed71b-296">Valore</span><span class="sxs-lookup"><span data-stu-id="ed71b-296">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed71b-297">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed71b-297">Minimum supported client</span></span><br/> | <span data-ttu-id="ed71b-298">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ed71b-298">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ed71b-299">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed71b-299">Minimum supported server</span></span><br/> | <span data-ttu-id="ed71b-300">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ed71b-300">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ed71b-301">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ed71b-301">Namespace</span></span><br/>                | <span data-ttu-id="ed71b-302">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ed71b-302">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ed71b-303">MOF</span><span class="sxs-lookup"><span data-stu-id="ed71b-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed71b-304"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed71b-304"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed71b-305">DLL</span><span class="sxs-lookup"><span data-stu-id="ed71b-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed71b-306"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ed71b-306"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ed71b-307">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed71b-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed71b-308">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="ed71b-308">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

