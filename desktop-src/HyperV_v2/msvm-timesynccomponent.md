---
description: Rappresenta lo stato del servizio di sincronizzazione dell'ora, che è responsabile della sincronizzazione dell'ora di sistema di una macchina virtuale con l'ora di sistema del sistema operativo in esecuzione nel sistema operativo di gestione.
ms.assetid: 551A81E9-E924-4A9C-965D-02FF25EE4A49
title: Classe Msvm_TimeSyncComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TimeSyncComponent
- Msvm_TimeSyncComponent.SetPowerState
- Msvm_TimeSyncComponent.EnableDevice
- Msvm_TimeSyncComponent.OnlineDevice
- Msvm_TimeSyncComponent.QuiesceDevice
- Msvm_TimeSyncComponent.SaveProperties
- Msvm_TimeSyncComponent.RestoreProperties
- Msvm_TimeSyncComponent.InstanceID
- Msvm_TimeSyncComponent.Caption
- Msvm_TimeSyncComponent.Description
- Msvm_TimeSyncComponent.ElementName
- Msvm_TimeSyncComponent.InstallDate
- Msvm_TimeSyncComponent.Name
- Msvm_TimeSyncComponent.OperationalStatus
- Msvm_TimeSyncComponent.StatusDescriptions
- Msvm_TimeSyncComponent.Status
- Msvm_TimeSyncComponent.HealthState
- Msvm_TimeSyncComponent.CommunicationStatus
- Msvm_TimeSyncComponent.DetailedStatus
- Msvm_TimeSyncComponent.OperatingStatus
- Msvm_TimeSyncComponent.PrimaryStatus
- Msvm_TimeSyncComponent.EnabledState
- Msvm_TimeSyncComponent.OtherEnabledState
- Msvm_TimeSyncComponent.RequestedState
- Msvm_TimeSyncComponent.EnabledDefault
- Msvm_TimeSyncComponent.TimeOfLastStateChange
- Msvm_TimeSyncComponent.AvailableRequestedStates
- Msvm_TimeSyncComponent.TransitioningToState
- Msvm_TimeSyncComponent.SystemCreationClassName
- Msvm_TimeSyncComponent.SystemName
- Msvm_TimeSyncComponent.CreationClassName
- Msvm_TimeSyncComponent.DeviceID
- Msvm_TimeSyncComponent.PowerManagementSupported
- Msvm_TimeSyncComponent.PowerManagementCapabilities
- Msvm_TimeSyncComponent.Availability
- Msvm_TimeSyncComponent.StatusInfo
- Msvm_TimeSyncComponent.LastErrorCode
- Msvm_TimeSyncComponent.ErrorDescription
- Msvm_TimeSyncComponent.ErrorCleared
- Msvm_TimeSyncComponent.OtherIdentifyingInfo
- Msvm_TimeSyncComponent.PowerOnHours
- Msvm_TimeSyncComponent.TotalPowerOnHours
- Msvm_TimeSyncComponent.IdentifyingDescriptions
- Msvm_TimeSyncComponent.AdditionalAvailability
- Msvm_TimeSyncComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ea9a33d665a315861d9e6c51fd529f10f07b4aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308733"
---
# <a name="msvm_timesynccomponent-class"></a><span data-ttu-id="f4e5c-103">\_Classe MSVM TimeSyncComponent</span><span class="sxs-lookup"><span data-stu-id="f4e5c-103">Msvm\_TimeSyncComponent class</span></span>

<span data-ttu-id="f4e5c-104">Rappresenta lo stato del servizio di sincronizzazione dell'ora, che è responsabile della sincronizzazione dell'ora di sistema di una macchina virtuale con l'ora di sistema del sistema operativo in esecuzione nel sistema operativo di gestione.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-104">Represents the state of the time synchronization service, which is responsible for synchronizing the system time of a virtual machine with the system time of the operating system running in the management operating system.</span></span>

<span data-ttu-id="f4e5c-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4e5c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4e5c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TimeSyncComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Time Synchronization";
  string   Description = "Microsoft Time Synchronization Service";
  string   ElementName = "Time Synchronization";
  datetime InstallDate;
  string   Name = "Time Synchronization";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = {"OK"};
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_TimeSyncComponent";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="f4e5c-107">Members</span><span class="sxs-lookup"><span data-stu-id="f4e5c-107">Members</span></span>

<span data-ttu-id="f4e5c-108">La **classe \_ TimeSyncComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f4e5c-108">The **Msvm\_TimeSyncComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="f4e5c-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="f4e5c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="f4e5c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f4e5c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f4e5c-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="f4e5c-111">Methods</span></span>

<span data-ttu-id="f4e5c-112">La **classe \_ TimeSyncComponent di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-112">The **Msvm\_TimeSyncComponent** class has these methods.</span></span>



| <span data-ttu-id="f4e5c-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="f4e5c-113">Method</span></span>                                                                  | <span data-ttu-id="f4e5c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4e5c-114">Description</span></span>                              |
|:------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="f4e5c-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-115">**EnableDevice**</span></span>                                                        | <span data-ttu-id="f4e5c-116">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f4e5c-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-117">**OnlineDevice**</span></span>                                                        | <span data-ttu-id="f4e5c-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f4e5c-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-119">**QuiesceDevice**</span></span>                                                       | <span data-ttu-id="f4e5c-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="f4e5c-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-121">**RequestStateChange**</span></span>](msvm-timesynccomponent-requeststatechange.md) | <span data-ttu-id="f4e5c-122">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="f4e5c-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-123">**Reset**</span></span>](msvm-timesynccomponent-reset.md)                           | <span data-ttu-id="f4e5c-124">Reimposta il componente.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-124">Resets the component.</span></span><br/>         |
| <span data-ttu-id="f4e5c-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-125">**RestoreProperties**</span></span>                                                   | <span data-ttu-id="f4e5c-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f4e5c-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-127">**SaveProperties**</span></span>                                                      | <span data-ttu-id="f4e5c-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f4e5c-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-129">**SetPowerState**</span></span>                                                       | <span data-ttu-id="f4e5c-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f4e5c-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f4e5c-131">Properties</span></span>

<span data-ttu-id="f4e5c-132">La **classe \_ TimeSyncComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-132">The **Msvm\_TimeSyncComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4e5c-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-134">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-136">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="f4e5c-137">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su 6 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-138">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-139">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-141">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-141">The primary availability and status of the device.</span></span> <span data-ttu-id="f4e5c-142">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="f4e5c-143">Valore</span><span class="sxs-lookup"><span data-stu-id="f4e5c-143">Value</span></span>                                                                        | <span data-ttu-id="f4e5c-144">Significato</span><span class="sxs-lookup"><span data-stu-id="f4e5c-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f4e5c-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f4e5c-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="f4e5c-146">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="f4e5c-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f4e5c-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-148">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-150">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="f4e5c-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="f4e5c-151">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-152">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-155">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-155">A short description of the object.</span></span> <span data-ttu-id="f4e5c-156">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-158">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-160">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="f4e5c-161">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f4e5c-162">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f4e5c-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f4e5c-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f4e5c-170">)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f4e5c-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-174">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-174">The scoping system's creation class name.</span></span> <span data-ttu-id="f4e5c-175">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-176">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-179">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="f4e5c-179">A description of the object.</span></span> <span data-ttu-id="f4e5c-180">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-182">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-184">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="f4e5c-185">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f4e5c-186">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f4e5c-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f4e5c-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f4e5c-195">)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f4e5c-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-199">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="f4e5c-200">Questa proprietà viene ereditata [**da CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Microsoft:*VMGUID* \\ *GUID*", dove *VMGUID* è la proprietà **Name** dell'istanza [**MSVM \_ ComputerSystem**](msvm-computersystem.md) associata a questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) instance associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-204">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-204">A display name for the object.</span></span> <span data-ttu-id="f4e5c-205">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-206">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-207">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-209">Configurazione predefinita o di avvio di un amministratore per la **EnabledState** di un elemento.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-209">An administrator's default or startup configuration for the **EnabledState** of an element.</span></span> <span data-ttu-id="f4e5c-210">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-210">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="f4e5c-211">Valore</span><span class="sxs-lookup"><span data-stu-id="f4e5c-211">Value</span></span>                                                                        | <span data-ttu-id="f4e5c-212">Significato</span><span class="sxs-lookup"><span data-stu-id="f4e5c-212">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="f4e5c-213"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="f4e5c-213"><dt>7</dt></span></span> </dl> | <span data-ttu-id="f4e5c-214">Nessun valore predefinito</span><span class="sxs-lookup"><span data-stu-id="f4e5c-214">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f4e5c-215">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-215">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-216">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-218">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-218">The enabled and disabled states of an element.</span></span> <span data-ttu-id="f4e5c-219">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e viene impostata su 2 (Enabled) o 3 (disabilitato).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-219">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is either set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="f4e5c-220">Valore</span><span class="sxs-lookup"><span data-stu-id="f4e5c-220">Value</span></span>                                                                        | <span data-ttu-id="f4e5c-221">Significato</span><span class="sxs-lookup"><span data-stu-id="f4e5c-221">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="f4e5c-222"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f4e5c-222"><dt>2</dt></span></span> </dl> | <span data-ttu-id="f4e5c-223">Abilitato</span><span class="sxs-lookup"><span data-stu-id="f4e5c-223">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="f4e5c-224"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f4e5c-224"><dt>3</dt></span></span> </dl> | <span data-ttu-id="f4e5c-225">Disabled</span><span class="sxs-lookup"><span data-stu-id="f4e5c-225">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f4e5c-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-227">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-229">Indica se l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-229">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="f4e5c-230">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-232">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-234">Stringa che fornisce ulteriori informazioni sull'errore registrato nella proprietà **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-234">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="f4e5c-235">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-236">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-236">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-237">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-239">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-239">The current health of the element.</span></span> <span data-ttu-id="f4e5c-240">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="f4e5c-241">Valore</span><span class="sxs-lookup"><span data-stu-id="f4e5c-241">Value</span></span>                                                                        | <span data-ttu-id="f4e5c-242">Significato</span><span class="sxs-lookup"><span data-stu-id="f4e5c-242">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="f4e5c-243"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f4e5c-243"><dt>5</dt></span></span> </dl> | <span data-ttu-id="f4e5c-244">OK</span><span class="sxs-lookup"><span data-stu-id="f4e5c-244">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f4e5c-245">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-245">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-246">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-246">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-248">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="f4e5c-248">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="f4e5c-249">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-249">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-250">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-250">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-251">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-251">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-253">Data e ora in cui il servizio di integrazione è stato installato nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-253">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="f4e5c-254">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-255">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-255">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-256">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-258">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-258">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-259">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-259">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f4e5c-260">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-261">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-261">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-262">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-264">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-264">The last error code reported by the logical device.</span></span> <span data-ttu-id="f4e5c-265">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-266">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-266">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-267">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-269">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-269">This property has been deprecated.</span></span> <span data-ttu-id="f4e5c-270">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-270">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-271">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-271">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-272">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-273">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-274">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-274">The label by which the object is known.</span></span> <span data-ttu-id="f4e5c-275">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-275">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-276">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-276">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-277">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-277">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-279">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="f4e5c-279">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="f4e5c-280">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-280">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f4e5c-281">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f4e5c-282"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-282"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-283"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-283"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-284"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-284"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-285"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-285"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-286"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-286"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-287"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-287"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-288"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-288"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-289"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-289"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-290"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-290"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-291"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-291"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-292"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-292"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-293"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-293"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-294"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-294"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-295"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-295"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-296"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-296"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-297"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-297"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-298"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-298"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f4e5c-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f4e5c-301">)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-301">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f4e5c-302">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-302">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-303">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-303">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-305">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-305">The current status of the element.</span></span> <span data-ttu-id="f4e5c-306">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-306">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="f4e5c-307">Di seguito sono riportati i valori possibili per il valore della proprietà **OperationalStatus** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="f4e5c-307">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="f4e5c-308">Valore</span><span class="sxs-lookup"><span data-stu-id="f4e5c-308">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="f4e5c-309">Significato</span><span class="sxs-lookup"><span data-stu-id="f4e5c-309">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f4e5c-310"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f4e5c-310"><dt>{ 2 }</dt></span></span> </dl>                                                                                                                                                                                                    |                                                                                                                                                                                                                                          |
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="f4e5c-311"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f4e5c-311"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="f4e5c-312">Il servizio funziona normalmente.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-312">The service is operating normally.</span></span> <span data-ttu-id="f4e5c-313">I  \[ valori delle \] proprietà OperationalStatus 1 e **StatusDescriptions** \[ 1 \] possono contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-313">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="f4e5c-314"><dt></dt> Ridotto <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f4e5c-314"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="f4e5c-315">Il servizio funziona normalmente, ma il servizio Guest ha negoziato una versione del protocollo di comunicazione compatibile.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-315">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="f4e5c-316">I  \[ valori delle \] proprietà OperationalStatus 1 e **StatusDescriptions** \[ 1 \] possono contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-316">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="f4e5c-317"><dt>**Errore irreversibile**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="f4e5c-317"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="f4e5c-318">Il Guest non supporta una versione del protocollo compatibile.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-318">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="f4e5c-319">I  \[ valori delle \] proprietà OperationalStatus 1 e **StatusDescriptions** \[ 1 \] possono contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-319">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="f4e5c-320"><dt>**Nessun contatto**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="f4e5c-320"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="f4e5c-321">Il servizio Guest non è installato o non è stato ancora contattato.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-321">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="f4e5c-322"><dt>**Perdita di comunicazione**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="f4e5c-322"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="f4e5c-323">Il servizio Guest non risponde più normalmente.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-323">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="f4e5c-324">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-324">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-325">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-327">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-327">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="f4e5c-328">Questa proprietà deve essere impostata su **null** se la proprietà **EnabledState** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-328">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="f4e5c-329">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-330">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-330">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-331">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-331">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-333">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-333">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="f4e5c-334">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-334">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-335">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-335">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-336">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-336">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-338">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-338">The power management capabilities of the device.</span></span> <span data-ttu-id="f4e5c-339">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-339">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-340">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-340">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-341">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-341">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-343">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-343">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="f4e5c-344">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-345">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-345">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-346">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-346">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-348">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-348">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="f4e5c-349">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-350">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-350">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-351">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-353">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-353">Provides high level status information.</span></span> <span data-ttu-id="f4e5c-354">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-354">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="f4e5c-355">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-355">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f4e5c-356">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f4e5c-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-358"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-358"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-359"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-359"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-360"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-360"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-361"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-361"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-362"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f4e5c-362"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f4e5c-363">)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-363">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f4e5c-364">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-364">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-365">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-365">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-366">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-367">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-367">The last requested or desired state for the element.</span></span> <span data-ttu-id="f4e5c-368">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-368">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="f4e5c-369">Valore</span><span class="sxs-lookup"><span data-stu-id="f4e5c-369">Value</span></span>                                                                         | <span data-ttu-id="f4e5c-370">Significato</span><span class="sxs-lookup"><span data-stu-id="f4e5c-370">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f4e5c-371"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="f4e5c-371"><dt>12</dt></span></span> </dl> | <span data-ttu-id="f4e5c-372">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="f4e5c-372">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f4e5c-373">**Status**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-373">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-374">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-376">Stringa che specifica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-376">A string that specifies the current status of the object.</span></span> <span data-ttu-id="f4e5c-377">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-378">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-378">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-379">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-381">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="f4e5c-381">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="f4e5c-382">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-384">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-385">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-386">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-386">The current state of the logical device.</span></span> <span data-ttu-id="f4e5c-387">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-387">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-388">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-388">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-389">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-391">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-391">The creation class name of the scoping system.</span></span> <span data-ttu-id="f4e5c-392">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-393">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-393">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-394">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-395">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-396">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-396">The name of the scoping system.</span></span> <span data-ttu-id="f4e5c-397">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-398">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-398">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-399">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-399">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-401">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-401">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="f4e5c-402">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-402">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-403">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-403">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-404">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-404">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-405">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-406">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-406">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="f4e5c-407">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f4e5c-408">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-408">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e5c-409">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4e5c-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e5c-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4e5c-411">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-411">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="f4e5c-412">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="f4e5c-413">Valore</span><span class="sxs-lookup"><span data-stu-id="f4e5c-413">Value</span></span>                                                                         | <span data-ttu-id="f4e5c-414">Significato</span><span class="sxs-lookup"><span data-stu-id="f4e5c-414">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f4e5c-415"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="f4e5c-415"><dt>12</dt></span></span> </dl> | <span data-ttu-id="f4e5c-416">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="f4e5c-416">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4e5c-417">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4e5c-417">Remarks</span></span>

<span data-ttu-id="f4e5c-418">L'accesso alla **classe \_ TimeSyncComponent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-418">Access to the **Msvm\_TimeSyncComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f4e5c-419">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f4e5c-419">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4e5c-420">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4e5c-420">Requirements</span></span>



| <span data-ttu-id="f4e5c-421">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4e5c-421">Requirement</span></span> | <span data-ttu-id="f4e5c-422">Valore</span><span class="sxs-lookup"><span data-stu-id="f4e5c-422">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4e5c-423">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4e5c-423">Minimum supported client</span></span><br/> | <span data-ttu-id="f4e5c-424">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f4e5c-424">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f4e5c-425">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4e5c-425">Minimum supported server</span></span><br/> | <span data-ttu-id="f4e5c-426">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f4e5c-426">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f4e5c-427">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f4e5c-427">Namespace</span></span><br/>                | <span data-ttu-id="f4e5c-428">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f4e5c-428">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f4e5c-429">MOF</span><span class="sxs-lookup"><span data-stu-id="f4e5c-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4e5c-430"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4e5c-430"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4e5c-431">DLL</span><span class="sxs-lookup"><span data-stu-id="f4e5c-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4e5c-432"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f4e5c-432"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f4e5c-433">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4e5c-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4e5c-434">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-434">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="f4e5c-435">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-435">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

