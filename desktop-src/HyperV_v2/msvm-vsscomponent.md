---
description: Rappresenta lo stato del servizio di Servizio Copia Shadow del volume (VSS), che implementa il richiedente del servizio Copia Shadow del volume nel sistema operativo guest.
ms.assetid: 4DD38929-1E3F-4105-BC1A-B367516F7B6E
title: Classe Msvm_VssComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponent
- Msvm_VssComponent.SetPowerState
- Msvm_VssComponent.EnableDevice
- Msvm_VssComponent.OnlineDevice
- Msvm_VssComponent.QuiesceDevice
- Msvm_VssComponent.SaveProperties
- Msvm_VssComponent.RestoreProperties
- Msvm_VssComponent.InstanceID
- Msvm_VssComponent.Caption
- Msvm_VssComponent.Description
- Msvm_VssComponent.ElementName
- Msvm_VssComponent.InstallDate
- Msvm_VssComponent.Name
- Msvm_VssComponent.OperationalStatus
- Msvm_VssComponent.StatusDescriptions
- Msvm_VssComponent.Status
- Msvm_VssComponent.HealthState
- Msvm_VssComponent.CommunicationStatus
- Msvm_VssComponent.DetailedStatus
- Msvm_VssComponent.OperatingStatus
- Msvm_VssComponent.PrimaryStatus
- Msvm_VssComponent.EnabledState
- Msvm_VssComponent.OtherEnabledState
- Msvm_VssComponent.RequestedState
- Msvm_VssComponent.EnabledDefault
- Msvm_VssComponent.TimeOfLastStateChange
- Msvm_VssComponent.AvailableRequestedStates
- Msvm_VssComponent.TransitioningToState
- Msvm_VssComponent.SystemCreationClassName
- Msvm_VssComponent.SystemName
- Msvm_VssComponent.CreationClassName
- Msvm_VssComponent.DeviceID
- Msvm_VssComponent.PowerManagementSupported
- Msvm_VssComponent.PowerManagementCapabilities
- Msvm_VssComponent.Availability
- Msvm_VssComponent.StatusInfo
- Msvm_VssComponent.LastErrorCode
- Msvm_VssComponent.ErrorDescription
- Msvm_VssComponent.ErrorCleared
- Msvm_VssComponent.OtherIdentifyingInfo
- Msvm_VssComponent.PowerOnHours
- Msvm_VssComponent.TotalPowerOnHours
- Msvm_VssComponent.IdentifyingDescriptions
- Msvm_VssComponent.AdditionalAvailability
- Msvm_VssComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab4039ce110af9fa023a662c31d1f9962b080e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305972"
---
# <a name="msvm_vsscomponent-class"></a><span data-ttu-id="a1030-103">\_Classe MSVM VssComponent</span><span class="sxs-lookup"><span data-stu-id="a1030-103">Msvm\_VssComponent class</span></span>

<span data-ttu-id="a1030-104">Rappresenta lo stato del servizio di Servizio Copia Shadow del volume (VSS), che implementa il richiedente del servizio Copia Shadow del volume nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="a1030-104">Represents the state of the Volume Shadow Copy Service (VSS) service, which implements the VSS Requester in the guest operating system.</span></span>

<span data-ttu-id="a1030-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a1030-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1030-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1030-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "VSS";
  string   Description = "Microsoft VSS Service";
  string   ElementName = "VSS";
  datetime InstallDate;
  string   Name = "VSS";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
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
  string   CreationClassName = "Msvm_VssComponent";
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

## <a name="members"></a><span data-ttu-id="a1030-107">Members</span><span class="sxs-lookup"><span data-stu-id="a1030-107">Members</span></span>

<span data-ttu-id="a1030-108">La **classe \_ VssComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a1030-108">The **Msvm\_VssComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="a1030-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="a1030-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="a1030-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a1030-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a1030-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="a1030-111">Methods</span></span>

<span data-ttu-id="a1030-112">La **classe \_ VssComponent di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a1030-112">The **Msvm\_VssComponent** class has these methods.</span></span>



| <span data-ttu-id="a1030-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="a1030-113">Method</span></span>                                                             | <span data-ttu-id="a1030-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1030-114">Description</span></span>                              |
|:-------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="a1030-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="a1030-115">**EnableDevice**</span></span>                                                   | <span data-ttu-id="a1030-116">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a1030-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a1030-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="a1030-117">**OnlineDevice**</span></span>                                                   | <span data-ttu-id="a1030-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a1030-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a1030-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="a1030-119">**QuiesceDevice**</span></span>                                                  | <span data-ttu-id="a1030-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a1030-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="a1030-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="a1030-121">**RequestStateChange**</span></span>](msvm-vsscomponent-requeststatechange.md) | <span data-ttu-id="a1030-122">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="a1030-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="a1030-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="a1030-123">**Reset**</span></span>](msvm-vsscomponent-reset.md)                           | <span data-ttu-id="a1030-124">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="a1030-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="a1030-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="a1030-125">**RestoreProperties**</span></span>                                              | <span data-ttu-id="a1030-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a1030-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a1030-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="a1030-127">**SaveProperties**</span></span>                                                 | <span data-ttu-id="a1030-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a1030-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a1030-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a1030-129">**SetPowerState**</span></span>                                                  | <span data-ttu-id="a1030-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a1030-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a1030-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a1030-131">Properties</span></span>

<span data-ttu-id="a1030-132">La **classe \_ VssComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a1030-132">The **Msvm\_VssComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1030-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="a1030-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-134">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1030-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a1030-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-136">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1030-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="a1030-137">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a1030-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a1030-138">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="a1030-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-139">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1030-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-141">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1030-141">The primary availability and status of the device.</span></span> <span data-ttu-id="a1030-142">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a1030-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="a1030-143">Valore</span><span class="sxs-lookup"><span data-stu-id="a1030-143">Value</span></span>                                                                        | <span data-ttu-id="a1030-144">Significato</span><span class="sxs-lookup"><span data-stu-id="a1030-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a1030-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="a1030-146">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a1030-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a1030-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="a1030-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-148">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1030-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a1030-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-150">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="a1030-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="a1030-151">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="a1030-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a1030-152">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a1030-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1030-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-155">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a1030-155">A short description of the object.</span></span> <span data-ttu-id="a1030-156">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a1030-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1030-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="a1030-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-158">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1030-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-160">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="a1030-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a1030-161">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="a1030-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a1030-162">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a1030-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a1030-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a1030-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="a1030-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="a1030-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="a1030-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="a1030-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="a1030-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a1030-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a1030-170">)</span><span class="sxs-lookup"><span data-stu-id="a1030-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a1030-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a1030-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1030-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-174">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="a1030-174">The scoping system's creation class name.</span></span> <span data-ttu-id="a1030-175">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a1030-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a1030-176">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a1030-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1030-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-179">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="a1030-179">A description of the object.</span></span> <span data-ttu-id="a1030-180">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a1030-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1030-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a1030-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-182">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1030-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-184">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="a1030-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a1030-185">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="a1030-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a1030-186">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a1030-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a1030-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="a1030-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="a1030-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="a1030-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="a1030-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="a1030-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="a1030-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="a1030-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a1030-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a1030-195">)</span><span class="sxs-lookup"><span data-stu-id="a1030-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a1030-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a1030-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1030-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-199">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a1030-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="a1030-200">Questa proprietà viene ereditata [**da CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Microsoft:*VMGUID* \\ *GUID*", dove *VMGUID* è la proprietà **Name** del [**MSVM \_ ComputerSystem**](msvm-computersystem.md) associato a questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1030-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="a1030-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a1030-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1030-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-204">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a1030-204">A display name for the object.</span></span> <span data-ttu-id="a1030-205">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a1030-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1030-206">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="a1030-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-207">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1030-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-209">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 7 (nessuna impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="a1030-209">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 7 (No Default).</span></span>



| <span data-ttu-id="a1030-210">Valore</span><span class="sxs-lookup"><span data-stu-id="a1030-210">Value</span></span>                                                                        | <span data-ttu-id="a1030-211">Significato</span><span class="sxs-lookup"><span data-stu-id="a1030-211">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="a1030-212"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-212"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a1030-213">Abilitato</span><span class="sxs-lookup"><span data-stu-id="a1030-213">Enabled</span></span><br/>    |
| <dl> <span data-ttu-id="a1030-214"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-214"><dt>3</dt></span></span> </dl> | <span data-ttu-id="a1030-215">Disabled</span><span class="sxs-lookup"><span data-stu-id="a1030-215">Disabled</span></span><br/>   |
| <dl> <span data-ttu-id="a1030-216"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-216"><dt>7</dt></span></span> </dl> | <span data-ttu-id="a1030-217">Nessun valore predefinito</span><span class="sxs-lookup"><span data-stu-id="a1030-217">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a1030-218">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a1030-218">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-219">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1030-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-221">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="a1030-221">The enabled and disabled states of an element.</span></span> <span data-ttu-id="a1030-222">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a1030-222">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="a1030-223">Valore</span><span class="sxs-lookup"><span data-stu-id="a1030-223">Value</span></span>                                                                        | <span data-ttu-id="a1030-224">Significato</span><span class="sxs-lookup"><span data-stu-id="a1030-224">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="a1030-225"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-225"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a1030-226">Abilitato</span><span class="sxs-lookup"><span data-stu-id="a1030-226">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="a1030-227"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-227"><dt>3</dt></span></span> </dl> | <span data-ttu-id="a1030-228">Disabled</span><span class="sxs-lookup"><span data-stu-id="a1030-228">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a1030-229">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a1030-229">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-230">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a1030-230">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-232">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="a1030-232">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="a1030-233">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="a1030-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a1030-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a1030-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-235">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1030-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-237">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="a1030-237">A string that provides more information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span> <span data-ttu-id="a1030-238">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="a1030-238">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a1030-239">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a1030-239">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-240">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1030-240">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-242">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a1030-242">The current health of the element.</span></span> <span data-ttu-id="a1030-243">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="a1030-243">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="a1030-244">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="a1030-244">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="a1030-245">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a1030-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="a1030-246">Valore</span><span class="sxs-lookup"><span data-stu-id="a1030-246">Value</span></span>                                                                        | <span data-ttu-id="a1030-247">Significato</span><span class="sxs-lookup"><span data-stu-id="a1030-247">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="a1030-248"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-248"><dt>5</dt></span></span> </dl> | <span data-ttu-id="a1030-249">OK</span><span class="sxs-lookup"><span data-stu-id="a1030-249">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a1030-250">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a1030-250">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-251">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="a1030-251">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1030-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-253">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="a1030-253">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="a1030-254">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="a1030-254">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a1030-255">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a1030-255">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-256">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a1030-256">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-258">Data e ora in cui il servizio di integrazione è stato installato nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a1030-258">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="a1030-259">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a1030-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1030-260">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a1030-260">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1030-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1030-263">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="a1030-263">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a1030-264">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="a1030-264">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a1030-265">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a1030-265">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1030-266">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a1030-266">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-267">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a1030-267">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-269">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a1030-269">The last error code reported by the logical device.</span></span> <span data-ttu-id="a1030-270">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="a1030-270">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a1030-271">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="a1030-271">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-272">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a1030-272">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-273">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-274">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="a1030-274">This property has been deprecated.</span></span> <span data-ttu-id="a1030-275">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a1030-275">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a1030-276">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a1030-276">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-277">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1030-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-279">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="a1030-279">The label by which the object is known.</span></span> <span data-ttu-id="a1030-280">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a1030-280">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1030-281">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="a1030-281">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-282">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1030-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-284">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="a1030-284">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a1030-285">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="a1030-285">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a1030-286">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a1030-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a1030-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a1030-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-288"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="a1030-288"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-289"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="a1030-289"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-290"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="a1030-290"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-291"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="a1030-291"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-292"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="a1030-292"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-293"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="a1030-293"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-294"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="a1030-294"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-295"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="a1030-295"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-296"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="a1030-296"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-297"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="a1030-297"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-298"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="a1030-298"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-299"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="a1030-299"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-300"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="a1030-300"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-301"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="a1030-301"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-302"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="a1030-302"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-303"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="a1030-303"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-304"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="a1030-304"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-305"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a1030-305"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a1030-306">)</span><span class="sxs-lookup"><span data-stu-id="a1030-306">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a1030-307">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a1030-307">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-308">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1030-308">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a1030-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-310">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a1030-310">The current status of the element.</span></span> <span data-ttu-id="a1030-311">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a1030-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="a1030-312">Di seguito sono riportati i valori possibili per il valore della proprietà **OperationalStatus** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="a1030-312">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="a1030-313">Valore</span><span class="sxs-lookup"><span data-stu-id="a1030-313">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="a1030-314">Significato</span><span class="sxs-lookup"><span data-stu-id="a1030-314">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a1030-315"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-315"><dt>{ 2 }</dt></span></span> </dl>                                                                                                                                                                                                    |                                                                                                                                                                                                                                          |
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="a1030-316"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-316"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="a1030-317">Il servizio funziona normalmente.</span><span class="sxs-lookup"><span data-stu-id="a1030-317">The service is operating normally.</span></span> <span data-ttu-id="a1030-318">I  \[ valori delle \] proprietà OperationalStatus 1 e **StatusDescriptions** \[ 1 \] possono contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="a1030-318">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="a1030-319"><dt></dt> Ridotto <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-319"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="a1030-320">Il servizio funziona normalmente, ma il servizio Guest ha negoziato una versione del protocollo di comunicazione compatibile.</span><span class="sxs-lookup"><span data-stu-id="a1030-320">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="a1030-321">I  \[ valori delle \] proprietà OperationalStatus 1 e **StatusDescriptions** \[ 1 \] possono contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="a1030-321">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="a1030-322"><dt>**Errore irreversibile**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-322"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="a1030-323">Il Guest non supporta una versione del protocollo compatibile.</span><span class="sxs-lookup"><span data-stu-id="a1030-323">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="a1030-324">I  \[ valori delle \] proprietà OperationalStatus 1 e **StatusDescriptions** \[ 1 \] possono contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="a1030-324">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="a1030-325"><dt>**Nessun contatto**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-325"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="a1030-326">Il servizio Guest non è installato o non è stato ancora contattato.</span><span class="sxs-lookup"><span data-stu-id="a1030-326">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="a1030-327"><dt>**Perdita di comunicazione**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-327"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="a1030-328">Il servizio Guest non risponde più normalmente.</span><span class="sxs-lookup"><span data-stu-id="a1030-328">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="a1030-329">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="a1030-329">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-330">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1030-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-332">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="a1030-332">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="a1030-333">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="a1030-333">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="a1030-334">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a1030-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a1030-335">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="a1030-335">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-336">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="a1030-336">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1030-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-338">Dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a1030-338">Additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="a1030-339">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="a1030-339">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a1030-340">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a1030-340">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-341">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1030-341">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a1030-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-343">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1030-343">The power management capabilities of the device.</span></span> <span data-ttu-id="a1030-344">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="a1030-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a1030-345">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a1030-345">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-346">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a1030-346">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-348">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="a1030-348">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="a1030-349">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="a1030-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a1030-350">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="a1030-350">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-351">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a1030-351">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-353">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="a1030-353">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="a1030-354">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="a1030-354">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a1030-355">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="a1030-355">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-356">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1030-356">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-358">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="a1030-358">Provides high level status information.</span></span> <span data-ttu-id="a1030-359">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="a1030-359">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="a1030-360">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="a1030-360">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a1030-361">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a1030-361">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a1030-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a1030-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-363"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="a1030-363"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-364"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="a1030-364"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-365"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="a1030-365"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="a1030-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a1030-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a1030-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a1030-368">)</span><span class="sxs-lookup"><span data-stu-id="a1030-368">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a1030-369">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="a1030-369">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-370">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1030-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-372">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a1030-372">The last requested or desired state for the element.</span></span> <span data-ttu-id="a1030-373">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a1030-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="a1030-374">Valore</span><span class="sxs-lookup"><span data-stu-id="a1030-374">Value</span></span>                                                                         | <span data-ttu-id="a1030-375">Significato</span><span class="sxs-lookup"><span data-stu-id="a1030-375">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a1030-376"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-376"><dt>12</dt></span></span> </dl> | <span data-ttu-id="a1030-377">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a1030-377">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a1030-378">**Status**</span><span class="sxs-lookup"><span data-stu-id="a1030-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-379">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1030-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-381">Stringa che specifica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a1030-381">A string that specifies the current status of the object.</span></span> <span data-ttu-id="a1030-382">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="a1030-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a1030-383">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a1030-383">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-384">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="a1030-384">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1030-385">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-386">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="a1030-386">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a1030-387">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a1030-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1030-388">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a1030-388">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-389">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1030-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-391">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a1030-391">The current state of the logical device.</span></span> <span data-ttu-id="a1030-392">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="a1030-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a1030-393">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a1030-393">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-394">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1030-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-395">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-396">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="a1030-396">The scoping system's creation class name.</span></span> <span data-ttu-id="a1030-397">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a1030-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a1030-398">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a1030-398">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-399">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1030-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-401">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="a1030-401">The scoping system's name.</span></span> <span data-ttu-id="a1030-402">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a1030-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a1030-403">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="a1030-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-404">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a1030-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-405">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-406">Data o ora dell'Ultima modifica apportata al **EnabledState** dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a1030-406">The date or time when the **EnabledState** of the element last changed.</span></span> <span data-ttu-id="a1030-407">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="a1030-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a1030-408">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="a1030-408">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-409">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a1030-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-411">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="a1030-411">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="a1030-412">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="a1030-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a1030-413">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="a1030-413">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1030-414">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1030-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1030-415">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1030-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1030-416">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a1030-416">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="a1030-417">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a1030-417">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="a1030-418">Valore</span><span class="sxs-lookup"><span data-stu-id="a1030-418">Value</span></span>                                                                         | <span data-ttu-id="a1030-419">Significato</span><span class="sxs-lookup"><span data-stu-id="a1030-419">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a1030-420"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-420"><dt>12</dt></span></span> </dl> | <span data-ttu-id="a1030-421">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a1030-421">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1030-422">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1030-422">Remarks</span></span>

<span data-ttu-id="a1030-423">L'accesso alla **classe \_ VssComponent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="a1030-423">Access to the **Msvm\_VssComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a1030-424">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a1030-424">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1030-425">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1030-425">Requirements</span></span>



| <span data-ttu-id="a1030-426">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1030-426">Requirement</span></span> | <span data-ttu-id="a1030-427">Valore</span><span class="sxs-lookup"><span data-stu-id="a1030-427">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1030-428">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1030-428">Minimum supported client</span></span><br/> | <span data-ttu-id="a1030-429">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a1030-429">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a1030-430">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1030-430">Minimum supported server</span></span><br/> | <span data-ttu-id="a1030-431">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a1030-431">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a1030-432">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a1030-432">Namespace</span></span><br/>                | <span data-ttu-id="a1030-433">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a1030-433">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a1030-434">MOF</span><span class="sxs-lookup"><span data-stu-id="a1030-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1030-435"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-435"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1030-436">DLL</span><span class="sxs-lookup"><span data-stu-id="a1030-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1030-437"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a1030-437"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a1030-438">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1030-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1030-439">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="a1030-439">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="a1030-440">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="a1030-440">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

